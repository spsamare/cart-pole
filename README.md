# Cart-Pole [Custom]
## _Some useful variants of openai-gym environment_

Cart-Pole [Custom] is a modified version of openai-gym cartpole v1 that is developed focusing on visual-based controlling.

## General modifications:
- Initial angle can be set via env.reset()
- Simulation duration can be modified via env.reset()
- Success range of the angle is extended to the range \[-45,45\] degrees
- env.render() is modified
  - Mode 'rgb_array' is extended to return grayscale and black-and-white pixel views
  - Allows to return pixel view without rendering the scene on a window
    - _Known issue: a window is rendered and set to hidden during viewer initialization to avoid generating empty pixel outputs_
- Pixel views can be compressed to low resolution views with env.down_scale()
- Reward is modified based on the deviation from the refernce state [_to be improved in future_]


### cart_pole_discreet.py:

- Added action for no force, i.e., force with zero magnitude

### cart_pole_continous.py:

- Action is set to a continous input, i.e. force magnitude is continous in both directions
- No bound for the input force magnitude [_to be improved as an option in future_]


## Installation

Install the dependencies.

```python
pip install -U gym
```

For testing with exporting views.

```python
pip install opencv-python
```
