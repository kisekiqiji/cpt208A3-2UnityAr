# AR Object Viewer Tool
This AR scene is built with Unity XR Foundation, following a modular hierarchical structure to support cross-platform AR interaction.

---

## Development Environment
- Unity 2020+ / 2021+
- AR Foundation / AR Core (Android supported)
- 3D model assets + custom UI icon resources

---

## Usage
1. Install the application on your Android device and grant camera permission.
2. Download Google Play Services for AR.

---

## Project Structure
- `AR Session / AR Session Origin`: Core AR components
- `Object Menu`: UI menu for model switching
- `Scroll View > Viewport > Content`: Parent container for UI buttons
- `Scripts`: AR tracking, object spawning, and button control logic

---

## Vibe Coding
The root object XR Origin (AR Rig) serves as the core tracking system, containing a Camera Offset transform node that adjusts the camera's physical position relative to the AR tracking origin. Within the offset, the Main Camera handles AR visual rendering and pose tracking, while the Screen Space Ray Interactor enables touch-based ray interaction for placing virtual objects in the real world. The Object Spawner component manages the instantiation and placement of AR content, triggered by user input. The AR Session object controls the AR lifecycle, including session initialization, tracking state management, and plane detection. Additional components such as Directional Light and UI provide basic scene lighting and user interface support, ensuring stable visual feedback and interactive experience.
