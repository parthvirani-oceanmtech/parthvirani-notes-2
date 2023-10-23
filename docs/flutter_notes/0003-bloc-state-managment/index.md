---
created: 2023-10-18T16:38:53+05:30
updated: 2023-10-23T15:03:54+05:30
title: Best State Management Practice to Follow in Oceanmtech
share: "true"
---

# State Management (BLoC)

**Best Bloc State management practice to follow in oceanmtech**

## Why State Management

### Importance of State Management

- State Management ae aek critical aspects che top-notch flutter application create karva mate and as a seasoned flutter developer tamne significance state management idea hashe.
- Generally State management dynamic, interective and responsive way ma user no experience better karava mate help karshe, aapde aa article ma details ma state management and different state management nu brief overview aapvana chavi.
- Aapde throughout article ma comprehensive state management ni guide jovana chavi jema major backbone discuss karvana che ae topic nu list ma nichena point cover karishu:
- Fundamental Concepts ma aapde basic fundamental concept jovana chavi jema basic of state managment aavshe and state management nu solid foundation create karvani try karavanu che
- Poor state management ae mostly set state thi jova male che aetle aeno use always avoid karvano jyare pan state management no use karvano hoy tyare.
- Just Demo create karvano hoy standalone application ma tyare ae setstate no use valid che but large scale ni application or live project hoy tyare tya bhul thi pan setstate no use nai karvano and always je pan state management no use karta hov aeno j karvano reshe.
- amaro je experience che ae real time example na based par je che jyare me approx 3 year pela jyare motivation quotes ni application develop kareli tyare home page par bow j element hata jya quetes show thay che ae page par and jyare pan quotes update thay tyare state change mate setstate no use karel je bow j junkey ui generate kari ne aaptu hatu and aena lidhe me ae application aakhi develop thay gayel hati to pan play console ma upload noti kareli just because ae user ne bad experience create kartu hatu and aena pachi getx use karel but same result and guess what jyare bloc sikhi ne implement karel to top level nu performance achive thayel and aena pachi bloc was the preferred solution for every project i developed since the date, and aena pachi je rite bloc ma update aavela ae adapt kari ne finally top level nu bloc state managment thay aenu dhyan ma rakhta hovi chavi.
- setState as flutter built-in method che and ae widget na state ne update karvama help kare che hence ae option small and simple apps mate hoy che.
- Most of flutter developer setstate no use karta hoy che state management karva mate but aapde better option check karvana chavi for example jyare basic state managment mate setstate no use kari ne code develope karo cho tyare tamaro code je rite show thay che aenu example niche aapelo che ae rite hoy shake pachi aapde aagal check kari shu ke bloc ma convert karavathi shu thashe.
- jyare tami set state no use kari ne code implement karo cho for example shopping app hoy tyare ae code niche write karel che ae rite show thato hoy che.

#### Example:

![[attachments/Pasted image 20231021133815.png]]

## State Management Option

- Jyare pan large application par work thatu hoy tyare generally large UI component ne several small pice ma convert karvama aave che jenathi code ni readability improve thay che and jyare multiple component create karel hoy tyare ae crucial point hoy che ke effective communication thay ae bathe smaller component ni vachee and ae component ne always aena state ni khabar hovi jaruri che so ae handle karva mate je technique use thay che aene state management kevay che.
- Jem aapane idea che aem ae aapde setstate no use kari ne kari shakay che but aena advantages and disadvange aapde niche joyela che.
- setState ae simple state management needs mate valid hoy shake but ae unwieldy and hard thay jay jyare large application ne maintain karva mate use thay so luckily aapdi pase bija options available che state management mate.
    1.  **BLoC (Preferred Solution @OceanMTech - Medium or Large Application)**
    2.  **Provider (2nd preferred option - Small to Medium Level Application)**
    3.  **InheritedWidget**
    4.  **MobX**
    5.  **Redux**
    6.  **Riverpod**
    7.  **Cube**
    8.  **GetX**
