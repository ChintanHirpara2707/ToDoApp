# To-Do App (Android) - Kotlin

A simple and efficient To-Do app built using Kotlin and Android Studio. This app allows users to create, read, update, delete, and search tasks. It also features time tracking for each task and stores tasks locally for persistence. 

## Features

- **Create Tasks**: Add new tasks with titles and descriptions.
- **Read Tasks**: View the list of tasks stored locally.
- **Update Tasks**: Edit existing tasks.
- **Delete Tasks**: Remove tasks from the list.
- **Time Tracking**: Add a due time for each task.
- **Search Tasks**: Easily search for tasks by title or description.
- **Local Storage**: Tasks are saved locally using Room Database for persistence.

## Tech Stack

- **Programming Language**: Kotlin
- **Framework**: Android SDK
- **Architecture**: MVVM (Model-View-ViewModel)
- **Local Storage**: Room Database
- **Search Functionality**: Room with LiveData and Flow
- **Time**: DatePicker and TimePicker for task scheduling

## Getting Started

To get a copy of this project running on your local machine for development and testing, follow these steps.

### Prerequisites

- Android Studio installed on your machine
- JDK 8 or later
- Kotlin plugin (usually pre-installed in Android Studio)

### Clone the Repository

1. Open your terminal/command line interface.
2. Clone the repository:

   ```sh
   git clone https://github.com/ChintanHirpara2707/ToDoApp.git
   ```

3. Build and run the app on an emulator or a physical device.

### Open in Android Studio

1. Open Android Studio.
2. Select **Open an existing project** and navigate to the project folder.
3. Android Studio will automatically sync and download the necessary dependencies.

### Build and Run

1. Connect your Android device via USB or use an emulator.
2. Click on the **Run** button in Android Studio (the green play button).
3. The app should now launch on your device or emulator.

### Gradle Configuration

Ensure that your project is set up with the correct Android SDK version in the `build.gradle` files.

#### App-level `build.gradle.kts`:

Make sure to set `compileSdk` and `targetSdk` to **35** as per the following:

```kotlin name=app/build.gradle.kts
plugins {
    id("com.android.application")
    id("org.jetbrains.kotlin.android")
}

android {
    compileSdk = 35
    defaultConfig {
        applicationId = "com.example.todoapp"
        minSdk = 21
        targetSdk = 35
        versionCode = 1
        versionName = "1.0"
    }
    buildTypes {
        release {
            isMinifyEnabled = false
            proguardFiles(getDefaultProguardFile("proguard-android-optimize.txt"), "proguard-rules.pro")
        }
    }
}

dependencies {
    implementation("androidx.core:core-ktx:1.6.0")
    implementation("androidx.appcompat:appcompat:1.3.1")
    implementation("androidx.constraintlayout:constraintlayout:2.0.4")
    implementation("androidx.lifecycle:lifecycle-runtime-ktx:2.3.1")
    implementation("androidx.room:room-runtime:2.3.0")
    kapt("androidx.room:room-compiler:2.3.0")
    implementation("androidx.recyclerview:recyclerview:1.2.0")
    implementation("androidx.lifecycle:lifecycle-livedata-ktx:2.3.1")
    implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:2.3.1")
    implementation("com.google.android.material:material:1.4.0")
}
```

### SDK Location Setup

To ensure Android Studio can find the correct Android SDK, make sure your `local.properties` file is set up with the proper SDK location.

Open or create the `local.properties` file in the root directory of your project and add the following line (modify the path to reflect the actual location of your SDK):

```properties name=local.properties
sdk.dir=/path/to/your/android/sdk
```

For example, on Windows, the path might look like this:

```properties name=local.properties
sdk.dir=C:\\Users\\YourUsername\\AppData\\Local\\Android\\Sdk
```

## Usage

1. Launch the app on your device.
2. Use the add button to create a new task.
3. View your tasks in the list.
4. Tap on a task to edit or delete it.
5. Use the search bar to find specific tasks.
6. Track the time spent on each task.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspiration from various to-do list applications.
- Thanks to the open-source community for their valuable contributions.
