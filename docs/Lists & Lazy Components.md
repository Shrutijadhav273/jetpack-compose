🚀 What does “Lazy” mean?

👉 “Lazy” = only render items that are visible on screen

📌 This improves:

Performance ⚡
Memory usage 💾 


🔁 RecyclerView Equivalent

👉 In old Android (XML system), we used:

RecyclerView

👉 In Compose:

LazyColumn (vertical list)
LazyRow (horizontal list)

✔️ No Adapter needed
✔️ No ViewHolder needed
✔️ Much simpler code

🧩 1. LazyColumn (Vertical List)

👉 Works like RecyclerView (vertical scrolling)

LazyColumn {
    items(10) { index ->
        Text(text = "Item $index")
    }
}

📌 Output:

Scrollable vertical list
✅ With Data List
val names = listOf("Shruti", "Amit", "Neha")

LazyColumn {
    items(names) { name ->
        Text(text = name)
    }
}