- jem uper joi shako cho generally aatla major option available hoy che jyare pan state management mate nu option pic kariye tyare type of apps and ketli big thay shake aena basis par pic karvanu hoy che jenathi project ne manage karva easy pade and plus point ke large and complex project easliy manage and scalable thay shake.
- Aapde je major option che aemathi mainly two state management mate jovana chavi aema bloc je aapdu main preferred option che for developing large and scalable application @oceanmtech company and aek provider package option jema small to medium application mate work kariye tyare help karshe but specifically aapde aa article ma BLoC package ne details ma check karvana chavi like best pratice, how to use and how to implement in better way.
- aapde bloc and provider na pros and cons check kariye to ae niche details ma explain karel che:

### BLoC (Pros and Cons)

- Bloc Pattern ae streams no use kari ne state ne manage kare che flutter ma.
- Aa Pattern bow j fine work kare jo application ma bow data fetching and complex data manipulation operation hoy.
- Bloc easily separation create kari ne aapshe business logic ne ui mathi separate karava ma.
- However Bloc ae bit complicated setup thashe and ae overkill pan thay jo aene simple application mate use karvama
- aeno meaning ae nathi ke Simple application ma bloc use karvathi performance down thay but ae simple application ma use na karo to chale baki aek var tamne bloc aavdi jay to pachi tamne bloc sivay bija state managment use kavani pan maja nai aave.

#### Pros:

- Clear separation between UI and Business Logic kari ne aape che janathi easy to modification ui and easy to modification business logic provide kari ne aape che.
- Code ne clean, organized, and maintainable create kari ne aape che and especially for larger apps.
- Enables Easy Testing of App's Business Logic
- Easily Complex State Transitions and Asynchronous Operations effectively way ma handle kari ne aapshe.
- reactive programming and real-time ui updates karvama help karshe.

#### Cons:

- Bloc shikhva mate bit leaning curve ni requirement hoy che and especially je new developers hoy che reactive programming and streams na concepts ma hoy because bloc ae streams na concepts par work kare che.
- Bloc ne setup karva mate boilerplate code required hoy che je simple app ne overly complex feel lagi shake.
- Overuse of blocs ae over-engineered architecture ma convert kari shake che je difficult to maintain thay shake che.
- Number of file generate thay bloc use karvi ae koik developers mate overhelming hoy shake che but thanks to cubit jema file generation ochi hoy che and aapde in details ma check karishu.

#### When to use BLoC:

- When application has complex logic and aene handle karva mate multiple states and asynchronous operations ni requirement hoy tyare bloc no better use thay shake che.
- When Business Logic Test karvanu priority ma hoy tyare ae help kare che.
- Jyare large application ma work karta hov tyare clear separation nu concerns hoy tyare bloc preferred options hoy che.

#### When not to use BLoC:

- For Small apps jema complex state management ni requirement na hoy.
- Jyare app ma simple business logic hoy and ae bija state management thi easily handle thay shake like provider tyare bloc ne avoid kari shakay che.

### Provider (Pros and Cons)

- Provider ae inherited widget option no use kari ne banel che but ae aakhi process ne simplified kari ne aape che.
- Provider ae easy to use hovathi popular state management option bani gayu che flutter ma.
- Provider no use kari ne aapde koi pan widget ne data provide kari shakay che, je flexible and powerful tool che.
- Provider good performance provide kare che and ae optimized che so only ae widget j rebuild thashe jene rebuild karvani jarur hashe.

#### Pros:

- Provider lightweight and flexible state management option che.
- ae granular and localised approach provider kare che for state management compared to other state management options.
- Provider dependency injection allow kare che je object na instances ne easy to share kari aape che across the app
- Ae flutter na other features jeva streams, ChangeNotifier and ValueNotifier sathe integrate sari rite thay shake che.

#### Cons:

- Provider sometime difficult thay jay che setup karvu beginners mate.
- For Managing Complex and Dynamic states ne multiple widget mate shared karvu ae may not be best option.
- Provider ma built-in time-travel debugging support available nathi, so ae sometime hard thay jay certain issue ne debug karva mate

#### When to use Provider:

