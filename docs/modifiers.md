MODIFIERS :
Modifiers are used to:

Change UI appearance
Control layout (size, position)
Add behavior (click, scroll, etc.)


🧩 1. padding

👉 Adds space inside the component

Text(
    text = "Hello",
    modifier = Modifier.padding(16.dp)
)

📌 Result:

Space between text and its boundary
🧩 2. margin (Indirect in Compose)

❗ Important:
👉 Compose does NOT have a direct margin

Instead, we use:

Modifier.padding()

👉 Difference:

padding = inside space
margin = outside space

👉 In Compose:
➡️ Parent controls spacing (so margin is handled outside)

Example:

Column(
    modifier = Modifier.padding(16.dp) // acts like margin
)
🧩 3. background

👉 Adds background color or shape

Box(
    modifier = Modifier
        .background(Color.Blue)
        .padding(16.dp)
)

📌 Order matters:

background applied first
then padding
🧩 4. clickable

👉 Makes component interactive

Text(
    text = "Click me",
    modifier = Modifier.clickable {
        println("Clicked!")
    }
)

📌 Used for:

Buttons
Cards
Any UI interaction
🧩 5. fillMaxWidth()

👉 Makes component take full available width

Text(
    text = "Full width",
    modifier = Modifier.fillMaxWidth()
)