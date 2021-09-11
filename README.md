# ebiten-input
Map keys to actions in ebiten

## Usage
```go
import input "github.com/tducasse/ebiten-input"

keys := map[string][]ebiten.Key{
    "up":    {ebiten.KeyArrowUp, ebiten.KeyW},
    "down":  {ebiten.KeyArrowDown, ebiten.KeyS},
    "right": {ebiten.KeyArrowRight, ebiten.KeyD},
    "left":  {ebiten.KeyArrowLeft, ebiten.KeyA},
  }
input.Init(keys)

// add actions later with
input.AddAction("action", []ebiten.Key{ebiten.KeySpace})

// check the status with 
if input.IsPressed("up") {
  // do something here
}
```