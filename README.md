# LoloWard Android App

مرحباً بك في تطبيق LoloWard - تطبيق Android يعرض مجموعة من الصور والأشكال والحيوانات والأشياء.

Welcome to LoloWard Android App - An Android application that displays a collection of images, shapes, animals, and objects.

## Features / المميزات

- 📱 Native Android application built with Kotlin
- 🖼️ Image gallery with categorized content
- 🐱 Animals section with various animals
- 🔷 Shapes and objects collection
- 🌟 Modern Material Design UI
- 🇦🇪 Arabic language support

## Build Instructions / تعليمات البناء

### Local Build / البناء المحلي

1. Clone the repository:
```bash
git clone https://github.com/ahmadox1/loloward.git
cd loloward
```

2. Build the project:
```bash
./gradlew build
```

3. Generate debug APK:
```bash
./gradlew assembleDebug
```

4. Generate release APK:
```bash
./gradlew assembleRelease
```

The APK files will be generated in `app/build/outputs/apk/`

### GitHub Actions Build / البناء باستخدام GitHub Actions

This project is configured with GitHub Actions for automated builds. Every push to the main branch or pull request will trigger:

- Automated build process
- APK generation (debug and release)
- Test execution
- Artifact upload

You can download the generated APKs from the Actions tab in the GitHub repository.

## Requirements / المتطلبات

- Android API Level 21+ (Android 5.0+)
- JDK 17
- Android SDK
- Gradle 8.0+

## Project Structure / هيكل المشروع

```
loloward/
├── app/
│   ├── src/main/
│   │   ├── java/com/ahmadox1/loloward/
│   │   │   └── MainActivity.kt
│   │   ├── res/
│   │   │   ├── drawable/          # Image resources
│   │   │   ├── layout/            # Layout files
│   │   │   ├── values/            # Strings, colors, themes
│   │   │   └── mipmap-*/          # App icons
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── gradle/wrapper/
├── .github/workflows/
│   └── build.yml                  # GitHub Actions workflow
├── build.gradle
├── settings.gradle
└── gradlew

# Original image assets (preserved)
├── animals/                       # Animal images
├── images/                        # General images
├── objects/                       # Object images
└── shapes/                        # Shape images
```

## Contributing / المساهمة

Feel free to contribute to this project by:
- Adding new features
- Improving the UI/UX
- Adding more images to the gallery
- Translating to other languages

## License

This project is open source. Please check the repository for license information.

---

Made with ❤️ by [ahmadox1](https://github.com/ahmadox1)