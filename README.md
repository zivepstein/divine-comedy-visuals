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
```
//Flor de Fuego

shape(200,0.5,1.5)
.scale(0.5,0.5)
.color([0.5,2].smooth(1),0.3,0)
.repeat(2,2)
.modulateScale(osc(3,0.5),-0.6)
.add(o0,0.5)
.scale(0.9)
.out()
```

```
// by Mahalia H-R
// IG: mm_hr_

shape(()=>Math.sin(time)+1*3, .5,.01)
.repeat(5,3, ()=>a.fft[0]*2, ()=>a.fft[1]*2)
.scrollY(.5,0.1)
.layer(
  src(o1)
  .mask(o0)
  .luma(.01, .1)
  .invert(.2)
)
.modulate(o1,.02)
.out(o0)

osc(40, 0.09, 0.9)
.color(.9,0,5)
.modulate(osc(10).rotate(1, 0.5))
.rotate(1, 0.2)
.out(o1)

render(o0)
```
```
voronoi(20,-0.1,50)
.add(osc(1,0,1)).kaleid(3)
.scale(1,1,2).colorama().out(o1)
src(o1).mult(src(s0).modulateRotate(o1,100), -0.5)
  .out(o0)
```