- Provider good option for small and medium-sized apps with simpler state management options
- App ma hierarchical structure hoy with nested widget je same state no access kare tyare provider good choice hoy shake
- Jyare object ne multiple part ma share karvano hoy tyare provider will be good solution

#### When not to use Provider:

- Large apps and complex state management hoy tyare provider may not be the best option.
- Jyare multiple state share thata hoy across many parts of app and lot's of dependency hoy tyare bloc choose karvu vadhu better hoy che.
- Bow simple state management ni needs hoy tyare state management library no use na karvo jovo like jyare normal demo create karta hov tyare.

### Conclusion:

- Small and Medium Size na project mate provider ae great choice hoy che but larger apps mate powerfull state management no use karvu preferred solution hoy che.
- Jyare Large Project hoy tyare bloc use karavanu else small and medium level mate provider use karvu jove.

## About BLoC State Management

**(Preferred @OceanMTech Private Limited)**

- Business Logic Components (BLoC) ae business logic ne UI thi separate karva mate thay che and BLoC ma karel code ae easier to write and test ma reuse karva mate help kare che.
- Simple terms ma bloc ae streams of event no input le che pachi ae event na data ne process kari ne states produced kare che aeno simple flow diagrame niche show karel che.

### How BLoC & Cubit Works (Working flow)

- ![[attachments/Pasted image 20231023091500.png]]
- Jem uper ni image ma demonstration karel che ae rite jyare rotate 90% par click thay tyare RotateEvent dispatched thashe bloc ma and je rotate nu state represent karshe ae RotatedState emit thashe and at the end triangle widget potane rotate karshe based on je state receive thashe aema, Similler way ma Change color to Red button is click thay tyare ae color nu state emit thay ne ColorChangedState return thashe.

### Important BLoC Concepts:

- Aapde Bloc nu details ma aagal joiae ae pela basic bloc na concept joi laiae so aapde batha same page par hova joiae jyare bloc implement kariae tyare.
- BLoC library ma two main component ma devide thayel che aetle BLoC and aek Cubit je bloc par thi generate karel method che but more simplified way ma, so aapde `BLoC` thi start kariye and aena pachi `Cubit` mate in details check karishu.

#### BLoC

- Bloc ni andar generally 3 file generate thay che per bloc wise jema aek event file, bloc file and state file ae rite different file hoy che.
- aa three file no content aapde details ma niche check kariye jema kai file kai rite data aavshe ae joiae one by one so better and clear understanding thay jashe.
- Bloc ne aapde demonstration karvi to ae aa rite work kare:
    ![[attachments/Pasted image 20231023111429.png]]
- Bloc Component takes event as input, analyse it inside bloc, and based on business logic it produces the corresponding states as output.

##### Event File

- Event ae bloc ne instruction pass kare che bloc aenu kaik action perform kare jema generally aapdu business logic hoy che, event ae koi pan place par thi fire kari shakay like UI Widget, External Events such as network connectivity, changes in sensor readings, etc..
- Event file ae generally niche describe karel che ae rite joi shakay che:

```dart

part of 'bottom_navigation_bloc.dart';

abstract class BottomNavigationEvent extends Equatable {
	const BottomNavigationEvent();
}

class BottomNavChangeEvent extends BottomNavigationEvent {

	final int currentIndex;
	const BottomNavChangeEvent({required this.currentIndex});

	@override
	List<Object?> get props => [currentIndex];
}

```

##### BLoC File

- Bloc is a man in the middle, all the business logic hoy ae inside bloc file hoy che ae simply events ne accepts kare, logic perform kare and state as output produce kare, ae generally niche explain karel way ma work karshe.

```dart

class BottomNavigationBloc extends Bloc<BottomNavigationEvent, BottomNavigationState> {

	List loadedPages = [0];
	bool isMounted = true;
	BottomNavigationBloc() : super(const BottomNavChanged(currentIndex: 0))
	{
		on<BottomNavChangeEvent>(bottomNavigationChanged);
	}

	FutureOr<void> bottomNavigationChanged(
		BottomNavChangeEvent event, Emitter<BottomNavigationState> emit
	) async {
			if (!loadedPages.contains(event.currentIndex)) {
				loadedPages.add(event.currentIndex);
			}
			emit(BottomNavChanged(currentIndex: event.currentIndex));
	}
}
```

