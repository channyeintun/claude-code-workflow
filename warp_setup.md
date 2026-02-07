# 🌀 Warp Terminal Setup

To get the same "cool" glassmorphism look in Warp:

## 1. Apply the Theme
1. Open Warp and go to `Settings > Appearance`.
2. Click on the **Current theme** box.
3. Select **CatppuccinMocha** (which I've just installed for you).

## 2. Enable Transparency & Blur
> [!IMPORTANT]
> Transparency in Warp is controlled by a slider in the UI, not by the theme file itself.
1. In `Settings > Appearance`, scroll down to the **Themes** section.
2. Find the **Window Opacity** slider. Move it to about **85%**.
3. Once opacity is below 100%, the **Blur radius** slider will activate. Set it to around **20**.

## 3. Troubleshooting (If it's not transparent)
- **Exit Full Screen**: Warp has a known bug where transparency doesn't work in native macOS full-screen mode. Try taking it out of full screen.
- **Restart Warp**: Always restart Warp after adding a new theme file or changing opacity for the first time.
- **MacOS Theme**: Ensure your macOS is set to "Dark" or "Auto" in System Settings, as this can sometimes affect how translucent windows render.
- **Graphics Backend**: If the slider does nothing, try changing the graphics backend in `Settings > Features > System` to `Vulkan` or `OpenGL` and restart.

## 4. Font Setup
1. In `Settings > Appearance`, find the **Text** section.
2. Set your font to **JetBrainsMono Nerd Font** (or your preferred Nerd Font).


---
*Your terminal setup is now synchronized across Ghostty and Warp!*
