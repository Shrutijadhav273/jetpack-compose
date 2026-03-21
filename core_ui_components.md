🧩 1. Text
Used to display text on the screen.

🧠 Example:
Text(text = "Hello World")

🔑 Important properties:
text → what you want to show
color → text color
fontSize → size of text
fontWeight → bold/light

💡 Example with styling:
Text(
    text = "Hello Shruti",
    color = Color.Blue,
    fontSize = 20.sp,
    fontWeight = FontWeight.Bold
)


🔘 2. Button
A clickable component used for user actions.

🧠 Basic example:
Button(onClick = { 
    println("Button clicked") 
}) {
    Text("Click Me")
}

🔑 Key points:
onClick → action when clicked
Inside {} → UI of the button (usually Text)
💡 Styled Button:
Button(
    onClick = { /* action */ },
    colors = ButtonDefaults.buttonColors(Color.Green)
) {
    Text("Submit")
}

