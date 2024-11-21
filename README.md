# av3a_ffmpeg_decoder
av3a real ffmpeg decoder. Transcoding fast! Thanks feiyang build it. 
av3a 真正的解码器，速度很快。感谢肥羊大佬的编译。

用法  
1. 在release页面下载压缩包，解压(https://github.com/raddyfiy/av3a_ffmpeg_decoder/releases/download/v1.0/av3a_ffmpeg.zip)
2. 打开一个ubuntu环境，或者windows装子系统也行
3. 加载so库：  export LD_LIBRARY_PATH=./av3a_ffmpeg_lib/
4. 解码cctv文件示例

./av3a_ffmpeg -i input.ts -map 0:v -map 0:a  -c:v copy -c:a:0 eac3 -filter:a:0 "channelmap=0|1|2|3|4|5:FL+FR+FC+LFE+SL+SR" output.ts

可能的错误  

1. 如果你的环境提示缺了某个so库，那么可以装一个ubuntu22虚拟机，用find命令搜到相应的位置，把so拷贝出来，放入av3a_ffmpeg_lib

