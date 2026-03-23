Material Design in Jetpack Compose

👉 Material Design is a design system created by Google.

It provides:

Ready-made UI components
Consistent design (colors, typography, spacing)
Modern look & feel



1. Buttons

👉 Used for user actions (click events)

✅ Basic Button
Button(onClick = { }) {
    Text("Click Me")
}
🔹 Types of Buttons
Button Type	Use
Button	Primary action
OutlinedButton	Secondary
TextButton	Minimal
ElevatedButton	With shadow
✅ Example
Button(
    onClick = { },
    modifier = Modifier.fillMaxWidth()
) {
    Text("Submit")
}


🧩 2. Cards

👉 Used to group content (like items, profiles, posts)

✅ Basic Card
Card(
    modifier = Modifier
        .fillMaxWidth()
        .padding(8.dp)
) {
    Text(
        text = "This is a Card",
        modifier = Modifier.padding(16.dp)
    )
}

📌 Use cases:
Product items
Notes
List items
