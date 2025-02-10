## Install android studio
- setup a basic project using empty activity.
- minimum sdk api 24 (7) (nougat)
- build and refresh

```kotlin
class MainActivity : ComponentActivity() {
	override fun onCreate(savedInstanceState: Bundle?) {
		super.onCreate(savedInstanceState)
		setContent {
			GreetingCardTheme {
			// A surface container using the 'background' color from theme
				Surface(
					modifier = Modifier.fillMaxSize(),
					color = MaterialTheme.colorScheme.background
				) {
					Greeting("Android")
				}
			}
		}
	}
}
```

- The `onCreate()` function is the entry point to this Android app and calls other functions to build the user interface. In Kotlin programs, the `main()` function is the entry point/starting point of execution. In Android apps, the `onCreate()` function fills that role.
- The [`setContent()`](https://developer.android.com/reference/kotlin/androidx/compose/ui/platform/ComposeView#setContent\(kotlin.Function0\)) function within the `onCreate()` function is used to define your layout through composable functions. All functions marked with the `@Composable` annotation can be called from the `setContent()` function or from other Composable functions. The annotation tells the Kotlin compiler that this function is used by Jetpack Compose to generate the UI.

```kotlin
@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {
	Text(
		text = "Hello $name!",
		modifier = modifier
	)
}
```

- above greetings function is a composable function, use @Composable annotation before the function.
- @Composable function names are capitalized
- @Composable functions can't return anything.

```kotlin
@Preview(showBackground = true)  
@Composable  
fun GreetingPreview() {  
    GreetingCardTheme {  
        Greeting("Saad")  
    }  
}
```

- The `GreetingPreview()` function is a cool feature that lets you see what your composable looks like without having to build your entire app. To enable a preview of a composable, annotate with `@Composable` and `@Preview`. The `@Preview` annotation tells Android Studio that this composable should be shown in the design view of this file.
- As you can see, the `@Preview` annotation takes in a parameter called `showBackground`. If `showBackground` is set to **true**, it will add a background to your composable preview.
- Since Android Studio by default uses a light theme for the editor, it can be hard to see the difference between `showBackground` `=` `true` and `showBackground` `=` `false`. However, this is an example of what the difference looks like.

## Change the bg color

- To set a different background color for your introduction, you'll need to surround your text with a [`Surface`](https://developer.android.com/reference/kotlin/androidx/compose/material/package-summary#Surface\(androidx.compose.ui.Modifier,androidx.compose.ui.graphics.Shape,androidx.compose.ui.graphics.Color,androidx.compose.ui.graphics.Color,androidx.compose.foundation.BorderStroke,androidx.compose.ui.unit.Dp,kotlin.Function0\)). A `Surface` is a container that represents a section of UI where you can alter the appearance, such as the background color or border.

```kotlin
@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {    
	Surface(color = Color.Cyan) {        
		Text(            
			text = "Hi, my name is $name!",            
			modifier = modifier        
		)    
	}
}
```

- Highlight `text` and right click, then
- Surround with widget => Surround with container 
- By default the container is set to Box 
- Surface can have a parameter color set it to Color
- import `androidx.compose.ui.graphics.Color`
- after importing you can do like this Color.Cyan or Color.black or Color.Blue

## Add Padding

just use modifier.padding(24.dp)
dp here is density independent pixel
- A [`Modifier`](https://developer.android.com/reference/kotlin/androidx/compose/ui/Modifier) is used to augment or decorate a composable. One modifier you can use is the `padding` modifier, which adds space around the element (in this case, adding space around the text). This is accomplished by using the [`Modifier.padding()`](https://developer.android.com/reference/kotlin/androidx/compose/ui/Modifier#\(androidx.compose.ui.Modifier\).padding\(androidx.compose.ui.unit.Dp\)) function.
- Every composable should have an optional parameter of the type `Modifier`. This should be the first optional parameter.

```kotlin
@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {
	Surface(color = Color.Cyan) {
		Text(
			text = "Hi my name is $name!"
			modifier = modifier.padding(24.dp)
		)
	}
}
```

- These imports are necessary
	- import androidx.compose.ui.unit.dp
	- import androidx.compose.foundation.layout.padding