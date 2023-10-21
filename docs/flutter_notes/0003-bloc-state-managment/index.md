---
created: 2023-10-18T16:38:53+05:30
updated: 2023-10-21T16:50:11+05:30
title: Best State Managment Practice to Follow in Oceanmtech
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

## Refer Official Documentation for Latest Updates

## How BLoC & Cubit Works (Working flow)

## Equatable Package & Uses

## Create Basic Application

## Local BLoC Declaration

## Global BLoC Declaration

## Bloc Best Practice (Declare, Initialise, Dispose)

##
