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

Embed Gist test:<br>
Maya python script for doing cube reset on selected object

{% gist 3a2f1f07ef795074781a191fd4e4e224 %}
