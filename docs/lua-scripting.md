# Lua Scripting

An incredible powerful feature of Metaburner Pro is the ability to code your own Lua scripts.

Simply use the **Lua** Content Source, then use the **Custom Field** to type your code.

Anything you write to the `result` global variable will be displayed in Metaburner Pro.

For example:

![](/static/lua-scripting.png)

You have access to the full FCPXML via the `fcpxmlData` global variable, which is stored as a `string`:

![](/static/lua-fcpxml.png)

You have access to Metaburner Pro's processed data via the `processedData` global variable, which is stored as a `table`:

![](/static/lua-processed-data.png)

You can manipulate this data any way you want.

The Lua environment is shared between all instances of the Metaburner Pro plugin, so you can even pass information between different Metaburner Pro Titles!

You can learn more about Lua Scripting on the [CommandPost website](https://commandpost.io/developer/lua-overview/).