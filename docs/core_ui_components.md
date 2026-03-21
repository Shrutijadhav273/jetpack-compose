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


🖼️ 3. Image
Displays images from resources or internet.

🧠 Example (from drawable):
Image(
    painter = painterResource(id = R.drawable.sample),
    contentDescription = "Sample Image"
)

🔑 Important:
painter → image source
contentDescription → accessibility (VERY important)
💡 With size:
Image(
    painter = painterResource(R.drawable.sample),
    contentDescription = "Profile",
    modifier = Modifier.size(100.dp)
)


⭐ 4. Icon
Small graphical symbol (like heart, menu, back arrow).

🧠 Example:
Icon(
    imageVector = Icons.Default.Home,
    contentDescription = "Home Icon"
)
🔑 Key points:
Uses Material icons
Lightweight compared to Image
💡 Clickable Icon:
Icon(
    imageVector = Icons.Default.Favorite,
    contentDescription = "Like",
    modifier = Modifier.clickable { }
)