##### States File

- States ae processed result hoy che je aapde screen side aapde show karvanu hoy che so ae basically je data pan display karvanu hoy ae data aapde states file ma add karvanu hoy che and at a time koi pan single state display thay shake che.
- State file niche display karel che jema aapde je pan possible state hoy ae declare karvana hoy che.

```dart
// ignore_for_file: annotate_overrides, overridden_fields
part of 'bottom_navigation_bloc.dart';

abstract class BottomNavigationState extends Equatable {
	final int currentIndex;
	const BottomNavigationState({required this.currentIndex});

	@override
	List<Object> get props => [currentIndex];
}

class BottomNavChanged extends BottomNavigationState {
	final int currentIndex;
	const BottomNavChanged({required this.currentIndex}) :
		super(currentIndex: currentIndex);

	@override
	List<Object> get props => [currentIndex];
}



class BottomNavErrorState extends BottomNavigationState {

	final int currentIndex;
	const BottomNavErrorState({required this.currentIndex}) :
		super(currentIndex: currentIndex);

	@override
	List<Object> get props => [currentIndex];
}
```

#### Cubit

- Cubit ae bloc no simpler version che jema aapde generally lesser file generate thay che bloc karta and easy to use hoy che jema aapde function declare karela hoy and aena par thi ae data process kari ne state emit karshe.
- Jyare Cubit write karo tyare events file eliminate thay jashe, so thodo boilerplace code remove thay jashe.
- ![[attachments/Pasted image 20231023120159.png]]
- ![[attachments/Pasted image 20231023120218.png]]
- Jem uper na screen ma display karel che ae rite cubit che ae generally function call par aenu logic perform kari ne new state emit karshe.
- Aapde cubit and state file ne details ma check kariye niche:

##### Cubit File

- Jyare pan cubit function call thay tyare new state emit thay and new output generate thashe.

###### Creation of Cubit

```dart
/// A `CounterCubit` which manages an `int` as its state.
class CounterCubit extends Cubit<int> {
  /// The initial state of the `CounterCubit` is 0.
  CounterCubit() : super(0);

  /// When increment is called, the current state
  /// of the cubit is accessed via `state` and
  /// a new `state` is emitted via `emit`.
  void increment() => emit(state + 1);
}
```

##### Using a Cubit

```dart
void main() {
  /// Create a `CounterCubit` instance.
  final cubit = CounterCubit();

  /// Access the state of the `cubit` via `state`.
  print(cubit.state); // 0

  /// Interact with the `cubit` to trigger `state` changes.
  cubit.increment();

  /// Access the new `state`.
  print(cubit.state); // 1

  /// Close the `cubit` when it is no longer needed.
  cubit.close();
}
```

- Jem uper code describe karel che aema increment function che aapde ui side or diffrent cubit mathi call karvanu hoy che and ae aenu logic calculation kari ne next state emit kari ne aapshe.

##### States File

- State file aapde as usual Equatable class thi extends karel hoy che so aema jyare pan data emit thay tyare new state notification generate thashe je widget listen kari ne based on state data ae view update thashe.
- state file ne declare karva mate niche explain karel che:

```dart
part of 'counter_cubit.dart';

abstract class CounterState extends Equatable {

	const CounterState();

	@override
	List<Object?> get props => [];
}

class CounterIncrementState extends CounterState {
	final int counter;

	const CounterIncrementState({required this.counter});

	 @override
	List<Object?> get props => counter];
}
```

- so based on data particular state emit thatu hoy che ae show karvanu hoy che.

## Refer Official Documentation for Latest Updates

