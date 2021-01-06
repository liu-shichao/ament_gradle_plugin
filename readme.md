```
./gradlew publishHelloPublicationToMavenRepository 
```

output file in the 'repo'


### using in android 


1.
```
apply plugin: 'com.github.liushichao.gradles'

```

2.
```
buildscript {
  repositories {
    google()
    jcenter()
    mavenCentral()
    mavenLocal()
      maven {
          url("/Users/liushichao/workspace/gradles/ament_gradle_plugin/repo")
      }
//      maven {
//          url("https://plugins.gradle.org/m2/")
//      }

  }

  dependencies {
    classpath 'com.android.tools.build:aapt2:3.6.4-6197926'
    classpath 'com.android.tools.build:gradle:3.6.4'
//      classpath "org.ros2.tools.gradle:ament:0.7.0"
      classpath "com.github.liushichao.gradles:ament:0.0.1"
  }
}
```