---
created: 2023-10-18T16:38:53+05:30
updated: 2023-10-19T16:57:26+05:30
title: Best App Architecture Practice to Follow in Oceanmtech
share: "true"
---

# Clean Architecture + Feature First Moduler


![[attachments/Pasted image 20231005203824.png]]

![[attachments/Pasted image 20231005203846.png]]


Uper nu je structure che aenu architecture calling nicheni sequence based karvanu reshe jenathi easy way ma implementation karvama help karshe:

## How perform clean architecture

### Generate Model Class (Data Layer)

**Generate Model Class- (Api na response no use kari ne model generate karvanu first) (Data Layer)**

- Je pan api ma responce male aene json to dart convert kari ne jem possible hoy ae rite common model generate karvana so app side pass karvama easy pade.
- Ae model ma renaming karvanu, jya nullable vairable hoy tya nullable karvanu and jya na hoy to tya null handle karvanu
- proper variable ma convert karvanu like int value 0/1 api side thi aavti hoy je bool mate use thay to app side aene bool ma convert karvanu
- possible hoy tya default value assign karvani and try catch no proper use karvano
- infuture scenario ne dhyan ma rakhi ne model ne restructure karvanu and aena naming pan je type ni functinality hoy ae rite rename karvanu jenathi infuture search and idetify karva mate easy reshe.
- je name nu model hoy ae name nu j file name hovu jaruri che suppose ke home data fetch karvanu model che to class name should be HomeDataModel and filename will be home_data_model.dart
- model class ne entity class ni sathe inherit karvanu so jyare model no construcuture intilize thay tyare entity file no constructure pan call thay.
- Aa file Data Layer par models folder ma create karvani hoy che (data->models->home_data_model.dart)

#### Example: 
![[attachments/Pasted image 20231018142845.png]]

###  Generate Data Entity Class  (Domain Layer)
**Generate Data Entity File - Based on Model Class (Domain Layer)**
- Je pan model class che aema all type na data aavi shake che admin ni api mathi ae might be usefull hoy and na pan hoy at that moment but future ma usefull hoy to admin data send karshe.
- But app side jetlu show karvanu hoy aetla variables ne j lai ne aagal vadhvanu hoy che to aena mate aapde entity file no use karvi chavi jema only ui side variable ni jarur pade aetlu j rakhvanu.
- entity file ne equatable class thi extends always karvano so je pan entity file che ae monitor thashe
- Entity file ma aapde copywith method or tojson method je rite requiered hoy ae rite set karvanu
- entity file ma je parameter hashe aej aapde ui side use karvana aavshe to aena basis par aema parameter hova jaruri che.
- Entity file nu name je rite use hoy ae rite rakhvanu like jo home data che to aapde model class nu name HomeDataModel rakhelu same way ma HomeDataEntity name reshe entity class nu and file name for that will be home_data_entity.dart
- Aa file Domain Layer par entities folder ma create karvani hoy che (domain->entities->home_data_entity.dart)

#### Example: 
![[attachments/Pasted image 20231018142903.png]]

### Generate Use Case (Domain Layer)

**Generate Use Case file (Domain Layer) **
- Aek var model and entity class generation done thay pachi aeno usecase create karvano because ae place par aapde je response jove che ae allocate karvano hoy che.
- Usecase: ae aek abstract class che so je pan class aene call karshe ae class ne Usecase in method implement karvani reshe.
- Use case nu naming je use mathe thatvanu hoy ae rakhvanu reshe like home data fetch karavana che to GetHomeData and file name for that use case will be get_home_data.dart
- Usecase no type define karva mate ae two type na params pick karshe jema aek response type aavshe and aek api ma pass karva mate params class aavshe.
- For Example home data get karvanu che to aeno response class nu name UseCase<HomeDataEntity, HomeDataParams> aa rite usecase ni type defined karvani reshe and jo koi api ma params pass nathi thata to NoParams as params type select karavnu reshe.
- Usecase jyare pan generate karo tyare tamne idea hovo jove ke kai repository mathia e usecase return thavano che and aeno object create karvano je help karshe api call implement karvama,

