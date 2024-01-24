Fixes the "Only supported on Bukkit 1.7+" error message when using ACF on modern Spigot versions.

## Maven
```xml
<repositories>
    <repository>
        <id>jeff-media-public</id>
        <url>https://repo.jeff-media.com/public/</url>
    </repository>
    <repository>
        <id>aikar</id>
        <url>https://repo.aikar.co/content/groups/aikar/</url>
    </repository>
</repositories>

<dependencies>
    <dependency>
        <groupId>com.github.spigotbasics</groupId>
        <artifactId>acf-paper</artifactId>
        <version>0.5.1-SNAPSHOT</version>
        <scope>compile</scope>
    </dependency>
</dependencies>
```

## Gradle Kotlin DSL
```kotlin
repositories {

    maven {
        name = "jeff-media-public"
        url = uri("https://repo.jeff-media.com/public/")
        content {
            includeGroup("com.jeff-media")
            includeGroup("com.github.spigotbasics")
        }
    }

    maven {
        name = "aikar"
        url = uri("https://repo.aikar.co/content/groups/aikar/")
        content {
            includeGroup("co.aikar")
        }
    }
}

dependencies {
    implementation("com.github.spigotbasics:acf-paper:0.5.1-SNAPSHOT") // or api(...)
}
```

## Gradle Groovy
Use Kotlin DSL.