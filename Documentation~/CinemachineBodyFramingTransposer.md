# Framing Transposer

This Virtual Camera **Body** algorithm moves the camera in a fixed screen-space relationship to the **Follow** target. You can also specify offsets, damping, and composition rules. **Framing Transposer** only changes the camera’s position in space. It does not re-orient or otherwise aim the camera.

**Framing Transposer** is designed for 2D and orthographic cameras. But it works equally well with perspective cameras and 3D environments.

This algorithm first moves the camera along the camera Z axis until the **Follow** target is at the desired distance from the camera’s X-Y plane. It then moves the camera in its X-Y plane until the **Follow** target is at the desired point on the camera’s screen.

**Note**: To use **Framing Transposer**, the **Look At** property must be empty.

If the **Follow** target is a [Target Group](CinemachineTargetGroup.html), then additional properties are available to frame the entire group.

## Properties

| **Property:** || **Function:** |
|:---|:---|:---|
| **Lookahead Time** || Adjusts the offset of the Virtual Camera from the Follow target based on the motion of the target. Cinemachine estimates the point where the target will be this many seconds into the future. This feature is sensitive to noisy animation and can amplify the noise, resulting in undesirable camera jitter. If the camera jitters unacceptably when the target is in motion, turn down this property, or animate the target more smoothly. |
| **Lookahead Smoothing** || The smoothness of the lookahead algorithm. Larger values smooth out jittery predictions and increase prediction lag. |
| **Lookahead Ignore Y** || If checked, ignore movement along the Y axis for lookahead calculations. |
| **X Damping** || How responsively the camera tries to maintain the offset in the x-axis. Small numbers make the camera more responsive. Larger numbers make the camera respond more slowly.  Using different settings per axis can yield a wide range of camera behaviors. |
| **Y Damping** || How responsively the camera tries to maintain the offset in the y-axis. Small numbers make the camera more responsive. Larger numbers make the camera respond more slowly.   |
| **Z Damping** || How responsively the camera tries to maintain the offset in the z-axis. Small numbers make the camera more responsive. Larger numbers make the camera respond more slowly.   |
| **Screen X** || Horizontal screen position for target. The camera moves to position the tracked object here. |
| **Screen Y** || Vertical screen position for target, The camera moves to position the tracked object here. |
| **Camera Distance** || The distance to maintain along the camera axis from the Follow target. |
| **Dead Zone Width** || Do not move the camera horizontally when the target is within this range of the position. |
| **Dead Zone Height** || Do not move the camera vertically if the target is within this range of the position. |
| **Dead Zone Depth** || Do not move the camera along its z-axis if the Follow target is within this distance of the specified camera distance. |
| **Unlimited Soft Zone** || If checked, then the soft zone is unlimited in size. |
| **Soft Zone Width** || When the target is in this range, move the camera horizontally to frame the target in the dead zone. The Damping properties affect the rate of the camera movement.  |
| **Soft Zone Height** || When the target is in this range, move the camera vertically to frame the target in the dead zone. The Damping properties affect the rate of the camera movement.  |
| **Bias X** || Moves the target position horizontally away from the center of the soft zone. |
| **Bias Y** || Moves the target position vertically away from the center of the soft zone. |
| **Group Framing Mode** || Available when Follow specifies a [Target Group](CinemachineTargetGroup.html). Specifies the screen dimensions to consider when framing.  |
| | _Horizontal_ | Consider only the horizontal dimension. Ignore vertical framing. |
| | _Vertical_ | Consider only the vertical dimension. Ignore horizontal framing. |
| | _Horizontal And Vertical_ | Use the larger of the horizontal and vertical dimensions to get the best fit. |
| | _None_ | Don’t do any framing adjustment. |
| **Adjustment Mode** || How to adjust the camera to get the desired framing. You can zoom, dolly in or out, or do both. Available when Follow specifies a Target Group.  |
| | _Zoom Only_ | Don’t move the camera, only adjust the FOV. |
| | _Dolly Only_ | Move the camera, don’t change the FOV. |
| | _Dolly Then Zoom_ | Move the camera as much as permitted by the ranges, then adjust the FOV if necessary to make the shot. |
| **Group Framing Size** || The bounding box that the targets should occupy. Use 1 to fill the whole screen, 0.5 to fill half the screen, and so on. Available when Follow specifies a Target Group.  |
| **Max Dolly In** || The maximum distance toward the target to move the camera. Available when Follow specifies a Target Group.  |
| **Max Dolly Out** || The maximum distance away from the target to move the camera. Available when Follow specifies a Target Group.  |
| **Minimum Distance** || Set this to limit how close to the target the camera can get. Available when Follow specifies a Target Group.  |
| **Maximum Distance** || Set this to limit how far from the target the camera can get. Available when Follow specifies a Target Group.  |
| **Minimum FOV** || If adjusting FOV, do not set the FOV lower than this. Available when Follow specifies a Target Group.  |
| **Maximum FOV** || If adjusting FOV, do not set the FOV higher than this. Available when Follow specifies a Target Group.  |
| **Minimum Ortho Size** || If adjusting Orthographic Size, do not set it lower than this. Available when Follow specifies a Target Group.  |
| **Maximum Ortho Size** || If adjusting Orthographic Size, do not set it higher than this. Available when Follow specifies a Target Group. |



