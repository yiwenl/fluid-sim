# Fluid Simulation

Tool class for Fluid Simulation using alfrid

![Demo](demo.jpg)

## Install

Add this line to your package.json
`"fluid-sim": "github:yiwenl/fluid-sim"`

## Usage

`this._fluid = new FluidSimulation(settings);`

## API

### Update Fluid Simulation

`update()`

### Update with a flow

`updateFlow(mPos, mDir, mStrength = 1, mRadius = 1, mNoiseStrength = 0)`

### Update with a flow texture

`updateFlowWithMap(mTextureVel, mTextureDensity, uStrength = 1)`

## Example

```
import FluidSimulation from 'fluid-sim'

...

render() {
  ...
  // adding a flow at center (0.5, 0.5) moving up (0, 1)
  this._fluid.updateFlow([0.5, 0.5], [0, 1], 1, 1, 0.5);

  // update fluid
  this._fluid.update();

  // draw the density map
  this._bCopy.draw(this._fluid.density);

}
```
