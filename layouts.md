Layouts in Compose?

Layouts control how UI elements are arranged.

In Compose, layouts are also functions.

🧱 Most Important Layouts
1. Column (Vertical layout)
@Composable
fun ColumnExample() {
    Column {
        Text("First")
        Text("Second")
    }
}

👉 Output:

First
Second
2. Row (Horizontal layout)
@Composable
fun RowExample() {
    Row {
        Text("Left")
        Text("Right")
    }
}

👉 Output:

Left   Right
3. Box (Stack layout)
@Composable
fun BoxExample() {
    Box {
        Text("Bottom")
        Text("Top")
    }
}

👉 Items are placed on top of each other

🔹 3. Modifiers (VERY IMPORTANT)

Modifiers control:

Size
Padding
Background
Alignment
Text(
    "Hello",
    modifier = Modifier
        .padding(16.dp)
        .background(Color.Yellow)
)
🔹 4. Combining Layouts (Real Example)
@Composable
fun ProfileCard() {
    Row(modifier = Modifier.padding(16.dp)) {
        
        Column {
            Text("Shruti")
            Text("Android Developer")
        }
    }
}