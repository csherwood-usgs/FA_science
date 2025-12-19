### Propagation of error

It is super important to have a feel for the uncertainty in your measurements.  

When you know the uncertainty of some measurement $x$, you can state the uncertainty as $x\pm\delta x$, where $\delta x$ is the uncertainty.   

If you have many measurements of something, you typically report the mean (average) as your best guess of $x$, and the standard deviation as your value of $\delta x$.  

"Propagating" uncertainty means combining several sources of uncertainty to get the total value. 
Let's say you are adding $x + y$, with uncertainties of $\delta x$ and $\delta y$. The combined uncertainty is $\sqrt{\delta x^2 + \delta y^2}$.  

The formula is $\delta q = |q| * \sqrt{ (\delta x / x)^2 + (\delta y / y)^2 }$  

If you are are measuring his speed by timing how fast Usain Bolt runs a 100 m, you might have three stop watches with mean value of $t$ = 9.58 s, 
but a standard deviation of $\delta t$ = 0.02 s.  So his time is 9.58 $\pm$ 0.02.  

But the track distance measurement is not exact...there is a little bit of slop in where the finish line laser is located...say 2 millimeters, so $\delta x$ = 0.002 m. Thenl the distance he ran is $x$ = 100 $\pm$ 0.002 m. 
That adds some more uncertainty to our calculation of his speed.

His speed $q$ is 100 m / 9.58 s = 10.4384133612 m/s. 

The uncertainty is $\delta q = |10.4384133612| * \sqrt{ (0.002/100)^2 + (0.02/9.58)^2 } = 10.4384133612 * \sqrt{ 4 * 10^{-10} + 4.35841 * 10{-6} } $

We can take a little shortcut if we want to. 
Our uncertainty in timing is way bigger (100x) than our uncertainty in distance, so we will use that as our error estimate, and say our uncertainty in his speed was 0.02/9.58 = 0.002 m/s.


#### Interupting the lecture on propagation of error to discuss: How many significant digits to report?

His speed is 100 m / 9.58 = 10.4384133612 m/s. But, since we know our timing accuracy is only $\pm$ 0.02 s, it doesn't make sense to report all of those significant digits. 
The guideline is: **Report the result to the same decimal place as its uncertainty.** So, we would report 10.438 $\pm$ 0.002 m/s.
