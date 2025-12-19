## Falmouth Academy Science Fair - Wave Attenuation

### Angular frequency
https://github.com/csherwood-usgs/FA_science/blob/main/sine_curves.ipynb

#### Sine curves
A sine curve is defined by four variables:
* Period ($T$) or frequency ($f = 1/T$)
* Amplitude ($a$)
* Phase ($\phi$)
* Time ($t$)

Because computers need the angular frequency ($\omega$)in radians, we have to convert the angular frequency to radians
$\omega = 2\pi/T = 2\pi*f$

Then elevation ($z$) can be calculated as:  

$z(t) = a*cos( \omega * t + \phi )$

#### Addition of sine curves
Sine curves can be added together to form more complicated time series.  
Special examples:
* Square wave
  * Sawtooth wave

https://github.com/csherwood-usgs/FA_science/blob/main/sine_curves_part2.ipynb

### Spectra (periodograms)
We can construct a time series that looks like a sea surface using a handful of amplitudes, periods, and random phases.  

We can invert the time series using a *discrete Fourier transform* (DFT) to get a spectrum...i.e., the amplitude of each sine curve at specific frequencies. A graph of this is called a *periodogram* or a *spectrum*. 
This procedure is often done using a famous alogorithm called the *fast Fourier transform* (FFT). If done at a special collection of frequencies, the proceedure is exact. If you pick other frequencies, there is some 
*spectral leakage* that blurs the peak periods.

https://github.com/csherwood-usgs/FA_science/blob/main/spectrum.ipynb

### Making synthetic sea surface
It turns out that ocean spectra have distinctive shapes and, after measuring a ton of waves, scientists have an *empirical* equation that describes that shape. 
We can use the formula to generate a collection of amplitudes at various frequencies and ust the to generate a fake time series that looks like a sea surface.
We just need to define our significant wave height ($H_{m0}$) and the peak period $T_p$.

https://github.com/csherwood-usgs/FA_science/blob/main/make_fake_sea_surface_elevations.ipynb

### Inverting sea surface to get spectrum
If we have a measured time series of water elevation, we can calculate the spectrum. For technical reasons, we divide the time series up into shorter, overlapping chunks and apply a *window* to the data to taper the ends.
Then we do an FFT, and average all of the FFTs to generate a spectrum (aka a periodogram). By convention, the spectrum has units of $m^2/Hz$, because squaring the meters generates units that are proportional to energy.
Summing all of the energy in over all frequencies gives the total energy, which can be used to calculate significant wave height $H_{m0}$.  

https://github.com/csherwood-usgs/FA_science/blob/main/elevation_to_spectrum.ipynb  

### First look at the data: Bucket test
Use Pandas to load the `.csv` file of the data, and Matplotlib to make a time series plot.  

https://github.com/csherwood-usgs/FA_science/blob/main/first_plot.ipynb
