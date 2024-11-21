# av3a_ffmpeg_decoder
av3a real ffmpeg decoder. Transcoding fast!
av3a 真正的解码器，速度很快。  

用法  
1. 在release页面下载压缩包，解压
2. 打开一个ubuntu环境，或者windows装子系统也行
3. 加载so库：  export LD_LIBRARY_PATH=./av3a_ffmpeg_lib/
4. 解码cctv文件
./av3a_ffmpeg -i decodetest.ts.ts -map 0:v -map 0:a  -c:v copy -c:a:0 eac3 -filter:a:0 "channelmap=0|1|2|3|4|5:FL+FR+FC+LFE+SL+SR" decoderes.ts
