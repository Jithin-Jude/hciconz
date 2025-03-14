# Habit Card Iconz
<a href="https://jitpack.io/#Jithin-Jude/hciconz"><img src="https://jitpack.io/v/Jithin-Jude/hciconz.svg"></a>
<a href="LICENSE">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg"></a>

For the past few years, I was using Lottie for showing both loading & other custom animations. Even tho Lottie is providing cooler animations, one major issue I was facing was that the Lottie files are not doing well in terms of performance.

So here is a <b>simple, performance-oriented, lightweight, easy-to-use</b> library for showing loading screen while app is doing heavy background tasks & network calls.

<img src="https://github.com/Jithin-Jude/lib_simpleloader/blob/feb5ea9ac1323fac14093e8287c88e7a6dda7615/images/loader_with_message_screenshot.jpg" width=25% height=25%>

[Buy Me a Coffee](https://www.buymeacoffee.com/jithinjude1997)

## Usage

### Dependencies

add inside `settings.gradle`
```
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

add inside `build.gradle` [app level]
```
dependencies {
	implementation 'com.github.Jithin-Jude:lib_simpleloader:1.0.2'
}
```
```
import dev.jithinjude.simpleloader.FullScreenLoader
```

### Loader initialization
```
var fullScreenLoader: FullScreenLoader? = null
fullScreenLoader = FullScreenLoader(context)
fullScreenLoader?.show()
```

### Loader listener
```
val callback = object : FullScreenLoader.FullScreenLoaderListener {
            override fun onFullScreenLoaderInitialized() {
                fullScreenLoader?.setLoaderColor(getColor(R.color.happy_yellow))
                fullScreenLoader?.setLoadingMessage("Loading message...")
            }

            override fun onFullScreenLoaderDismissed() {
                Timber.e("onFulScreenLoaderDismissed :=> callback worked")
            }
        }

fullScreenLoader?.setFullScreenLoadingDismissListener(callback)
```

### Making loader dismissible
```
fullScreenLoader?.setLoaderCancelable(true)
```

### Set Loader Color
```
fullScreenLoader?.setLoaderColor(getColor(R.color.yellow))
```

### Set Loading message
```
fullScreenLoader?.setLoadingMessage("Your loading message...")
```

### Suggestions for improvements are welcome
