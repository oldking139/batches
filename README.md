README.md

音频均衡化
所需组件：ffmpeg-normalize
for %a in ("*.mp3") do ffmpeg-normalize "%~na.mp3" --force --progress --sample-rate "48000" --target-level "-23" --true-peak "-4" --output "C:\Downloads\ASMUSIC\normalized\%~na.mp3" -c:a mp3 -b:a 320k

