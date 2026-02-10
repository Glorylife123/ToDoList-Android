# ToDoList Android App

A modern, clean Todo List application for Android, built with Capacitor from vanilla JavaScript web technologies.

## Features

- **Add Tasks** - Create new tasks with a single click or press Enter
- **Delete Tasks** - Remove tasks you no longer need
- **Mark Complete** - Toggle task completion status with checkboxes
- **Task Filtering** - View All, Pending, or Completed tasks
- **Search** - Quickly find tasks by keyword
- **Statistics Panel** - Real-time display of total, completed, and pending task counts
- **Multilingual Support** - Switch between Chinese and English instantly
- **Data Persistence** - Tasks are saved to localStorage
- **Responsive Design** - Optimized for mobile devices
- **Offline Support** - Works without internet connection

## Download APK

### Automatic Builds
Every push to the `main` branch automatically builds and releases a new APK:

1. Visit [Releases](https://github.com/Glorylife123/ToDoList-Android/releases)
2. Download the latest `app-debug.apk`
3. Install on your Android device

### Download from Workflow
1. Visit [Actions](https://github.com/Glorylife123/ToDoList-Android/actions)
2. Click the latest workflow run
3. Download the APK from the Artifacts section

## Project Structure

```
ToDoList/
├── www/                   # Web application source
│   ├── index.html        # Main HTML page
│   ├── css/
│   │   └── style.css     # Styles and animations
│   └── js/
│       └── app.js        # Application logic
├── android/              # Android native project
│   └── app/              # Android app module
├── capacitor.config.ts   # Capacitor configuration
├── package.json          # Node dependencies
└── .github/
    └── workflows/
        └── build-android.yml  # CI/CD for APK building
```

## Building Locally

### Prerequisites
- Node.js 22+
- Java 21+
- Android Studio or Android SDK

### Build Steps

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Sync Capacitor**
   ```bash
   npx cap sync android
   ```

3. **Open in Android Studio**
   ```bash
   npx cap open android
   ```

4. **Build APK in Android Studio**
   - Build → Build Bundle(s) / APK(s) → Build APK(s)
   - APK will be in `android/app/build/outputs/apk/debug/`

### Or use command line

```bash
cd android
./gradlew assembleDebug
```

## Development

### Syncing changes
After modifying the web files in `www/`, sync to Android:

```bash
npx cap copy android
```

### Running on emulator/device
```bash
npx cap run android
```

## Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic markup |
| **CSS3** | Modern styling with animations |
| **JavaScript (ES6+)** | Application logic |
| **Capacitor** | Cross-platform native wrapper |
| **Android SDK** | Native Android platform |
| **Gradle** | Build system |

## License

MIT
