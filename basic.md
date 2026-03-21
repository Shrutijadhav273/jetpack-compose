🔹 What is Jetpack Compose?

Jetpack Compose is a modern UI toolkit developed by Google for building native Android user interfaces using Kotlin.

It replaces the traditional XML-based UI system
Uses a declarative programming approach
UI is built using functions (Composable functions)

🔹 Declarative UI vs Imperative UI

✅ Declarative UI (Used in Compose)
In declarative UI, you describe what the UI should look like based on the current data (state).

UI automatically updates when data changes
Less code, easier to maintain

Example idea:

Text("Hello $name")
👉 When name changes → UI updates automatically

❌ Imperative UI (Old Android XML approach)
In imperative UI, you describe how to change UI step-by-step.

You manually update views
More boilerplate code

Example idea:

textView.setText("Hello " + name)