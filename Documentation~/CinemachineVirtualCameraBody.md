# Body properties

Use the Body properties to specify the algorithm that moves the Virtual Camera in the Scene. To rotate the camera, set the [Aim properties](CinemachineVirtualCameraAim.html).

![**Body** properties, with the **Transposer** algorithm (red)](Images/CinemachineBody_5c6c12dcdd83130d44febdd0.png)

Cinemachine includes these algorithms for moving a Virtual Camera:

* [**Transposer**](CinemachineBodyTransposer.html): moves in a fixed relationship to the **Follow** target.
* [**Do Nothing**](CinemachineBodyDoNothing.html): does not move the Virtual Camera.
* [**Framing Transposer**](CinemachineBodyFramingTransposer.html): moves in a fixed screen-space relationship to the **Follow** target.
* [**Orbital Transposer**](CinemachineBodyOrbitalTransposer.html): moves in a variable relationship to the **Follow** target, optionally accepting player input.
* [**Tracked Dolly**](CinemachineBodyTrackedDolly.html): moves along a predefined path.
* [**Hard Lock to Target**](CinemachineBodyHardLockTarget.html): uses the same position at the **Follow** target.
