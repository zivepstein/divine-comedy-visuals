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
