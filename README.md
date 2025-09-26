# Magicbot-Gen1 Description (URDF & MJCF)

## Overview

This package includes a universal humanoid robot description (URDF & MJCF) for the [Magicbot-Gen1](https://www.magiclab.top/human), developed by Magiclab Robotics.

<table>
  <tr>
    <td><img src="doc/rviz.png" width="400"/></td>
    <td><img src="doc/mujoco.png" width="400"/></td>
  </tr>
</table>

Magicbot-Gen1 Humanoid have 30 joints:

```text
root [⚓] => /pelvis/
    left_hip_roll_joint [⚙+X] => /left_hip_roll_link/
        left_hip_yaw_joint [⚙+Z] => /left_hip_yaw_link/
            left_hip_pitch_joint [⚙+Y] => /left_hip_pitch_link/
                left_knee_pitch_joint [⚙+Y] => /left_knee_pitch_link/
                    left_ankle_pitch_joint [⚙+Y] => /left_ankle_pitch_link/
                        left_ankle_roll_joint [⚙+X] => /left_ankle_roll_link/
    right_hip_roll_joint [⚙+X] => /right_hip_roll_link/
        right_hip_yaw_joint [⚙+Z] => /right_hip_yaw_link/
            right_hip_pitch_joint [⚙+Y] => /right_hip_pitch_link/
                right_knee_pitch_joint [⚙+Y] => /right_knee_pitch_link/
                    right_ankle_pitch_joint [⚙+Y] => /right_ankle_pitch_link/
                        right_ankle_roll_joint [⚙+X] => /right_ankle_roll_link/
    waist_roll_joint [⚙+X] => /waist_roll_link/
        waist_yaw_joint [⚙+Z] => /waist_yaw_link/
            head_yaw_joint [⚙+Z] => /head_yaw_link/
                head_pitch_joint [⚙+Y] => /head_pitch_link/
                    left_shoulder_pitch_joint [⚙+Y] => /left_shoulder_pitch_link/
                        left_shoulder_roll_joint [⚙+X] => /left_shoulder_roll_link/
                            left_shoulder_yaw_joint [⚙+Z] => /left_shoulder_yaw_link/
                                left_elbow_roll_joint [⚙+X] => /left_elbow_roll_link/
                                    left_wrist_yaw_joint [⚙+Z] => /left_wrist_yaw_link/
                                        left_wrist_roll_joint [⚙+X] => /left_wrist_roll_link/
                                            left_wrist_pitch_joint [⚙+Y] => /left_wrist_pitch_link/
                    right_shoulder_pitch_joint [⚙+Y] => /right_shoulder_pitch_link/
                        right_shoulder_roll_joint [⚙+X] => /right_shoulder_roll_link/
                            right_shoulder_yaw_joint [⚙+Z] => /right_shoulder_yaw_link/
                                right_elbow_roll_joint [⚙+X] => /right_elbow_roll_link/
                                    right_wrist_yaw_joint [⚙+Z] => /right_wrist_yaw_link/
                                        right_wrist_roll_joint [⚙+X] => /right_wrist_roll_link/
                                            right_wrist_pitch_joint [⚙+Y] => /right_wrist_pitch_link/
```
## Usages

### RViz
```bash
sudo apt install ros-humble-joint-state-publisher-gui
cd magicbot-gen1_description
colcon build
source install/setup.bash
ros2 launch magicbot-gen1_description view.launch.py 
```

### MuJoCo
```bash
pip install mujoco
cd magicbot-gen1_description
python3 -m mujoco.viewer --mjcf=mjcf/MAGICBOT.xml
```