- DartZ Package:
	- DartZ Package aek class provide kar che Either name nu and ae class ma type define karvani hoy che jema Left and Right Params na format ma ae accepts kare che
	- Left Params tyare use thay jyare error hoy and RIght side params tyare use thay jyare success result hoy so aena base par aapde aeni return type lakvani hoy che.
	- Suppose aapde home data fetch karvi chavi to Either type aa rite defin thashe: Either<AppError,HomeDataEntity>.
	- aa usecase no je cubit mathi call thato hoy tya aene .fold no use kari ne left and right variable expose thashe jeno use karni aapde condition lakhi shakay che. 

- Usecase ma je call method che aema return type aapde Either use karvi chavi jeme aeni type defin karvani hoy che.
- Je ether type che ae either type throught call defined karvani reshe jo jyare remote data source mathi response return thay tyare ae type ma j data return thavo joiae and ae na thay to error generate thashe.
- finally call repository function call from usecase and pass the params if you had else leave it as it as. 
- Aa file Domain Layer par usecases folder ma create karvani hoy che (domain->usecases->get_home_data.dart)

#### Example: 
![[attachments/Pasted image 20231018142910.png]]

###  Dependency Injection (get_it.dart)

 **Register Above created UseCase in Dependency Injection file(get_it.dart)**

- Aek var usecase create thay jay pachi aene dependency injection ma register karvanu reshe ae karvathi aapde jyare pan je file ne aeni requirement hashe tyare aene provide kari shakay
- Dependency Injection ae loose coupling create karshe jenathi ae koi pan class aek bija par depedent nai reshe, and jyare je pan usecase, repository, data source or cubit ni requirement hashe tyare ae allocate on-demand kari shakashe.
- Aema aapde two type na registration karvana hoy che maily jema aek registerFactory and registerLazySingleton method use kari ne register karvana hoy che.
- registoryFactory aena mate use thay jyare aapde multiple time aeno diffrent object creation or dispose and recreate karvana hovi and ae mostly cubit registration ma jova maslshe.
- registerLazySingleton no use jyare singleton object create karvano hoy tyare use thay che ae mostly datasource, reposotory and usecase ma use thashe.
- Dependency Injection ae file ni dependency ne resolve karva mate use thay che, jem ke koi cubit create karel che to aene registration kari ne aeni dependency biji file ma allocate karavama use thay che.
- Jyare pan data repository, data source, usecase ke cubit create karo aetle aene class na creation done thay aeni sathe get_it ma registration kari devanu
- Aa file di(dependency injection) folder ma hoy che (lib->di->get_it.dart)

#### Example: 
![[attachments/Pasted image 20231018142916.png]]

###   Remote Repository Abstract Class  (Domain Layer)

** Remote Repository Abstract Class Registration (Domain Layer)**
- Aekvar usecase register thay jay pachi aene domain layer ma register karvanu with same return type of usecase.
- Aa place par method declare thashe aetle pachi data layer par aa class extends thayel hovathi ae class ma implementation aavshe.
- aa file nu location data layer ma aavshe (lib->domain->repositories->remote_repository.dart)

#### Example: 
![[attachments/Pasted image 20231018142925.png]]

 
###  Remote Repository Implementation (Data Layer)
**Remote Repository Implementation (Data Layer)**
- aekvar remote repository ma method declare thay jay pachi aene data layer par ni remote repository ma implementation karvanu reshe and aa file data layer par available hashe
- aa file nu location data layer ma aavshe (lib->data->repositories->remote_repository_impl.dart)
- aa file ma remote data source na abstract class no object create karel jene call karvanu hoy che. 

#### Example: 
![[attachments/Pasted image 20231018142943.png]]

### Remote Data Source Abstract Class (Data Layer)

