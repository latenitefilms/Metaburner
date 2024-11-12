# Release Notes

### 1.1.0 (51)

**🎉 Released:**
- 12th November 2024

**🆕 Important Changes**
- This is a major update to Metaburner, and is not backwards compatible with previous releases.
- If you were previously using Metaburner, you'll need to delete any existing Metaburner titles and re-apply them.
- We have done major under-the-hood improvements to how we get the source timecode from clips.
- The **Audio Role** text field is currently not hooked up.

🔨 **Improvements:**
- Renamed **Content Source** to **Metadata Source**.
- Renamed **Content Field** to **Metadata Property**.
- Renamed **Custom Field** to **Custom Metadata"**.
- Changed order of parameters in the Inspector.
- Added a dedicated **Lua Script** text field.
- Added support for **Stabilisation** metadata.
- Added **Video - Source Frame Count** Metadata Property.
- **Filter by Video/Audio Role** now only works with complete Role names.
- Rather than aborting if we hit invalid timecode, we now just log an error and allow the invalid timecode.
- Added **Duration on Timeline (Frames)** Metadata Property.
- We now get the Source Start Timecode, Source Duration & Source Frame Rate from the source clip, instead of the parent clip on the timeline.
- Various other under-the-hood speed improvements, bug fixes and improvements.

---

### 1.0.7 (35)

**🎉 Released:**
- 24th January 2024

🐞 **Bug Fix:**
- Fixed a bug which caused the Final Cut Pro Viewer to appear "red" when using a Metaburner Title, even if the Title was disabled. This only affected Intel machines, not Apple Silicon. This was due to Metaburner's on-screen controls (that allow you to drag Text Layers in the Viewer). The red overlay disappeared on Intel if you disabled the on-screen controls in Apple Motion. Thanks for reporting Matthieu Laclau! Thanks Darrin Cardani and Gabriele de Simone for your problem solving genius!

---

### 1.0.6 (34)

**🎉 Released:**
- 23rd January 2024

🔨 **Changes:**
- Metaburner Presets now have the file extension `metaburnerPreset` (instead of `mbpPreset`).
- The Metaburner Motion Template has been updated.

🔨 **Improvements:**
- Lots of big under-the-hood improvements. Metaburner now can handle very complicated and long feature film timelines without dropping frames. Thanks for reporting Sam Pluemacher!
- Added a new **Open in Motion** button to **Controls**. This allows you to easily create a new Apple Motion Template which you can customise however you want!
- We've moved the **Open User Guide** to the top of **Controls** so that it's more obvious.
- We no longer display "Text Layer 1", "Text Layer 2", etc in the Final Cut Pro Inspector to make it cleaner.
- We now save and restore **Empty Data**, **Filter by Video Role** and **Filter by Audio Role** in Presets.
- We've added a built-in **Stabilisation** Preset.
- Improved the error messaging when a FCPXML fails to load.
- Added a checkbox to **Save FCPXML Internally** within the **Controls** section. This is off by default. You'll only ever really need to turn it on if you want to access the FCPXML data via the Lua Scripting Engine.

🐞 **Bug Fixes:**
- Metaburner now correctly renders when in **Half Resolution** in Apple Motion and **Better Performance** in Final Cut Pro.
- Final Cut Pro now allows you to copy and paste the Metaburner Title. Thanks for reporting Sam Pluemacher!

---

### 1.0.5 (33)

**🎉 Released:**
- 20th January 2024

🔨 **Improvements:**
- Added a Global Setting for **Empty Data**. This allows you to customise what gets displayed when no metadata exists for that Content Field. Thanks for suggesting Sam Pluemacher!
- Added seperate content fields for Markers with Marker Type. Thanks for suggesting Sam Pluemacher!
- Added Stabilisation Content Fields. Thanks for suggesting Matthieu Laclau!

---

### 1.0.4 (32)

**🎉 Released:**
- 19th January 2024

🔨 **Improvements:**
- If you're working inside a Compound Clip (as opposed to a Project), you can now apply Metaburner within that Compound Clip, and drag the Compound Clip from the Final Cut Pro Browser to the Metaburner Drop Zone. Thanks for suggesting Sam Pluemacher!

