![Screenshot iOS](https://i.imgur.com/Bcnlfbn.png)
<p align="center">
    <img src="https://img.shields.io/badge/Swift-4.2-orange.svg" />
</p>

## 📲 How to Run/Test?

Download .zip file `TestJuan.zip` and open `TestJuan.xcworkspace`.

## 📚 External libraries?
I use two external libraries by CocoaPods. `Lottie` (for micro-interaccions) and `RealmSwift` (To save data locally). Pods dependencies are commited inside folder. Pod install is not neccesary. Just run `TestJuan.xcworkspace`.

## 🌟 Primary Goals

- [x] Build an app that can display the user’s current location on a map
- [x] Update the map in real time as the user moves.
- [x] In response to a “tracking on/off” UI switch, record or do not record the user’s movements.
- [x] Display a path over the map as the user moves.
- [x] If a journey is defined as a set of recorded locations between a tracking on and a tracking off switch, retain the user’s journeys.
- [x] Allow the user to see all their journeys in a list. 
- [x] Allow the user to see the start and end times of their journeys when they select them from the list.
- [x] The app should record the user’s location in the background if the user selects “tracking on” and backgrounds the app.
- [x] The app should not use the battery if the user selects “tracking off” and backgrounds the app.
- [x] If the app is resumed from the background during tracking, it should correctly display a path representing the journey that is currently being recorded.


## 🌟🌟 Bonus Goals

- [x] Allow the user to see each journey’s path plotted on a map, when selected from the list.
- [x] Show any other interesting data you can think of relating to a journey, when selected from the list.
- [x] Secure the data that’s stored on the device.

## 🌟🌟🌟 Optional Goals
`I haven´t time to complete optional goals =(`

- [] Retain the user’s data if the app is deleted and re-installed.
I can use `Running Workout Sessions` and `Healtkit` in order to complete this goal. I have an personal application named `Waterink` that use this feature. Check `Waterink` in AppStore.
- [] Detect the user’s motion, and automatically determine when to turn tracking “on” or “off”, in a way that conserves battery power.
I can use `Motion Activity` to do this. But I have no time to implement. 


## 💡 Extra features (My ideas in order to build a cool iOS lovelly product)
- [x] Onboarding
- [x] Cool location permission handler
- [x] Focus on iOS Product. Design guidelines and UX
- [x] Micro-interaction with Lottie
- [x] Realm to save data locally
- [x] Current Journey card
- [x] Feedback generator
- [x] You can see current Journey path and old paths history without stop current recording.
- [x] See date on Journey card
- [x] Minimal validation to save new Journey

## 📈 Architecture

### 1 - LocationManager.swift 
```swift
Abstraction layer to handle native CLLocationManager. Receive location updates from VCs.
```

### 2 - JourneyManager.swift
```swift
Abstraction to manage current Journey and all historic (Saved) Journies. 
```

### 3 - StorageManager.swift
```swift
Abstraction layer to save data locally with Realm.
```

### 4 - JourneyViewModel.swift
```swift
Represent a Journey (ViewModel) for ViewControllers.
```

### 5 - JourneyModel.swift and LocationModel.swift
```swift
Represent persistense layer objects. To save into Realm.
```

### 6 - ComponentFactory.swift
```swift
Commonds and shared UI components factory.
```

### 7 - MainViewController.swift
```swift
Launch transition and permissions handler.
```

### 8 - MapViewController.swift
```swift
Handle Map user interactions. Include JourneyViewController as child container.
```

### 9 - JourneyViewController.swift
```swift
Journey list (CollectionView) and switch on/off.
```

### 10 - ComponentFactory.swift
```swift
Commonds and shared UI components factory.
```

### 11 - AppDelegate.swift
```swift
Initialize managers.
```

## 🎨 Consistency Colors
I create a basic pallete based on OpenTrens main color (aprox).
![Screenshot iOS](https://i.imgur.com/KDDv8n9l.jpg)


### 📋 Supported OS
* iOS 12.0+
* Swift 4.2
* xCode 10+

## 👨🏻‍💻 Author
Juan Sanzone - juan.sanzone@gmail.com
❤️ I love iOS Mobile Products. ❤️ 
