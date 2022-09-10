## TRY TO CONTROL DRONE TO TAKEOFF AND LAND USING MAVSDK

in this day i decide to try to control drone to takeoff and land using MAVSDK.
i start with the following code:

```python
from mavsdk import System
drone = System()
await drone.connect("udp://:14540")
await drone.action.arm()
print("Armed")
await drone.action.takeoff()
print("Taking off")
await asyncio.sleep(8)
await drone.action.land()
print("Landing")
```

## TO RUN
To run code in this day you need to install MAVSDK and Mavproxy.
And makesure your drone can connect using udp in port 14540.

```bash
```