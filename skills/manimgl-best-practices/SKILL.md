---
name: "manimgl-best-practices"
description: "Best practices for ManimGL - 3Blue1Brown's OpenGL animation engine"
---

# ManimGL Best Practices

Best practices for ManimGL (Grant Sanderson's 3Blue1Brown version) - OpenGL-based animation engine with interactive development.

NOT for Manim Community Edition (which uses `manim` imports and `manim` CLI).

## Trigger
User mentions "manimgl", "ManimGL", "3b1b manim", code contains `from manimlib import *`, or working with InteractiveScene.

## Basic Scene Structure
```python
from manimlib import *

class MyScene(InteractiveScene):
    def construct(self):
        circle = Circle()
        self.add(circle)
        self.play(ShowCreation(circle))
        self.wait(1)
```

## Render Command
```bash
manimgl scene.py MyScene        # Render and preview
manimgl scene.py MyScene -se 15  # Interactive mode
manimgl scene.py MyScene -w      # Write to file
```

## Key Differences from ManimCE
| Feature | ManimGL | Manim Community |
|---------|---------|-----------------|
| Import | `from manimlib import *` | `from manim import *` |
| CLI | `manimgl` | `manim` |
| Math text | `Tex(R"\pi")` | `MathTex(r"\pi")` |
| Scene | `InteractiveScene` | `Scene` |
| Create anim | `ShowCreation` | `Create` |
| Camera | `self.frame` | `self.camera.frame` |

## Interactive Development
ManimGL's killer feature: `manimgl scene.py MyScene -se 20` drops into shell at line 20.
- `checkpoint_paste()` — Run with animations
- `checkpoint_paste(skip=True)` — Run instantly

## Camera Control
```python
frame = self.frame
frame.reorient(45, -30, 0, ORIGIN, 8)
```

## Rule Files
- rules/scenes.md, rules/mobjects.md, rules/animations.md
- rules/tex.md, rules/text.md, rules/t2c.md
- rules/3d.md, rules/camera.md, rules/interactive.md
