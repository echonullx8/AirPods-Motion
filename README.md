# AirPods Motion

Control Ableton Live parameters with head movements from your AirPods Pro. Map yaw, pitch, and roll to up to eight targets per axis.

[Download the latest release](../../releases/latest) · [Report an issue](../../issues)

## Requirements

- Apple Silicon Mac running macOS 14 or later.
- Ableton Live with Max for Live support.
- AirPods Pro connected to the Mac and worn during use.

## Installation

1. Download `AirPodsMotion-Installer.zip` from Releases and extract it.
2. Open `Install AirPods Motion.app` and click **Install**.
3. The installer places the receiver in the system **Applications** folder and the device in your default **User Library → Presets → Audio Effects → Max Audio Effect**.
4. For a custom User Library, click **Change Library Location…**. You can find your library location in Live’s **Settings → Library**.
5. In Live’s browser, find **AirPods Motion** in your User Library and drag it onto a track.

Existing files are backed up before replacement. Backups are stored in your personal `Library/Application Support/AirPods Motion/Backups` folder.

This release uses local signing. macOS may display a developer verification message on first launch. Confirm that the download came from this repository’s release page. Allow Motion access for the receiver when macOS requests it.

## Quick start

1. Enable Live’s audio engine and put on your AirPods Pro.
2. Click **Start**. The receiver launches automatically.
3. Move your head and check the **Angle** readings and animated head.
4. Hold a comfortable neutral pose and click **Center** to set it as zero.
5. Click **Yaw**, **Pitch**, or **Roll** to open that axis’s mapping list.
6. Click **Map** on a row, then click the Live parameter you want to control.

Use the collapse button in the mapping area to close the list. Turning off the selected axis button also collapses it; selecting another axis switches the list.

## Headphone press to Center

The receiver includes an experimental headphone-press option. It currently does not reliably receive AirPods short-press events and should not be relied on for performance. Use the device's Center button or map Center to a MIDI controller or computer key instead.

## Controls

| Control | Function |
| --- | --- |
| Start | Launch the receiver and start motion input. |
| Stop | Stop input and release parameter control. |
| Center | Set the current head pose as zero. |
| Yaw | Turn your head left or right. Left is negative; right is positive. |
| Pitch | Tilt your head up or down. |
| Roll | Tilt your head toward either shoulder. |
| Angle | Current control angle in degrees. |
| Motion bar | Angle relative to zero, marked by the center line. |
| Range and ± | Motion required to reach each endpoint. A range of 30 covers −30° to +30°. |
| Freeze / Frozen | Hold one axis at its current angle. Click again to resume tracking. All mappings on that axis hold together; other axes keep responding. |
| Map | Select a target parameter. |
| ABS | Directly control the target parameter. |
| REL | Add modulation to the parameter’s existing base value. You can still adjust its original knob. |
| Min / Max | Set each mapping’s output limits. Reverse the limits to invert its direction. |
| Out | Control output: normalized target value in ABS, modulation offset in REL. This is not the target knob’s final displayed value. |
| × | Clear a mapping. |
| Status | Connection and receiver status in the bottom panel. |

All three Range parameters support Live automation and mapping from other modulation devices. The device also allows mapping to its own mappable parameters.

Freeze holds the axis input. In REL mode, the target parameter’s base value remains adjustable.

## Troubleshooting

### Angle readings do not change

- Check that your AirPods Pro are connected to this Mac and being worn.
- Check the receiver’s permission under **System Settings → Privacy & Security → Motion & Fitness**.
- Click **Stop**, then **Start**, and read the status message.
- Keep a single active receiver instance. Multiple devices or standalone Max receiver patches listening on UDP port 9000 can compete for motion data.

### Angle changes, but the mapped parameter does not

- Enable Live’s audio engine.
- Click **Map** again and select the target parameter.
- Check the axis’s Freeze state and the mapping’s Min / Max limits.

### The receiver cannot be found

Run the installer again and check that **AirPods Motion Bridge.app** is in the system **Applications** folder.

## Files and feedback

The `.amxd` includes its JavaScript dependencies. The installer installs the receiver App separately.

This repository distributes the installer and documentation. When reporting an issue, include your macOS version, Live version, AirPods model, and status message. Screenshots are useful for interface issues.
