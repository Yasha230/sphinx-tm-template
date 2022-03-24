# Codes

## Chapitre 1: projet 1

### module 

```python
import pygame

def init():
    pygame.init()
    window = pygame.display.set_mode((400, 300))
    
def getKey(Kname):
    ans = False
    for event in pygame.event.get(): pass
    keyInput = pygame.key.get_pressed()
    myKey = getattr(pygame, 'K_{}'.format(Kname))
    if KeyInput[myKey]:
        ans = True
    pygame.display.update()
    
    return ans
    
if __name__ == '__main__':
    init()
```

### code principal

```python
from djitellopy import tello
from time import sleep
import keypress as kp


kp.init()

dragonfly = tello.Tello()
dragonfly.connect()
print(dragonfly.get_battery())

def keyboardInput():
    lr, fb, ud, yv = 0, 0, 0, 0
    speed = 100

    if kp.getKey("a"): lr = -speed
    elif kp.getKey("d"): lr = speed

    if kp.getKey("w"): fb = speed
    elif kp.getKey("s"): fb = -speed

    if kp.getKey("UP"): ud = speed
    elif kp.getKey("DOWN"): ud = -speed

    if kp.getKey("LEFT"): yv = -speed
    elif kp.getKey("RIGHT"): yv = speed

    if kp.getKey("l"): dragonfly.land()
    elif kp.getKey("t"): dragonfly.takeoff()

    return [lr, fb, ud, yv]

while True:
    vals = keyboardInput()
    dragonfly.send_rc_control(vals[0], vals[1], vals[2], vals[3])
    sleep(0.05)
```