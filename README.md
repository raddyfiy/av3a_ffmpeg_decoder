# av3a_ffmpeg_decoder
av3a real ffmpeg decoder. Transcoding fast! 
Thanks @BaiPiaoH build windows version, and @feiyang build linux version.  

av3a 真正的解码器，速度很快。 感谢@BaiPiaoH编译的windows版本和肥羊大佬的linux版本。

## windows用法  
1. 在release页面下载压缩包，解压(https://github.com/raddyfiy/av3a_ffmpeg_decoder/releases/download/v1.0/)
4. 转码cctv文件示例

    D:\\av3a_ffmpeg_win\bin\ffmpeg.exe -i input.ts -map 0:v -map 0:a  -c:v copy -c:a:0 eac3 -filter:a:0 "channelmap=0|1|2|3|4|5:FL+FR+FC+LFE+SL+SR" output.ts  

    （ffmpeg路径要写所在文件夹的路径，修改input.ts为你的文件名即可）


## linux用法  
1. 在release页面下载压缩包，解压(https://github.com/raddyfiy/av3a_ffmpeg_decoder/releases/download/v1.0/)
2. 打开一个ubuntu环境，或者windows装子系统也行
3. 加载so库：  export LD_LIBRARY_PATH=./av3a_ffmpeg_lib/
4. 转码cctv文件示例：

    ./av3a_ffmpeg -i input.ts -map 0:v -map 0:a  -c:v copy -c:a:0 eac3 -filter:a:0 "channelmap=0|1|2|3|4|5:FL+FR+FC+LFE+SL+SR" output.ts

## 现成播放器  

release页面有mpv和potplayer的，下载即可

## 可能的错误  

1. 如果你的环境提示缺了某个so库，那么可以装一个ubuntu22虚拟机，用find命令搜到相应的位置，把so拷贝出来，放入av3a_ffmpeg_lib

