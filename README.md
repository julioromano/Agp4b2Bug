# Agp4b2Bug
Sample to reproduce a potential bug reported to Google.

Bug report at: https://issuetracker.google.com/issues/151649643

Instructions to reproduce:
 - Uncomment the following line from app/build.gradle:
   
   `// implementation 'com.segment.analytics.android:analytics:4.3.1' // Uncomment this to reproduce!`
 - Run the debug build within Android Studio 4.0 beta02 on an API23 emulator.
 - App will crash on startup with a ClassNotFoundException.
 - Disabling coreLibraryDesugaringEnabled and removing its desugar_jdk_libs dependency solves the issue.
