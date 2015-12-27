```{r}

library(tuneR)
library(audio)

christmas_file <- tempfile()

download.file("https://sites.google.com/site/pocketecoworld/merrychristmas1.wav", christmas_file, mode = "wb")

myWave <- readWave(christmas_file)

mywav <- audioSample(myWave@left, myWave@samp.rate, myWave@bit)


a <- audio::play(mywav)

pause(a)

resume(a)

```
