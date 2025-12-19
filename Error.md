### Propagation of error

It is super important to have a feel for the uncertainty in your measurements.  

When you know the uncertainty of some measurement $x$, you can state the uncertainty as $x\pm\delta x$, where $\delta x$ is the uncertainty.   

If you have many measurements of something, you typically report the mean (average) as your best guess of $x$, and the standard deviation as your value of $\delta x$.  

"Propagating" uncertainty means combining several sources of uncertainty to get the total value. Let's say you are adding $x + y$, with uncertainties of $\delta x$ and $\delta y$. The combined uncertainty is $\sqrt{\delta x^2 + \delta y^2}$.

A more complicated example: if you are are measuring speed by timing how fast Usain Bolt runs a 100 m, you might have three stop watches with mean value of $t$ = 9.58 s, 
but a standard deviation of $\delta t$ = 0.02 s.  So his time is 9.58 $\pm$ 0.02 
and his speed is speed is 100 m / 9.58 s = 10.4384133612 m/s. 
The uncertainty from the timing is the fractional uncertainty $t / \delta t$ = 9.58/0.02 = 0.002. 
Multiply the fractional uncertainty by the total time, and we have 9.58 * 0.002 = 0.0196. Round that to two digits, and we have 0.002

But lets imagine that the track measurement is not exact...a little bit of slop in where the finish line laser is located...say 2 millimeters or 0.002 m. So the distance he ran is 100 $\pm$ 0.002 m. 
That adds some more uncertainty to our calculation of his speed.

Lets calculate the percentage of uncertainty:  

Distance uncertainty 100/0.002 = 0.00002 = 0.002%  

Time uncertainty 9.58/0.02 ≈ 0.002 = 0.2%  

Combined uncertainty: $\sqrt{ ({ \delta x / x } + { \delta t / t } )}$

Our uncertainty in timing is way bigger (100x) than our uncertainty in distance, so we will us that as our error estimate, and say our uncertainty in his speed was 0.002 x 


#### Interupting the lecture on propagation of error to discuss: How many significant digits to report?

His speed is 100 m / 9.58 = 10.4384133612 m/s. But, since we know our timing accuracy is only $\pm$ 0.02 s, it doesn't make sense to report all of those significant digits. 
The guideline is: **Report the result to the same decimal place as its uncertainty.** So, we would report