---

### 1.0.3 (31)

**🎉 Released:**
- 18th January 2024

🔨 **Improvements:**
- Added a `NSUpdateSecurityPolicy` to allow FxFactory to more seamlessly handle automatic unattended updates.

🐞 **Bug Fixes:**
- Fixed a regression which could cause Metaburner to silently crash when processing a clip with Captions or Live Drawings. Thanks for reporting Sam Pluemacher!
- Fixed a bug where Metaburner could be stuck on "Analyzing Project" infinitely. Thanks for reporting Sam Pluemacher!

---

### 1.0.2 (30)

**🎉 Released:**
- 18th January 2024

🔨 **Improvements:**
- Moved **Filter by Video/Audio Role** from Global Settings to individual Text Layers. These role filters now take into account all lanes. Thanks for suggesting Knut Hake & Sam Pluemacher!
- Added Content Field for **Audio Roles & Subroles**.
- Hooked up Above & Below Primary Storyline Content Sources.
- Added **Spatial Conform** Content Field.
- The status text now animates when analysing. Thanks [Daniel Saidi](https://github.com/danielsaidi)!
- If the current clip is an `clip` we now "pass through" the clip metadata to the **Primary Storyline - Inside Container** Content Sources for convenience. Thanks for suggesting Matthieu Laclau!


🐞 **Bug Fixes:**
- Fixed a regression which broke the Markers & Keywords Content Fields in some cases. Thanks for reporting Sam Pluemacher!

---

### 1.0.1 (29)

**🎉 Released:**
- 13th January 2024

🐞 **Bug Fixes:**
- Fixed a bug when using the **Marker + Notes** Content Field where markers would not be visible if they contained no note. Thanks for reporting Sam Pluemacher!
- Fixed a bug when using the **Marker + Notes** Content Field where the text layer would incorrectly end with a comma.
- Fixed bugs in **Scale**, **Position**, **Rotation** and **Opacity** Content Fields, where we weren't taking into account the timeline start timecode. Thanks for reporting Sam Pluemacher!

---

### 1.0.0 (28)

**🎉 Released:**
- 11th January 2024

🔨 **Improvements:**
- If the current clip is an `asset-clip` we now "pass through" the clip metadata to the **Primary Storyline - Inside Container** Content Sources for convenience. Thanks for suggesting Robin Moran!
- If you used the **Import Project via FCPXML** button, there's now a **Reload Project** buttons within the **Controls** section to refresh that existing FCPXML. Thanks for suggesting Knut Hake & Sam Pluemacher!
- Added metadata fields for Keywords & Markers on the Primary Storyline.
- Added metadata fields for Video and Audio Roles on the Primary Storyline.
- Added a **Filter by Video Role** and **Filter by Audio Role** option under **Global Settings** to allow you to only show a specific role. Thanks for suggesting Knut Hake & Sam Pluemacher!

🐞 **Bug Fixes:**
- Fixed a bug where you couldn't import FCPXML's via the **Import Project via FCPXML** button if they contained a Library > Event.

---

### 1.0.0 (27)

**🎉 Released:**
- 9th January 2024

🔨 **Changes:**
- Actually removed the App Sandbox this time, so it works properly on FxFactory.
- This is the first public beta on FxFactory! Woohoo!

---

### 1.0.0 (26)

**🎉 Released:**
- 9th January 2024

🔨 **Changes:**
- Removed the App Sandbox so that it hopefully plays nicely with FxFactory.

---

### 1.0.0 (25)

**🎉 Released:**
- 8th January 2024

🔨 **Changes:**
- This release is destined for FxFactory. We will no longer be posting builds to Apple's TestFlight.
- We've added a watermark to the image when in Trial Mode. You will be able to purchase the full version on FxFactory soon.
- We've removed the **Install Motion Template** button, as this will now be handled by FxFactory.

🔨 **Improvements:**
- Added an **Empty** built-in preset.
- Added a **Load Empty Preset** button in the **Presets** section.
- **Primary Storyline - Position** has been implemented.
- We now cache our Processed Data to dramatically improve Final Cut Pro's performance on big and complex projects.
- We now only read the FCPXML Data if Lua is used on a Text Layer (for a slight speed improvement).

🐞 **Bug Fixes:**
- Fixed a bug where the first frame of a clip could display incorrect metadata.
- Fixed a bug where the first frame of a keyframe could display incorrect metadata.
- Fixed a bug in Primary Storyline Timecode Format metadata.
- Removed a rogue space in Effects Lists.

---

### 1.0.0 (24)

**🎉 Released:**
- 5th January 2024

🔨 **Improvements:**
- **Primary Storyline - Video Effects (Horizontal/Vertical)** has been implemented.
- **Primary Storyline - Audio Effects (Horizontal/Vertical)** has been implemented.
- The main Wrapper application now installs the latest Motion Template if sandbox access has already been granted.
- Our FCPXML processor (`FCPXMLKit`) has been updated and improved.
- Updated the default Motion Template.

---

### 1.0.0 (23)

**🎉 Released:**
- 4th January 2024

🔨 **Improvements:**
- **Primary Storyline - Rotation** now displays in degrees rather than percentages.

---

### 1.0.0 (22)

**🎉 Released:**
- 3rd January 2024

🔨 **Improvements:**
- Improved error messages when FCPXML processing fails.
- Updated the default Motion Template.
- **Primary Storyline - Rotation** has been implemented.
- **Primary Storyline - Opacity** now works on Multicam Clips.
- **Primary Storyline - Scale** now works on Multicam Clips.
- Our FCPXML processor (`FCPXMLKit`) has been updated and improved.

---

### 1.0.0 (21)

**🎉 Released:**
- 3rd January 2024

🔨 **Changes:**
- We've renamed **Metaburner Pro** to just **Metaburner** for eventual release on FxFactory.

---

### 1.0.0 (20)

**🎉 Released:**
- 3rd January 2024

🔨 **Improvements:**
- We now include the version and build number in log file filename.
- Implemented **Frame Rate** for most clip types on the Primary Storyline.

---

### 1.0.0 (19)

**🎉 Released:**
- 2nd January 2024

🔨 **Improvements:**
- Major under-the-hood changes and improvements. It will now be much easier and faster for us to add new metadata fields.
- Implemented **Frame Rate** for an `asset-clip` on the Primary Storyline. More clip types will be added in a future beta.
- We now workaround a [bug](https://github.com/CommandPost/FCPCafe/issues/314) in Final Cut Pro 10.7.1 and FCPXML v1.11.
- We now support a `clip` (as opposed to just `asset-clip`) within a `sync-clip`.

---

### 1.0.0 (18)

**🎉 Released:**
- 31st December 2023

🔨 **Improvements:**
- Added "Scale" metadata field for `AssetClip`'s on the Primary Storyline. More clip types will be supported in a future beta.
- Added "Opacity" metadata field for `AssetClip`'s on the Primary Storyline. More clip types will be supported in a future beta.
- Updated the "Complex Example" preset.

---

### 1.0.0 (17)

**🎉 Released:**
- 31st December 2023

🔨 **Improvements:**
- You can now drag the text layers position in the Viewer.
- The position maths has been tweaked, so now a text layer set to a `[0,0]` position will appear in the top-left corner regardless of the Text Alignment.
- Added a label above each Text Layer in the Inspector. This will automatically populate, however you can override it via the **Custom Label** parameter.
- The **Load Preset**, **Save Preset** and **Load Template** buttons are now working.
- Some **Primary Storyline - Inside Container - 1st Audio Clip** parameters are now hooked up for Synchronised Clips.

---

### 1.0.0 (16)

**🎉 Released:**
- 25th December 2023

🔨 **Improvements:**
- Various under-the-hood improvements.

---

### 1.0.0 (15)

**🎉 Released:**
- 25th December 2023

🔨 **Improvements:**
- We now have a single shared Lua virtual machine, which means you can pass global variables between different Metaburner Titles.
- Improved how we update the status in the Final Cut Pro Inspector. It should now update more reliably and faster.
- Updated credits in the main Wrapper application.
- Added a **Reveal Crash Logs** button in the **Controls** section of the Titles Inspector.
- Various under-the-hood improvements.
- Updated Motion Template.

---

### 1.0.0 (14)

**🎉 Released:**
- 24th December 2023

🔨 **Improvements:**
- Cleaned up Project Logic.
- Exposed `processedData` and `fcpxmlData` in Lua Environment.

🐞 **Bug Fix:**
- Fixed bug if text layer was disabled.

---

### 1.0.0 (13)

**🎉 Released:**
- 24th December 2023

🔨 **Improvements:**
- Added Filename Metadata for Inside Video Container.
- Added Basic Lua Support.

---

### 1.0.0 (12)

**🎉 Released:**
- 23rd December 2023

🔨 **Improvements:**
- Added **Primary Storyline - Inside Container - 1st Video Clip** and **Primary Storyline - Inside Container - 1st Audio Clip** Content Sources.
- Added **Filename** and **Note** Content Fields.
- Added **Project Note**.
- Updated Motion Template.

---

### 1.0.0 (11)

**🎉 Released:**
- 23rd December 2023

🔨 **Improvements:**
- Added full error message to tooltip.
- Improved error messaging.

---

### 1.0.0 (10)

**🎉 Released:**
- 21st December 2023

🔨 **Improvements:**
- Added a "Welcome" image when no FCPXML is loaded.
- Removed all alerts/popups when importing a FCPXML. It now just updates the text in the Inspector.
- Added "Import Project via FCPXML".
- Added **Background Padding** & **Background Offset**.
- Update Motion Template.

🐞 **Bug Fix:**
- We now ensure all text is over the top of the background.

---

### 1.0.0 (9)

**🎉 Released:**
- 20th December 2023

🔨 **Improvements:**
- Added internal tests.

---

### 1.0.0 (8)

**🎉 Released:**
- 20th December 2023

🐞 **Bug Fix:**
- Fixed Opacity Bugs.

---

### 1.0.0 (7)

**🎉 Released:**
- 20th December 2023

🔨 **Improvements:**
- Added Project Loaded Status.
- Attempted to solve some UI glitches with dragging and dropping. Not sure I made it any better.
- Tweaked error handling.
- Updated Motion Template.

---

### 1.0.0 (6)

**🎉 Released:**
- 19th December 2023

🔨 **Improvements:**
- Disabled **Lane 1**, **Lane 2**, etc. from menu for now.
- We now write "-" instead of "TBC".
- We now write log files to disk.
- We now display `-` when metadata fails.
- Updated Motion Template.

🐞 **Bug Fixes:**
- Fixed **Project > Start Timecode** typo.
- Added missing Text Layer.

---

### 1.0.0 (5)

**🎉 Released:**
- 19th December 2023

🔨 **Improvements:**
- Under-the-hood improvements to our FCPXML Processing Engine.
- Added a "Cancel" button to the Progress Alert incase it stalls for some reason.
- Hooked up **Project Duration**, **Timecode Format** and **Start Timecode**.
- Added **Primary Storyline > HH:MM:SS:FF**.

🐞 **Bug Fix:**
- Fixed bug in Right Alignment.

---

### 1.0.0 (4)

**🎉 Released:**
- 18th December 2023

🔨 **Improvements:**
- Tweaked parameter defaults.
- Started building the FCPXML Processing Engine.
- Updated Motion Template.

---

### 1.0.0 (3)

**🎉 Released:**
- 18th December 2023

🔨 **Improvements:**
- Added **Alignment**, **Background Colour**, **Background Opacity** and **All Caps**.
- We now use an XY parameter for position.
- Improved how we draw text.
- Changed Default Font & Size.
- Changed the internal ID numbering to avoid a weird Final Cut Pro bug with ID `300`.
- Added ability to install the Motion Template from the Wrapper Application.
- Updated Motion Template.

---

### 1.0.0 (2)

**🎉 Released:**
- 17th December 2023

🔨 **Improvements:**
- The FCPXML drop zone is now working.
- Added placeholder **Preset** buttons.
- Updated the Motion Template.

---

### 1.0.0 (1)

**🎉 Released:**
- 16th December 2023

This is the first release of Metaburner Beta on TestFlight. Woohoo!
