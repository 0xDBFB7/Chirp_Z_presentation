

# Data preparation

Data was obtained via the Internet Archive. A recording by [LibreVox](https://archive.org/details/niblung_2406_librivox/
). Concatenated using:

```
s=""; for i in nib*.mp3; do s="$s|$i"; done; echo ${s:1}
ffmpeg -i "concat:<string>" -acodec copy wagner_ring_cycle.mp3
ffmpeg -i wagner_ring_cycle.mp3 wagner_ring_cycle.wav

```

