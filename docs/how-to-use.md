# How To Use

Metaburner is currently in **active development**. We are aiming to release sometime in January 2024.

If you're interested in helping with development, you can sign up to **TestFlight** (Apple's beta-testing service) for free [here](https://testflight.apple.com/join/dw7S2veN).

We will be posting regular beta builds to TestFlight as we add new features and functionality.

Got ideas or questions? Post them on our [Discussions page](https://github.com/latenitefilms/metaburner/discussions)!

![](/static/metaburner-pro-screenshot.jpeg)

---

### Known Issues & Bugs

Please check the [Issues page](https://github.com/latenitefilms/metaburner/issues) for any known bugs or issues.

You can find the full release notes [here](/release-notes/).

---

### Final Cut Pro Bug

**UPDATE:** As of Metaburner 1.0.0 (Build 20) we now workaround this issue.

There is currently a bug in Final Cut Pro 10.7.1, where it incorrectly exports FCPXML `v1.11` when projects have Multicam Clips with individual Audio Role Voice Isolation.

Because Metaburner only accepts valid FCPXML files, if you have a project that has Multicam Clips with individual Audio Role Voice Isolation, it won't import into Metaburner.

You can confirm this is the issue by exporting a FCPXML to your Desktop, then bringing it back it.

If you're hitting this bug you'll see something like this:

![](static/invalid-fcpxml.png)

The workaround is to instead export a FCPXML `v1.10` instead, then use the **Controls > Import Project via FCPXML** to bring it into Metaburner.

You can learn more about the bug on FCP Cafe [here](https://github.com/CommandPost/FCPCafe/issues/314).

We encourage you to also report it to Apple so they can fix it in the next update.

---

### Error Logs

You can press the **Reveal Log Files** button in the **Controls** section of the Inspector to access the `FxPlug.log` file in Finder:

![](static/reveal-log-files.png)

The log file is located here:

```
~/Library/Containers/com.latenitefilms.MetaburnerRenderer/Data/Library/Application Support/FxPlug.log
```

You can press the **Reveal Crash Logs** button in the **Controls** section of the Inspector to access the `DiagnosticReports` folder in Finder.

![](static/reveal-log-files.png)

The crash logs are located here:

```
~/Library/Logs/DiagnosticReports
```

The crash logs will have file names like `Metaburner Renderer-2023-12-24-103301.ips`. They might also be in the `Retired` sub-folder (these are reports that have already been posted to Apple).

Alternatively, you can access your User Library, by clicking on your **Desktop**, then holding down **OPTION** as you click the **Go** menu item in Finder. A **Library** option will appear:

![](static/finder-library.png)

You can also copy the above paths, press **COMMAND+SHIFT+G** from Finder (or via the **Go > Go to Folder...** menubar item), and paste in that path into the **Go to Folder** popup.

---

### Installing

If it's the first time installing the software, or if there's been an update to the Motion Template, you'll be prompted to **Install Motion Template**.

![](static/install-01.png)

Once you click the button, you'll be prompted to grant permission to your **Movies** folder. This is due to macOS's sandboxing, and you'll only need to do this once. Click **OK**.

![](static/install-02.png)

You then need to click **Grant Access**:

![](static/install-03.png)

Once done, you'll be presented with a successful message:

![](static/install-04.png)

The button will now be disabled, and will say **Motion Template Installed**. You can now close the Gyroflow Toolbox application.

![](static/install-05.png)

---

### Accessing in Final Cut Pro

After installing the Motion Template, you can find the Metaburner Title at the top of the Title sidebar in Final Cut Pro:

![](static/title-browser.png)

---

### Title Inspector

Simply add the Metaburner Title to the top of your timeline as an adjustment layer.

It should start at the very start of your timeline.

![](static/timeline.png)

You can then control it via the Inspector:

![](static/inspector.png)

There are **25 customisable text layers**, which you can customise however you want.

There are **Global Settings** which apply to all Text Layers:

![](static/global-settings.png)

You can override these Global Settings on an individual text layer by deselecting the **Use Global Settings** checkbox:

![](static/text-layer.png)

The **Content Source** dropdown is where you select where you want to get your metadata from.

![](static/content-source.png)

If you select **Custom Text** it will use the Custom Text textbox in the Inspector.

If you select **Project**, it will get the metadata from the project/timeline.

If you select **Primary Storyline**, it will get the metadata from the primary storyline, etc.

If you've selected something other than **Custom Text** you must then select a **Content Field**.

![](static/content-field.png)

For example, if you have **Project** selected in the **Content Source**, and **Name** selected in the **Content Field**, then it will display the name of your **Project** (after you drop a Final Cut Pro Project into the drop zone).

You can add a **Prefix** and a **Suffix** to all text fields, regardless of the **Content Source** and **Content Field**.

When you first add the Metaburner Title, it will display this image in your Viewer:

![](static/no-project-loaded.png)

As the image explains, so that Metaburner can access all the metadata in your project/timeline, you need to drag your project/timeline from the **Browser** to the drop zone at the top of the Inspector:

![](static/drop-zone.png)

What metadata Final Cut Pro provides when dragging a project/timeline, depends on what **Metadata View** you currently have selected in the **Info Inspector**:

![](static/metadata-view.png)

> Final Cut Pro can be a bit temperamental when dragging things from the Browser to the Inspector over the Viewer, so you might have to drag it slowly/carefully for it to work. Sometimes the Inspector will change views, which breaks the workflow, so simply try again.
>
> We have also noticed that sometimes Final Cut Pro can crash when exporting FCPXMLs, as documented [here](https://github.com/CommandPost/FCPCafe/issues/307). We hope that Apple will address this in a future Final Cut Pro update.

After dropping a FCPXML, the status text will change to **Analysing Project**:

![](static/loading-fcpxml.png)

After a short time, if successful, the status should change to **Project Loaded**:

![](static/project-loaded.png)

> Final Cut Pro can be a bit temperamental in terms of updating the status, so you may need to click away from the Metaburner Title and then go back to it for the text to update.

Once done, Metaburner has access to all the metadata within the FCPXML to populate all the Content Sources.

If you make changes to the project/timeline, you'll need to drag the project back again to update the contents of Metaburner.

If Metaburner was unable to import the FCPXML, you'll get an error status, which you can hover over with your mouse to get more detail:

![](static/error-in-inspector.png)

If you do run into an error, it's most likely a bug in Metaburner, so please share your Error Log and FCPXML on GitHub [here](https://github.com/latenitefilms/metaburner/issues).

---

### Custom Metadata Field

When you have the **Custom Metadata Field** selected, you also need to supply a **Custom Field** with the **key** for that metadata field.

For example, if you have the **Extended** Metadata View selected in the **Info Inspector**:

![](static/extended-metadata-inspector.png)

If you then export a FCPXML with the **Extended** Metadata View:

![](static/save-extended-metadata.png)

...and you open that file up in TextEdit, you'll see something like this within the FCPXML:

```
<metadata>
    <md key="com.apple.proapps.studio.reel" value="My Reel"/>
    <md key="com.apple.proapps.studio.scene" value="My Scene"/>
    <md key="com.apple.proapps.studio.shot" value="My Take"/>
    <md key="com.apple.proapps.studio.angle" value="My Camera Angle"/>
</metadata>
```

You can then use **com.apple.proapps.studio.reel** in the **Custom Field** within the Metaburner Inspector to display the Reel.

Keep in mind that Metaburner only has access to whatever metadata you have visible in the **Info Inspector**, so make sure you select the correct **Metadata View** before dragging your project to Metaburner's Drop Zone.

---

### Lua Scripting

You can learn more [here](/lua-scripting/).