# Release Notes

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
