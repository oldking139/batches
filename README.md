### 以下批处理仅适用于Windows CMD，并不适用于Powershell。

音频均衡化

所需组件：```ffmpeg-normalize```


批处理：

```for %a in ("*.mp3") do ffmpeg-normalize "%~na.mp3" --force --progress --sample-rate "48000" --target-level "-23" --true-peak "-4" --output "C:\Downloads\ASMUSIC\normalized\%~na.mp3" -c:a mp3 -b:a 320k```


---
获取音频文件名，时长，演唱者等



所需组件：```mediainfo cli```



批处理：

```for %a in ("*.mp3") do mediainfo --Inform="General;%FileName%,%Duration%,%Performer%" "%~na.mp3" >> info.txt```

---

