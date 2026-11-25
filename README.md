# AirPods Motion

Control Ableton Live with head movements from your AirPods Pro. Assign yaw, pitch, and roll to up to eight parameters each, with adjustable ranges and relative modulation.

[Download](https://github.com/echonullx8/AirPods-Motion/releases/latest) · [Report an issue](https://github.com/echonullx8/AirPods-Motion/issues)

## Requirements

- Apple Silicon Mac with macOS 14 or later
- Ableton Live with Max for Live
- AirPods Pro connected to your Mac and worn during use

## Install

1. Download and extract **AirPodsMotion-Installer.zip**.
2. Open **Install AirPods Motion.app** and click **Install**.
3. In Live, open **User Library → Presets → Audio Effects → Max Audio Effect** and drag **AirPods Motion** onto a track.

The receiver is installed in **Applications**. If you use a custom User Library, choose **Change Library Location…** in the installer.

On first use, allow the receiver to access Motion & Fitness. macOS may also ask you to approve opening the downloaded app.

## Start controlling

1. Enable Live’s audio engine, put on your AirPods Pro, and click **Start**.
2. Hold a comfortable neutral pose and click **Center**.
3. Select **Yaw**, **Pitch**, or **Roll**.
4. Click **Map**, then click the parameter you want to control in Live.
5. Adjust **Range**, **Min**, and **Max** to set the response.

Click **Stop** when finished. The receiver opens automatically when you click Start.

## Controls

| Control | What it does |
| --- | --- |
| Center | Treat your current head pose as zero. |
| Yaw | Turn left or right. Left is negative; right is positive. |
| Pitch | Look up or down. |
| Roll | Tilt toward either shoulder. |
| Angle | Show the current angle in degrees. |
| Range ± | Set the movement needed to reach either endpoint. A value of 30 covers −30° to +30°. |
| Freeze | Hold an axis at its current value. Click again to resume tracking. |
| ABS | Control the target parameter directly. |
| REL | Modulate around the target parameter’s own setting, which you can still adjust. |
| Min / Max | Set the output limits. Swap them to reverse the response. |
| Out | Show the control value: target percentage in ABS, modulation offset in REL. |
| × | Remove the mapping. |

Each axis has eight mapping slots. Click the selected axis again, or the collapse arrow, to close the mapping area.

Range, Center, and Freeze are available for mapping. Use Live’s MIDI or Key Map mode to assign a controller or key to Center or Freeze.

For recentering, use **Center** or a mapped controller/key. The receiver’s headphone-press option is currently unreliable.

## Help

**Angles are not moving:** Check that your AirPods are connected to this Mac and being worn. Check **System Settings → Privacy & Security → Motion & Fitness**, then click Stop and Start.

**Angles move, but the instrument does not respond:** Enable Live’s audio engine, check Freeze and the output limits, and map the target again.

**The receiver cannot be found:** Run the installer again and check for **AirPods Motion Bridge.app** in Applications.

Use one active AirPods Motion device at a time.

For help, [open an issue](https://github.com/echonullx8/AirPods-Motion/issues) with your macOS version, Live version, AirPods model, and the status shown on the device.
