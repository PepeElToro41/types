The CFrame property (not to be confused with [BasePart.CFrame](https://developer.roblox.com/api-reference/property/BasePart/CFrame)) determines the target orientation towards which torque will be exerted. Since `BodyGyro` does not apply translational force, the translational/positional component of the [DataType.CFrame](https://developer.roblox.com/search#stq=CFrame), `CFrame.p`, is ignored. Consider using one of the following CFrame constructors in setting this property: `CFrame.fromAxisAngle`, `CFrame.fromEulerAnglesXYZ` or `CFrame.fromEulerAnglesYXZ`. Beware of [gimbal lock](https://en.wikipedia.org/wiki/Gimbal_lock) as you choose which of these methods and what angles (in radians). Additionally, you could use `CFrame.new(gyro.Parent.Position, targetPosition)` in order to have the BodyGyro "look at" a targetPosition ([DataType.Vector3](https://developer.roblox.com/search#stq=Vector3)).