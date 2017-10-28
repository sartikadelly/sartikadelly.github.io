---
layout: post
title: Testing embedded python code & gist
---

Test post with embedded code & gist.
Embed python code:
```python
import random
import pymel.core as pm

# Create new shader
shader, shadingGrp = pm.createSurfaceShader('lambert', name='my_material')

# Randomize color
shader.setColor([random.random(), random.random(), random.random()])

# Assign new shader to selected object
pm.sets(shadingGrp, forceElement=pm.selected())
```

Embed Gist test:<br>
Maya python script for doing cube reset on selected object

{% gist 3a2f1f07ef795074781a191fd4e4e224 %}
