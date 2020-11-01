# video_streaming
Transmisión de video en tiempo real sobre un servidor http. Con FFMPEG, NGINX y HTTPS.

Pasos
1. Copiar la carpeta FFMPEG al disco local C
  C:/FFMPEG
  
  
  
  
COMANDOS
- ffmpeg -re -f dshow -i video="HP Wide Vision HD" -video_size 300x200 -c:v libx264 -b:v 64k -bufsize 64k -loop -2 -strict -2 -f flv rtmp://192.168.1.19:1935/livestream
- ffmpeg -re -i android.mp4 -c:v libx264 -loop -2 -b:a 160k -ar 44100 -strict -4 -f flv rtmp://192.168.1.19:1935/livestream
 
