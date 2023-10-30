### Hi there 👋

## This is a public mirror of a private repository of Odontoo App which you can find at Google Play store [HERE](https://play.google.com/store/apps/details?id=com.tanany365.odontoo)

<h1 align="center">Odontoo Connect</h1>

<p align="center">
  <a href="https://android-arsenal.com/api?level=24"><img alt="API" src="https://img.shields.io/badge/API-24%2B-brightgreen.svg?style=flat"/></a>
</p>

<p align="center">  
🦷 Odontoo Connect is a communication facilittor app targeting dentists with privacy as the main concern.
</p>
</br>

<p align="center">
<img src="https://github.com/tanany365/Odontoo-Connect/blob/main/assets/collage.png"/>
</p>

## Download
Find it on Play Store Here <a href='https://play.google.com/store/apps/details?id=com.tanany365.odontoo'>
<img src='https://simplemobiletools.com/images/button-google-play.svg' alt='Get it on Google Play' height='45' />
</a>

<img src="/previews/preview.gif" align="right" width="320"/>

## Tech stack 📚 :
- Minimum SDK level 24
- [Kotlin](https://kotlinlang.org/) based, [Coroutines](https://github.com/Kotlin/kotlinx.coroutines) + [Flow](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/) for asynchronous.
- Jetpack
    - [Compose](https://developer.android.com/jetpack/compose): Declarative UI library for building awesome UI.
        - [Material 3](https://developer.android.com/jetpack/androidx/releases/compose-material3): Google Material Design Library for ready-made UI components.
        - [Navigation](https://developer.android.com/jetpack/compose/navigation): Library of Navigation component for Compose support.
    - [Lifecycle](https://developer.android.com/reference/androidx/lifecycle/package-summary): Observe Android lifecycles and handle UI states upon the lifecycle changes.
    - [ViewModel](https://developer.android.com/reference/androidx/lifecycle/viewmodel/package-summary): Manages UI-related data holder and lifecycle aware. Allows data to survive configuration changes such as screen rotations.
    - [Room](https://developer.android.com/reference/androidx/room/package-summary): Constructs Database by providing an abstraction layer over SQLite to allow fluent database access.
    - [Hilt](https://dagger.dev/hilt/): for dependency injection.
    - [Paging 3](https://developer.android.com/topic/libraries/architecture/paging/v3-overview): Library for returning paging data from Room local database.

- [Firebase Analytics/Crashlytics](https://firebase.google.com/docs/analytics): App Monitoring and Analytics.
- [Google Ad mob](https://admob.google.com/home/): App onetization using Google Ad Mob



## Architecture
- MVVM Architecture (Model - View - ViewModel)
- Layered Architecture
    - Data Layer
    - Domain Lyaer (UseCase)
    - Presentation Layer

### Architecture Overview

![architecture](https://github.com/tanany365/Odontoo-Connect/blob/main/assets/system-design-odontoo-AddContact.drawio.png)

The overall architecture of **Odontoo Connect** is composed of three layers; the UI layer, domain layer and the data layer. Each layer has dedicated components and they have each different responsibilities, as defined below:

### Presentation Layer

![architecture](https://github.com/tanany365/Odontoo-Connect/blob/main/assets/arch-presentation-layer.png)

The Presentation layer consists of UI elements to configure screens that could interact with users and [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel) that holds app states and restores data when configuration changes.

**Unidirectional** Data flow principle is applied through firing events from Screen UI and passing data toward Screen


### Domain Layer

![architecture](https://github.com/tanany365/Odontoo-Connect/blob/main/assets/arch-domainlayer.png)

### Data Layer

![architecture](https://github.com/tanany365/Odontoo-Connect/blob/main/assets/arch-data-layer.png)

The data Layer consists of repositories implementation, which include business logic, such as querying data from the local database.. It is implemented as an offline source of business logic and follows the [single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth) principle.<br>

**Odontoo Connect** is an offline app is an app that is able to perform all core functionality without access to the internet. 