# RunTrack

RunTrack is a fitness tracking app utilizing modern Android technologies, including Jetpack Compose, MVVM architecture, and the Google Maps API. The app enables users to track their running activities, displaying real-time routes on an interactive map and storing essential statistics using a Room database.

---

## Features

1. **Live Activity Tracking**: Track running activities using GPS.
2. **Interactive Map**: Display running paths on a map using the Google Map Compose library.
3. **Foreground Service**: Continues tracking stats even when the app is closed or removed from the background.
4. **Statistics Management**: Store and manage running statistics with Room database.
5. **Advanced Navigation**: Handle nested navigation, deep linking, and conditional navigation to onboarding screens using the Jetpack Navigation Component.
6. **Image Picker**: Use the new Jetpack Compose image picker to select images without requiring permissions.
7. **Paging 3 Integration**: Efficiently load large datasets.
8. **Dynamic Themes**: Support dynamic colors for light and dark themes.
9. **Graphical Statistics**: Display weekly statistics with filters in graphical format.

---

## Screenshots

| Home Screen                                                                                                           | Live Tracking                                                                                                     | Running Info                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| ![run_track_home_ss](https://github.com/user-attachments/assets/6a104b92-06ac-40fd-9b32-0b85d9544446)                | ![runtrack_live_tracking_ss](https://github.com/user-attachments/assets/fd86f2cb-4114-41c5-ac43-06005cfcfbe9)    | ![runtrack_running_info_ss](https://github.com/user-attachments/assets/78e422ba-b6dd-41a6-8ccc-045a99658aae)    |
| Statistics                                                                                                           | Profile                                                                                                           | All Runs                                                                                                         |
| ![run_track_statistics_ss](https://github.com/sDevPrem/run-track/assets/130966261/b9d92744-7de1-461e-b96f-56950689e0a4) | ![runtrack_profile_ss](https://github.com/user-attachments/assets/0574c8e1-87a3-4858-9c09-5a347d4b5c02)          | ![runtrack_all_run_screen_ss](https://github.com/user-attachments/assets/58b6d8c6-bca2-40b4-ade8-e05e0e4ceec9)   |

---

## Package Structure

```
app
├── background: Handles background processes, such as services.
├── data: Responsible for data management, including entities, databases, and tracking.
│   ├── tracking: Handles location tracking.
├── di: Hilt modules for dependency injection.
├── domain: Contains use cases and interfaces.
├── ui: UI layer of the app.
│   ├── nav: Manages app navigation and destinations.
│   ├── screen: UI screens.
│   ├── theme: Material3 theme configurations.
│   ├── common: Common UI components and utilities.
├── common: Utility classes used across the app.
```

---

## Built With

- **[Kotlin](https://kotlinlang.org/):** Programming language.
- **[Jetpack Compose](https://developer.android.com/jetpack/compose):** UI development.
- **[Jetpack Navigation](https://developer.android.com/jetpack/compose/navigation):** Navigation management.
- **[Room](https://developer.android.com/jetpack/androidx/releases/room):** Database for statistics.
- **[Google Maps API](https://developers.google.com/maps/documentation/android-sdk):** Map integration for tracking speed, distance, and paths.
- **[Hilt](https://developer.android.com/training/dependency-injection/hilt-android):** Dependency injection.
- **[Preferences DataStore](https://developer.android.com/topic/libraries/architecture/datastore):** User data storage.
- **[Coil](https://coil-kt.github.io/coil/compose/):** Asynchronous image loading.
- **[Vico](https://patrykandpatrick.com/vico/):** Graph rendering for statistics.

---

## Architecture

The app follows the **MVVM architecture**, **Unidirectional Data Flow (UDF)** pattern, and **Single Responsibility Principle**.

### Tracking Architecture Diagram

![tracking_architecture](https://github.com/sDevPrem/run-track/assets/130966261/932e9df7-cf34-4902-aa84-73a6431ca236)

---

## Installation

1. Clone this repository and open it in Android Studio.
2. Follow the steps below for Google Maps integration (optional).

### Google Maps Integration

1. Obtain a Google Maps API key by following [this guide](https://developers.google.com/maps/documentation/android-sdk/get-api-key).
2. Open the `local.properties` file.
3. Add the following line:
   ```
   MAPS_API_KEY=your_maps_api_key
   ```

---
