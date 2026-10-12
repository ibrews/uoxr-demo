# UOXR Preview

Try the Ultimate OpenXR Template by **Alex Coulombe Presents** in your Android
headset. This repository distributes the playable demo, screenshots and test
notes. The Unreal project and template source remain private.

**[Download the preview APK](https://github.com/ibrews/uoxr-demo/releases/tag/preview-2026-10-12)**
· [Project page and simulator videos](https://alexcoulombepresents.com/lab/ultimate-openxr-template)

![The tutorial gallery](media/gallery-preview.jpg)

## Quickstart

1. Download `UOXR-Preview-Android-build3.apk` from the release assets.
2. Enable your headset's developer mode and install with its sideloading tool.
   If you use Android platform tools: `adb install -r UOXR-Preview-Android-build3.apk`.
3. Launch **UOXR Template** from your headset's applications/unknown-sources list.
   The separate application ID, `com.alexcoulombepresents.uoxrdemo`, preserves
   existing UOXR Template installations.
4. Open settings with **B/Y** on a controller, or hold **both thumb–index pinches
   for one second**, then release. Aim a ray and pinch once to select a button.
   Keyboard: **Tab**. Gamepad: **Start**.

This is a development-signed evaluation preview for Android OpenXR headsets, using
arm64, Vulkan and ASTC, with Android 12L/API 32 or newer required for build 3.
It is not a phone app or a store-certified release. An APK
cannot run on PCVR or Apple Vision Pro. Compatibility on untested headsets remains
unknown; include your model and OS version when reporting a problem.

## Things to Try

1. Walk through the **Tutorial** and complete its six guided exercises.
2. Open settings and try **Teleport**, **Walk**, **Fly**, snap turning and the
   **Light/Strong comfort tunnel**. The tunnel appears during continuous movement
   and clears at rest or while the menu is open.
3. Choose **Power puzzle** at the bottom of settings. Put the teal power cell in
   its socket, pass through the door and power the machine with the amber cell.
4. Visit **Grab lab** and **Door lab** from the same menu. Lift a coral reset cube
   to repeat an exercise. Selecting a room restarts it; comfort settings persist.
5. Swap between tracked hands and controllers. Core uses joint-based hand visuals;
   optional runtime mesh-hand plugins are not included in this preview.

![The Power Workshop](media/workshop-preview.jpg)

## Quality and validation

The app chooses a starting quality profile automatically: Quest 3/3S 100%, Quest
Pro 90%, Quest 2/PICO 85%, and a generic Android XR fallback 80% eye render scale.
All start with 4x MSAA. Shadow budgets vary by profile. These are starting presets,
not continuous thermal/FPS adaptation or frame-rate guarantees. ASW is off by
default; earlier experimental headset results do not certify this APK.

Before packaging, the source passed tutorial 17, Workshop 18, hand-menu 18 and
profile-selection 12 checks. xrsim with Meta XR Simulator 207 also drove hand
pinches through all four map destinations. Stereo captures exercised 80%/2x MSAA,
85%/4x and 100%/4x quality budgets. Simulator checks establish rendering and input
behavior on the host, not standalone headset performance. Exact-APK checks and
known limitations are listed in each release.

Build 3's exact APK was installed by SHA-256 and rendered the Tutorial in PICO
Emulator 0.13; its installed bytes were pulled and matched independently. Fresh
native simulator tests passed controller/hand switching 7/7, controller models 7/7
and hand-menu 18/18. Controller grips completed the labs and the full power puzzle.
Physical fit, stereo comfort and sustained headset performance remain pending.
**VIVE Focus3/API29 is not supported by this API32 APK.**

## Simulator walkthrough

[![Watch the 59-second simulator tour](media/simulator-walkthrough-landscape.jpg)](https://github.com/ibrews/uoxr-demo/releases/download/preview-2026-10-12/UOXR-Simulator-Walkthrough-landscape-2026-10-12.mp4)

Hands, controller models, comfort menus, flight, teleport, grabbing, doors and a
complete power puzzle, recorded in Meta XR Simulator and xrsim. The final shot
shows the packaged APK in PICO Emulator. Simulator windows and labels stay visible.
The source remains private.

- [Watch/download landscape](https://github.com/ibrews/uoxr-demo/releases/download/preview-2026-10-12/UOXR-Simulator-Walkthrough-landscape-2026-10-12.mp4)
- [Watch/download portrait](https://github.com/ibrews/uoxr-demo/releases/download/preview-2026-10-12/UOXR-Simulator-Walkthrough-portrait-2026-10-12.mp4)
- [Captions and suggested social caption](https://github.com/ibrews/uoxr-demo/releases/tag/preview-2026-10-12) are included in the release.

Model previews show Quest/Focus/PICO appearances in Meta runtime, rather than
claiming physical tests of those devices. The video has original music and
burned-in captions; gameplay audio and haptic feel were not captured.

## Feedback

Open an issue with your headset, OS, preview version, reproduction steps and any
screenshots. For a performance report, include whether the app was warm and which
room you visited. Please do not include account credentials or private logs.

© 2026 Alex Coulombe Presents. Downloading the demo does not grant access to or a
license for the private template source.
