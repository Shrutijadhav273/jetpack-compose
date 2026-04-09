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