- Jyare koi pan concept full details ma check karvanu hoy and always updated solution jotu hoy tyare always official documentation ne refer karvu jove aema always latest updated code hoy che. and BLoC nu official documentation aeni official website par malshe : [BLoC](https://bloclibrary.dev/#/)
- And hu recommanded karu chu ke aekvar aa article read kari lyo pachi complete bloc nu official documentation read kari ne aene samajvani try karvani, because state management ae proper concepts che jene effective way ma implement karvo ae aapdi responsibility che.

## Equatable Package & Uses

- Equatable Package ae Data Comparison mate use thay che jema ae `==` and `hashcode` ne internally overrides kari ne aape che je lots of builerplate code ne remove kare che and ae use case mate aapde `Equatable` ne `States and Events` classes thi extend karvanu hoy che.

### Equatable Implements

```dart
abstract class LoginStates extends Equatable{}
```

- Aene simple terms ma samjavani try karvi to Equatable ae Previous Value and New Value ne compare kare jyare pan state emit thay or event add thay tyare so jo value diffrent hashe to j ae state emit or event add thashe else ae data nu koi affect nai kare.
- So that means LoginStates ae duplicate calls create nai kare and ae state ne pan rebuild nai kare jo same state hashe to.

### Define State:

```dart
abstract class LoginStates extends Equatable{}
```

### Define State with Props:

- props no aek variable aapde override karvano hoy che jyare pan state compared karvanu hoy tyare means ke propes ma jetla variable add karela hashe ae compare thashe and aena based par new state return malshe.

```dart
class LoginData extends LoginStates {
  final bool status;
  final String userName;
  const LoginData({this.status, this.userName});
  @override
  List<Object> get props => [this.status, this.userName];
}
```

- As Explained in above example aapde `status` and `userName` ne observe karvi chavi so jyare `status` and `userName` ni value change thashe tyare aapdu new state emit thashe else nai thay.
- Similler way ma jo apde `userName` ne remove kari daiae props mathi to only `status` variable monitor thashe and hence jyare status variable change thashe tyare ae state emit thashe.
- so aapde `state ne equatable` thi extends karvi tyare ae old state data ne new state data sathe compare kari ne aapshe so new ae following way ma work karshe:

```dart
	emit(LoginData(true, 'Hello User'));
    emit(LoginData(true, 'Hello User')); //this will be avoided
```

## Create Basic Application

## Local BLoC Declaration

- Jyare Declare karel bloc particular class mate use thavano hoy tyare aene screen level par declare karvo ae best option hoy che and aeno object pan ae screen level par declare thay che.
- Lovel Level no bloc ae je te screen mate hoy che like Home Page par na data mate `HomePageBloc or HomePageCubit` na name thi declare karvama aave che.
- Lovel Level na bloc ma jyare bloc declare karel hoy aej file na dispose ma aene close karvano hoy che like `homePageCubit.close();` aanathi memory clean up thay jay che and jyare second time bloc ni jarur hoy tyare recreate kari shakay.

## Global BLoC Declaration

- Jyare Declare karel bloc aakhi app mate use thavano hoy tyare aene global level par declare karvo ae best option hoy che and aeno object singleton hoy tyare pan ae global level par declare thay che.
- Global Level no bloc ae material app ma `MultiBlocProvider` ma declare karvama aave che.
- Global Level na bloc na example joiae to aema Shopping app nu cart `CartCubit or CartBloc` pachi Payment mate nu `PaymentCubit or PaymentBloc` aa type na bloc hoy ae generally app level par declare karvama aave che and aenu dispose pan same file ma create karvama aave che.

## Bloc Best Practice (Declare, Initialise, Dispose)

- Jyare pan bloc declare karo tyare aeno generally based on bloc behaviour like local bloc or app level global bloc che aena based par declare karvano hoy.
- Jyare app level par hoy tyare aene material app file ma `MultiBlocProvider` ma declare kari ne provide karvanu hoy che and aenu dispose pan same file ma aavshe.
- Same way ma locally bloc declare karel hoy to ae BLoC ae perticular file ma declare karvano hoy che and generally initState ma initialisation karvanu hoy che.
- and after ae screen no jyare use na hoy and screen pop thay tyare ene dispose method ma ae particular `bloc` or `cubit` ne close karvu ae mandatory che janathi unnecessary memory consume na kare, and memory leak ne avoid kari shakay che.
- Jyare BlocProvider use karo tyare aena bloc ne dispose karvani koi jarur nathi hoti ae automatic dispose and initialise kari ne aape che.

## BLoC APIs

- BLoC Different APIs Provide kare che and ae no use pan je rite use problem hoy or je rite requirement hoy aena based par aapde aagal prcess karvanu hoy che.
- Bloc different widgets provide kare che:

### **BlocBuilder**

- **BlocBuilder** ae flutter widget che jene bloc and builder banne ni requirement hoy che.
- BlocBuilder ae widget building ne handle kare che based on new state je rite emit thay ae rite.
- Blocbuilder ae similler to StreamBuilder che but BlocBuilder ma simple API che je amount of boilerplace code ne reduce kare che.
- builder function ae potentially many time call thay che ae aena response ma widget ne leshe jyare pan state emit thashe tyare.
- Jo BlocBuilder ma bloc parameter ne ommited(assign na karvi), kariye to ae automatically aena bloc na instance nu lookup karshe using BlocProvider and BuildContext no use kari ne.
- Generally jyare global bloc declare karel hoy tyare.

#### Global Bloc Instance

```dart
BlocBuilder<BlocA, BlocAState>(
  builder: (context, state) {
    // return widget here based on BlocA's state
  }
)
```

- and Jyare pan scoped widget hoy and parent ma accessible na hoy via parent BlocProvider and BuildContext tyare bloc parameter assign karvo jaruri che means local bloc instance create karo tyare
- Genrally Scoped Widget or Local Bloc Instance Use karvano hoy tyare.

#### Local Bloc Instance

```dart
BlocBuilder<BlocA, BlocAState>(
  bloc: blocA, // provide the local bloc instance
  builder: (context, state) {
    // return widget here based on BlocA's state
  }
)
```

- Fine gained control jo implement karvo hoy builder par means ke builder function kyare new state emit refresh karvu jove to aena mate aapdi pase buildWhen function available che jema aapdi pase previousState and newState available hoy che jema aapde based on state condition aapde state rebuild control kari shakay.

```dart
BlocBuilder<BlocA, BlocAState>(
  buildWhen: (previousState, state) {
    // return true/false to determine whether or not
    // to rebuild the widget with state
  },
  builder: (context, state) {
    // return widget here based on BlocA's state
  }
)
```

### **BlocProvider**

- **BlocProvider** is a Flutter widget che je aena children in bloc instance create kare che so aena children using `BlocProvider.of<T>(context)` no use kari ne access kari shake, aa widget depedency injection (DI) ni jem work kare che so single instance multiple widget ne allocate kari shakay within subtree.
- BlocProvider ae potani rite bloc instance create kari shake che so aena subtree widget ne available hoy so `BlocPriver`ae responsible che ke bloc create karva mate and also aene automatically close karva mate.

```dart
BlocProvider(
  create: (BuildContext context) => BlocA(),
  child: ChildA(),
);
```

- By Default `BlocProvider` will create bloc lazily (on-demand je rite required hoy ae rite) and create will get executed when the bloc is looked up via `BlocProvider.of<BlocA>(context)`.
- To override this behavior and force `create` to be run immediately, `lazy` can be set to `false`.

```dart
BlocProvider(
  lazy: false,
  create: (BuildContext context) => BlocA(),
  child: ChildA(),
);
```

- In some cases, aapde `BlocProvider` ne exiting bloc pan assign kari shakay che with in widget tree, so in this case `BlocProvider` automatically close nathi kartu because ae provider ae perticular bloc ne generate nathi karel.

```dart
BlocProvider.value(
  value: BlocProvider.of<BlocA>(context),
  child: ScreenA(),
);
```

then from either `ChildA`, or `ScreenA` we can retrieve `BlocA` with:

```dart
// with extensions
context.read<BlocA>();

// without extensions
BlocProvider.of<BlocA>(context)
```

### **MultiBlocProvider**

**MultiBlocProvider** is a Flutter widget che te multiple `BlocProvider` widgets ne aek widget ma convert kari aape che. `MultiBlocProvider` ae code ni readability and eliminates ne remove karvama help kare che so instead of nesting `BlocProvider` we can use `MultiBlocProvider` :

```dart
BlocProvider<BlocA>(
  create: (BuildContext context) => BlocA(),
  child: BlocProvider<BlocB>(
    create: (BuildContext context) => BlocB(),
    child: BlocProvider<BlocC>(
      create: (BuildContext context) => BlocC(),
      child: ChildA(),
    )
  )
)
```

to:

```dart
MultiBlocProvider(
  providers: [
    BlocProvider<BlocA>(
      create: (BuildContext context) => BlocA(),
    ),
    BlocProvider<BlocB>(
      create: (BuildContext context) => BlocB(),
    ),
    BlocProvider<BlocC>(
      create: (BuildContext context) => BlocC(),
    ),
  ],
  child: ChildA(),
)
```

### **BlocListener**

**BlocListener** ae flutter widget che je state changed par aapde specific operation perform karvu hoy aema help kare che and aema listener method invoke thay che jema based on state value aapde diffrent operation perform kari shakay like `navigation, showing snackbar or showing a dialog` 

`listener` is only called once for each state change (**NOT** including the initial state) unlike `builder` in `BlocBuilder` and is a `void` function.

If the `bloc` parameter is omitted, `BlocListener` will automatically perform a lookup using `BlocProvider` and the current `BuildContext`.

```dart
BlocListener<BlocA, BlocAState>(
  listener: (context, state) {
    // do stuff here based on BlocA's state
  },
  child: Container(),
)
```

Only specify the bloc if you wish to provide a bloc that is otherwise not accessible via `BlocProvider` and the current `BuildContext`.

```dart
BlocListener<BlocA, BlocAState>(
  bloc: blocA,
  listener: (context, state) {
    // do stuff here based on BlocA's state
  },
  child: Container()
)
```

For fine-grained control over when the `listener` function is called an optional `listenWhen` can be provided. `listenWhen` takes the previous bloc state and current bloc state and returns a boolean. If `listenWhen` returns true, `listener` will be called with `state`. If `listenWhen` returns false, `listener` will not be called with `state`.

```dart
BlocListener<BlocA, BlocAState>(
  listenWhen: (previousState, state) {
    // return true/false to determine whether or not
    // to call listener with state
  },
  listener: (context, state) {
    // do stuff here based on BlocA's state
  },
  child: Container(),
)
```

### **MultiBlocListener**

- **MultiBlocListener** is a Flutter widget that merges multiple `BlocListener` widgets into one. `MultiBlocListener` improves the readability and eliminates the need to nest multiple `BlocListeners`. By using `MultiBlocListener` we can go from:

```dart
BlocListener<BlocA, BlocAState>(
  listener: (context, state) {},
  child: BlocListener<BlocB, BlocBState>(
    listener: (context, state) {},
    child: BlocListener<BlocC, BlocCState>(
      listener: (context, state) {},
      child: ChildA(),
    ),
  ),
)
```

to:

```dart
MultiBlocListener(
  listeners: [
    BlocListener<BlocA, BlocAState>(
      listener: (context, state) {},
    ),
    BlocListener<BlocB, BlocBState>(
      listener: (context, state) {},
    ),
    BlocListener<BlocC, BlocCState>(
      listener: (context, state) {},
    ),
  ],
  child: ChildA(),
)
```

### **BlocConsumer**

- **BlocConsumer** exposes a `builder` and `listener` in order to react to new states. `BlocConsumer` is analogous to a nested `BlocListener` and `BlocBuilder` but reduces the amount of boilerplate needed. `BlocConsumer` should only be used when it is necessary to both rebuild UI and execute other reactions to state changes in the `bloc`. `BlocConsumer` takes a required `BlocWidgetBuilder` and `BlocWidgetListener` and an optional `bloc`, `BlocBuilderCondition`, and `BlocListenerCondition`.

If the `bloc` parameter is omitted, `BlocConsumer` will automatically perform a lookup using `BlocProvider` and the current `BuildContext`.

```dart
BlocConsumer<BlocA, BlocAState>(
  listener: (context, state) {
    // do stuff here based on BlocA's state
  },
  builder: (context, state) {
    // return widget here based on BlocA's state
  }
)
```

An optional `listenWhen` and `buildWhen` can be implemented for more granular control over when `listener` and `builder` are called. The `listenWhen` and `buildWhen` will be invoked on each `bloc` `state` change. They each take the previous `state` and current `state` and must return a `bool` which determines whether or not the `builder` and/or `listener` function will be invoked. The previous `state` will be initialized to the `state` of the `bloc` when the `BlocConsumer` is initialized. `listenWhen` and `buildWhen` are optional and if they aren't implemented, they will default to `true`.

```dart
BlocConsumer<BlocA, BlocAState>(
  listenWhen: (previous, current) {
    // return true/false to determine whether or not
    // to invoke listener with state
  },
  listener: (context, state) {
    // do stuff here based on BlocA's state
  },
  buildWhen: (previous, current) {
    // return true/false to determine whether or not
    // to rebuild the widget with state
  },
  builder: (context, state) {
    // return widget here based on BlocA's state
  }
)
```

## Naming Conventions:

- Jyare pan bloc and state or event define karo tyare aeni mate special naming conventions follow karvu mandatory che because jyare large projects and multiple developer aek sathe work karta hoy so aek bija ne esiliy idea aave aena mate strongly recommended che proper namin conventions provide karel hoy.

### Event Conventions

> Events nu name  **past tense** because events are things that have already thay gayel hoy che bloc na perspective thi so aenu naming pan ae rite j aapvanu.

#### Anatomy

`BlocSubject` + `Noun (optional)` + `Verb (event)`

Initial load events should follow the convention: `BlocSubject` + `Started`

The base event class should be name: `BlocSubject` + `Event`.

#### Examples

✅ **Good**

```
sealed class CounterEvent {}
final class CounterStarted extends CounterEvent {}
final class CounterIncrementPressed extends CounterEvent {}
final class CounterDecrementPressed extends CounterEvent {}
final class CounterIncrementRetried extends CounterEvent {}
```

❌ **Bad**

```
sealed class CounterEvent {}
final class Initial extends CounterEvent {}
final class CounterInitialized extends CounterEvent {}
final class Increment extends CounterEvent {}
final class DoIncrement extends CounterEvent {}
final class IncrementCounter extends CounterEvent {}
```

### State Conventions

> States should be nouns because a state is just a snapshot at a particular point in time. There are two common ways to represent state: using subclasses or using a single class.

#### Anatomy

##### Subclasses

`BlocSubject` + `Verb (action)` + `State`

When representing the state as multiple subclasses `State` should be one of the following: `Initial` | `Success` | `Failure` | `InProgress` and initial states should follow the convention: `BlocSubject` + `Initial`.

##### Examples

✅ **Good**

```
sealed class CounterState {}
final class CounterInitial extends CounterState {}
final class CounterLoadInProgress extends CounterState {}
final class CounterLoadSuccess extends CounterState {}
final class CounterLoadFailure extends CounterState {}
```

##### Single Class

`BlocSubject` + `State`

When representing the state as a single base class an enum named `BlocSubject` + `Status` should be used to represent the status of the state: `initial` | `success` | `failure` | `loading`.

The base state class should always be named: `BlocSubject` + `State`.

##### Examples

```
enum CounterStatus { initial, loading, success, failure }
final class CounterState {
  const CounterState({this.status = CounterStatus.initial});
  final CounterStatus status;
}
```

❌ **Bad**

```
sealed class CounterState {}
final class Initial extends CounterState {}
final class Loading extends CounterState {}
final class Success extends CounterState {}
final class Succeeded extends CounterState {}
final class Loaded extends CounterState {}
final class Failure extends CounterState {}
final class Failed extends CounterState {}
```
