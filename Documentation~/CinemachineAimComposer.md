# Composer

This Virtual Camera **Aim** algorithm rotates the camera to face the **Look At** target. It also applies offsets, damping, and composition rules. Examples of targets for aiming: the upper spine or head bone of a character, vehicles, or dummy objects which are controlled or animated programmatically.

## Properties:

| **Property:** | **Function:** |
|:---|:---|
| **Tracked Object Offset** | Offset from the center of the Look At target, in target-local space. Fine-tune the tracking target position when the desired area is not the tracked object’s center. |
| **Lookahead Time** | Adjust the offset based on the motion of the Look At target. The algorithm estimates the point that the target will be this many seconds into the future. This feature is sensitive to noisy animation. It can amplify the noise, resulting in undesirable camera jitter. If the camera jitters unacceptably when the target is in motion, turn down this property or animate the target more smoothly. |
| **Lookahead Smoothing** | Controls the smoothness of the lookahead algorithm. Larger values smooth out jittery predictions and increase prediction lag. |
| **Lookahead Ignore Y** | Toggle to ignore movement along the Y axis for lookahead calculations. |
| **Horizontal Damping** | How responsively the camera follows the target in the screen-horizontal direction. Use small numbers for more responsive, rapid rotation of the camera to keep the target in the dead zone. Use larger numbers for a more heavy, slowly-responding camera.  |
| **Vertical Damping** | How responsively the camera follows the target in the screen-vertical direction. Use different vertical and horizontal settings to give a wide range of camera behaviors. |
| **Screen X** | Horizontal screen position for the center of the dead zone. The camera rotates so that the target appears here. |
| **Screen Y** | Vertical screen position for target, The camera rotates so that the target appears here. |
| **Dead Zone Width** | The width of the screen region within which the camera ignores any movement of the target.  If the target is positioned anywhere within this region, the Virtual Camera does not update its rotation. This is useful for ignoring minor target movement.  |
| **Dead Zone Height** | The height of the screen region within which the camera ignores any movement of the target.  If the target is positioned anywhere within this region, the Virtual Camera does not update its rotation. This is useful for ignoring minor target movement. |
| **Soft Zone Width** | The width of the soft zone.  If the target appears in this region of the screen, the camera will rotate to push it back out to the dead zone, in the time specified by the Horizontal Damping setting. |
| **Soft Zone Height** | The height of the soft zone.  If the target appears in this region of the screen, the camera will rotate to push it back out to the dead zone, in the time specified by the Vertical Damping setting. |
| **Bias X** | Positions the soft zone horizontally, relative to the dead zone. |
| **Bias Y** | Positions the soft zone vertically, relative to the dead zone. |