**Remote Data Source Abstract Class Registration (Data Layer)**
- Remote Repository implementation na class ma aek var implement thay pachi tyathi je method no call abstract class ma karel hoy aene absract class ma declare karvani with same method return type je remote repository ma hoy ae.
- aa file che aenu implementation je class aa ne extends kare aene karvanu reshe.
- aa file nu location data layer ma aavshe: (lib->data->data_sources->remote_data_source.dart)

#### Example: 
![[attachments/Pasted image 20231018142950.png]]

### Remote Data Source Implementation (Data Layer)

**Remote Data Source Implementation (Data Layer)**
- Remote Data Source na abstract class nu implementation aa class ma karvanu hoy che and aa class same file (lib->data->data_sources->remote_data_source.dart) abstract class ni niche declare thayel hoy che.
- aa class ma api implementation thayel hoy che aema aene handle karine valid left and right params return karvana hoy che je pan scenario hoy aena base.

#### Example: 
![[attachments/Pasted image 20231018142933.png]]

###  Params File(Domain Layer)

- Params file aapde jyare api ma parameter pass karvana hovi tyare create karvani hoy che, je usecase na type ma pass karvani hoy che.
- Aa file Domain Layer par params folder ma create karvani hoy che (domain->entities->params)

#### Example: 
 ![[attachments/Pasted image 20231018142957.png]]

### Args File(Domain Layer)

- Args file aapde jyare aek screen mathi biji screen ma navigation karvi and ae time par aek karta vadhu argument hoy tyare better hoy che ke args class create kari ne navigation kariye.
- Aa file Domain Layer par args folder ma create karvani hoy che (domain->entities->args)

#### Example: 
![[attachments/Pasted image 20231018164330.png]]

### Extra Important Notes:

- Uper ni je process explain karel che ae industry standard clean architecture no use kari ne karel che and aa generally large level na project mate hoy che basic project mate alag alag architecture available hoy che like MVC, MVP, MVVM, Stacked Arch etc.
- je uper no flow che ae aapda project ma implementation thashe and jyare je architecture implementation karvau thashe tyare inform karvama aavshe.
- For Clean Architecture je uper ni sequence ma explain karel che ae same sequence ma j always calling reshe and jo ae rite sequence ma implementation karsho to easy way ma api calling implement thay jashe.
- aek point dhyan ma rakhvano ke file name and class name valid hovu jove because big architecture and project ma indivisual file find karvama bow time lagto hoy che to better che ke ae name yad hoy jaldi find kari shakay che and ae pratice follow karvani reshe.
- Aapde Feature First Clean Architecture use karishu so aene jyare pan implement karo aetle tamne je feature allocate thayl che aena par j work karvanu che and je feature nu folder che tya j aene add karvanu che .
- aena sivay tami shared feature modify kari shako cho and common file modify kari shako cho baki bija na koi na feature ma implement karvanu nai aave.
- Koi pan problem hoy architecture samajvama to tamara team leader ne or tamara team member ne puchi ne confirm kari levu jenathi wrong implementation na karvu pade.
- Feature nu folder creation karava mate vscode extension no use karvano jenathi easily folder create thashe and and je folder name invalid che to aene rename kari ne aapde je rite use karvanu che ae rite kari devanu:


#### Feature First Clean Architecture VSCode Extension: 

- Download from visual studio marketplace: https://marketplace.visualstudio.com/items?itemName=KiritchoukC.flutter-clean-architecture 


### Read More at:

#### Explore More on Scalable App Architecture – [CodeWithAndrea](https://codewithandrea.com/articles/flutter-project-structure/)

1. https://github.com/md-siam/scalable_app_architecture?ref=flutterawesome.com
2. https://flutterawesome.com/a-modular-app-architecture-that-can-be-scalable-as-the-time-passes/
3. https://dev.to/mjablecnik/flutter-modular-architecture-2f15
4. https://codewithandrea.com/articles/comparison-flutter-app-architectures/
5. https://codewithandrea.com/articles/flutter-project-structure/
