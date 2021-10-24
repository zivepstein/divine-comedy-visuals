# divine-comedy-visuals
```
speed = 0.7


shape(20,0.2,0.3)
.color(0.5,0.8,50)
  .scale(() => Math.sin(time)+2*2)
  .repeat(() => Math.sin(time)*10)
  .modulateRotate(o0)
  .scale(() => Math.sin(time)+a.fft[2] *0.2)
  .modulate(noise(2,2))
  .rotate(1, .2)
   .invert(2.4)
.out(o0)
```


```
voronoi(100,0.15)
  	.modulateScale(osc(8).rotate(Math.sin(time)),.5)
  	.thresh(.8)
	.modulateRotate(osc(7),.4)
	.thresh(.7)
  	.diff(src(o0).scale(1.8))
	.modulateScale(osc(2).modulateRotate(o0,.74))
	.diff(src(o0).rotate([-.012,.01,-.002,0]).scrollY(0,[-1/199800,0].fast(0.7)))
	.brightness([-.02,-.17].smooth().fast(.5))
	.out()
  ```
