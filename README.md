README.md

音频均衡化

所需组件：```ffmpeg-normalize```

单个文件：

```ffmpeg "2020.12.12 万有引力1.0.mp3" -af loudnorm=I=-23:LRA=7:tp=-2:measured_I=-30:measured_LRA=1.1:measured_tp=-11 04:measured_thresh=-40.21:offset=-0.47 -ar 48k -y "C:\Downloads\ASMUSIC\normalized\2020.12.12 万有引力1.0.mp3"```


批处理：

```for %a in ("*.mp3") do ffmpeg-normalize "%~na.mp3" --force --progress --sample-rate "48000" --target-level "-23" --true-peak "-4" --output "C:\Downloads\ASMUSIC\normalized\%~na.mp3" -c:a mp3 -b:a 320k```


---
获取音频文件名，时长，演唱者等



所需组件：```mediainfo cli```



批处理：

```for %a in ("*.mp3") do mediainfo --Inform="General;%FileName%,%Duration%,%Performer%" "%~na.mp3" >> info.txt```


