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