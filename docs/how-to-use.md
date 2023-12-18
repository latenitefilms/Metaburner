# How To Use

Metaburner Pro is currently in **early development**.

If you're interested in helping with development, you can sign up to **TestFlight** [here](https://testflight.apple.com/join/dw7S2veN).

Got ideas or questions? Post them on our [Discussions page](https://github.com/latenitefilms/metaburnerpro/discussions)!

Found a bug? Post about it on our [Issues page](https://github.com/latenitefilms/metaburnerpro/issues).

![](/static/overlay-example.png)

---

### Known Issues & Limitations

#### Metaburner Pro v1.0.0 (Build 6)

**19th December 2023**

- The **Primary Storyline** Content Source will only work with `Asset Clips` currently (i.e. not Multicam, Synchronised Clips, Titles, Compound Clips, etc.).
- When using the **Primary Storyline** Content Source, sometimes the first frame of an `Asset Clip` will display no date. This is a bug I'm trying to hunt down.
- **Lane 1**, **Lane 2** and **Lane 3** Content Sources currently just display the text "TBC".
- The **Control** buttons currently don't do anything.
- The **Preset** buttons currently don't do anything.

Got ideas or questions? Post them on our [Discussions page](https://github.com/latenitefilms/metaburnerpro/discussions)!

Found a bug? Post about it on our [Issues page](https://github.com/latenitefilms/metaburnerpro/issues).

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

After installing the Motion Template, you can find the Metaburner Pro Title at the top of the Title sidebar in Final Cut Pro:

![](static/title-browser.png)

---

### Title Inspector

Simply add the Metaburner Pro Title to the top of your timeline as an adjustment layer.

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

So that Metaburner Pro can access all the metadata in your project/timeline, you need to drag your project/timeline from the **Browser** to the drop zone at the top of the Inspector:

![](static/drop-zone.png)

What metadata Final Cut Pro provides when dragging a project/timeline, depends on what **Metadata View** you currently have selected in the **Info Inspector**:

![](static/metadata-view.png)

Final Cut Pro can be a bit temperamental when dragging things from the Browser to the Inspector over the Viewer, so you might have to drag it slowly/carefully for it to work. Sometimes the Inspector will change views, which breaks the workflow, so simply try again.

We have also noticed that sometimes Final Cut Pro can crash when exporting FCPXMLs, as documented [here](https://github.com/CommandPost/FCPCafe/issues/307). We hope that Apple will address this in a future Final Cut Pro update.

You will see a progress alert whilst Metaburner Pro is processing:

![](static/loading.png)

You can **Cancel** it if it's taking a very long time and try again.

Once you've successfully imported a project/timeline, you'll get a message like this:

![](static/import-complete.png)

Once done, Metaburner Pro has access to all the metadata within the FCPXML to populate all the Content Sources.

If you make changes to the project/timeline, you'll need to drag the project back again to update the contents of Metaburner Pro.