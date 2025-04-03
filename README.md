# Habit Card Iconz
<a href="https://jitpack.io/#Jithin-Jude/hciconz"><img src="https://jitpack.io/v/Jithin-Jude/hciconz.svg"></a>
<a href="LICENSE">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg"></a>

270+ icons accross 5 different categories.</br>
A Big thanks to [Lucide](https://lucide.dev)

<img src="https://github.com/Jithin-Jude/hciconz/blob/7b44b9762346152cd36ab31716b15f7e5a81b4b9/images/iconz.png" width=15% height=15%>

[Quick try icons on Habit Card](https://play.google.com/store/apps/details?id=habit.tracker.habitcard)

## Usage

### Dependencies

add inside `settings.gradle.kts`
```
	dependencyResolutionManagement {
		repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
		repositories {
			mavenCentral()
			maven { url = uri("https://jitpack.io") }
		}
	}
```

add inside `build.gradle.kts` [app level]
```
	dependencies {
	        implementation("com.github.Jithin-Jude:hciconz:1.0.0")
	}
```
```
import habit.tracker.hciconz.HCIconUtils.allHabitIconList
```

### Display Icon
```
                Icon(
                    imageVector = ImageVector.vectorResource(id = habit.tracker.hciconz.HCIconUtils.hcIcPlus.iconRes),
                    tint = Color.Green,
                    contentDescription = "Add",
                    modifier = Modifier
                        .size(48.dp)
                )
```

### Suggestions for improvements are welcome
