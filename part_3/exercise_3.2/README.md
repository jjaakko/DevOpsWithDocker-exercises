To download video from yle areena to current folder, use image like this:

```
docker build -t yle-dl .
docker run -v "$(pwd)":/videos yle-dl https://areena.yle.fi/tv/ohjelmat/30-21?play=1-50410620
```
