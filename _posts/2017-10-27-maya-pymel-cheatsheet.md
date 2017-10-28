---
layout: post
title: Maya PyMEL quick cheatsheet
---

Testing 1st post with a PyMEL cheatsheet, as a reminder for myself.

Testing python code:
```python
# Simpy Getting Shapes from Shape/Vertex/Face/Mesh/Transform
shape = selection.getShape() if pm.objectType(selection, isType='transform') else pm.PyNode(selection)
```

