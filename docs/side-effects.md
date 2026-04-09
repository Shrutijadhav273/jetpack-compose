1. LaunchedEffect (MOST IMPORTANT)
📌 Use when:
You want to run code once
Or when some value changes
✅ Example: Run once
@Composable
fun MyScreen() {
    LaunchedEffect(Unit) {
        println("Runs only once")
    }

    Text("Hello")
}
✅ Example: When value changes
@Composable
fun Counter() {
    var count = remember { mutableStateOf(0) }

    LaunchedEffect(count.value) {
        println("Count changed: ${count.value}")
    }

    Button(onClick = { count.value++ }) {
        Text("Count: ${count.value}")
    }
}
🧠 Key Point:
Runs in coroutine
Safe for API calls


2. SideEffect
📌 Use when:
You want to run code after every recomposition
✅ Example:
@Composable
fun MyScreen(name: String) {
    SideEffect {
        println("Runs every recomposition: $name")
    }

    Text(name)
}
🧠 Key Point:
Runs again and again
Avoid heavy work here ❌


3. DisposableEffect
📌 Use when:
You need cleanup
Like:
Stop listener
Remove observer
Release resources
✅ Example:
@Composable
fun MyScreen() {
    DisposableEffect(Unit) {

        println("Start something")

        onDispose {
            println("Clean up when screen removed")
        }
    }

    Text("Hello")
}
🧠 Key Point:
onDispose {} is called when composable is destroyed


4. rememberCoroutineScope
📌 Use when:
You want to run coroutine on button click or event
✅ Example:
@Composable
fun MyScreen() {
    val scope = rememberCoroutineScope()

    Button(onClick = {
        scope.launch {
            println("Running inside coroutine")
        }
    }) {
        Text("Click Me")
    }
}
🧠 Key Point:
Used for user actions
Not automatic like LaunchedEffect