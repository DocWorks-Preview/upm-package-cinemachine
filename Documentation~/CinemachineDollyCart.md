# Cinemachine Dolly Cart

**Cinemachine Dolly Cart** is a component that constrains the transform of its GameObject to a **Cinemachine Path** or **Cinemachine Smooth Path**. Use it to animate a GameObject along a path, or as a **Follow** target for Virtual Cameras.

## Properties:

| **Property:** || **Function:** |
|:---|:---|:---
| **Path** || The path to follow. |
| **Update Method** || When to move the cart when velocity is non-zero. Use **Update** for normal `MonoBehaviour` updating, **Fixed Update** for updates in sync with the Physics module, `FixedUpdate()`. |
| **Position Units** || The unit of measure for **Position**.  |
| | _Path Units_ | Use waypoints along the path. The value 0 represents the first waypoint on the path, 1 is the second waypoint, and so on. |
| | _Distance_ | Use distance along the path. The path is sampled according to the Resolution property of the path. Cinemachine creates a distance lookup table, which it stores in an internal cache. |
| | _Normalized_ | Use the beginning and end of the path. The value 0 represents the beginning of the path, 1 is the end of the path. |
| **Speed** || Move the cart with this speed. The value is interpreted according to **Position Units**. |
| **Position** || The position along the path to place the cart. This can be animated directly or, if the speed is non-zero, will be updated automatically. The value is interpreted according to **Position Units**. |
