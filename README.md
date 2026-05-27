> ⚠️ **DEPRECATION WARNING: PROJECT NO LONGER MAINTAINED**
> 
> I have moved on to using the **Godot** engine and will no longer be updating this repository. 
> 
> **Keijiro Takahashi-san** (the creator of the original glitch effect) has since released his own official URP version of these glitch effects. If this repository breaks, please check out his official repository instead: **[KinoGlitchURP](https://github.com/keijiro/KinoGlitchURP)**.

> **Note:** If you are coming from the older URP Glitch video, you need to download the older `2021.3.8f1+` package from the **Releases** section.
> **Note:** If you are coming from the older URP Glitch video, you need to download the older `2021.3.8f1+` package from the **Releases** section.

# URP Glitch Effect
**URP Glitch** is a glitch effect for the Universal Render Pipeline (URP), originally based on [mao-test-h's project](https://github.com/mao-test-h/URPGlitch), which in turn was inspired by [keijiro's HDRP Glitch effect](https://github.com/keijiro/KinoGlitch). This effect has been tested on Unity versions `6000.0.0f1` and `6000.0.23f1`.

[digital.webm](https://github.com/user-attachments/assets/18246342-0e59-4b7b-8d63-27207f5277b7)
[analog.webm](https://github.com/user-attachments/assets/d5fa80ed-0953-4f5d-8854-a1351919c928)

Tutorial - https://youtu.be/JFDuHaWDUvo
---

## Installation Instructions

### Option 1: Install via Package Manager
1. Open **Package Manager** in Unity (Window → Package Manager).
2. Click the **+** icon in the top-left corner.
3. Select **Install package from Git URL...**
4. Paste the following URL and click **Install**:
   ```
   https://github.com/saimarei/URPGlitch.git
   ```

### Option 2: Modify `manifest.json`
1. Navigate to your project folder in the file explorer.
2. Open the `Packages` folder and locate the `manifest.json` file.
3. Add this line in the `"dependencies"` section:
   ```json
   "com.subbu.urp-glitch": "https://github.com/saimarei/URPGlitch.git",
   ```
   You can place it:
   - **At the beginning of `"dependencies"`**:
     ```json
     {
       "dependencies": {
         "com.subbu.urp-glitch": "https://github.com/saimarei/URPGlitch.git",
         "com.unity.collab-proxy": "2.5.2",
         ...
       }
     }
     ```
   - **After any other dependency** (with a comma after the previous entry):
     ```json
     {
       "dependencies": {
         "com.unity.collab-proxy": "2.5.2",
         "com.subbu.urp-glitch": "https://github.com/saimarei/URPGlitch.git",
         ...
       }
     }
     ```
   - **At the end of the dependencies list** (without a comma afterward):
     ```json
     {
       "dependencies": {
         ...
         "com.unity.modules.xr": "1.0.0",
         "com.subbu.urp-glitch": "https://github.com/saimarei/URPGlitch.git"
       }
     }
     ```

### Option 3: Install from Local Package
1. Download the package from the **Releases** section of the GitHub page.
2. In Unity, right-click and select **Import Package → Custom Package**.
3. Choose the downloaded package file. Beginners may want to import all files.

---

## Setup Instructions

1. **Add Glitch Render Feature**:
   - Locate your URP renderer asset in Unity.
   - Click **Add Render Feature**.
   - Choose the **Analog/Digital Glitch Feature**.
   - Set the **Shader** field by selecting an appropriate shader (click the eye icon to reveal hidden shaders).
   - In the **Render Pass** dropdown, choose **After Rendering Transparents**.

2. **Configure Global Volume**:
   - In the Scene Hierarchy, create a volume: **Right-click → Volume → Global Volume**.
   - Select the volume and create a **New Profile**.
   - Add an override and select the **Analog/Glitch Volume**.
   - Ensure **Post-Processing** is enabled on the main camera to apply the effect.

---

## Sample Scene Setup

1. Download and open the **Sample Scene**.
2. Find the URP asset file in the project.
3. In the **Renderer List**, click the **+** icon.
4. Assign the **2D Sample Renderer** or **Sample Universal Renderer**.
5. The effect should now be active. 

> The settings object in the sample scene includes a script that demonstrates how to use buttons to control the effects programmatically.

---

## License

This project is released under the same license as [keijiro/KinoGlitch](https://github.com/keijiro/KinoGlitch).
