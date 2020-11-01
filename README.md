# video_streaming
Transmisión de video en tiempo real sobre un servidor http. Con FFMPEG, NGINX y HTTPS.

Pasos
1. Copiar la carpeta FFMPEG al disco local C
   C:\FFMPEG
2. Copiar la carpeta NGINX al disco local C
   C:\NGINX
3. Copiar la carpeta CCTV al escritorio
   C:\...\DESKTOP\CCTV
4. Abrir terminal y ejecutar siguiente comando
   cd C:\...\DESKTOP\CCTV
5. Ejecutar comando desde la terminal
   npm run dev 
6. Abrir algun navegador y colocar
   http://localhost:8000
   
  
  
  
COMANDOS
- ffmpeg -re -f dshow -i video="HP Wide Vision HD" -video_size 300x200 -c:v libx264 -b:v 64k -bufsize 64k -loop -2 -strict -2 -f flv rtmp://192.168.1.19:1935/livestream
- ffmpeg -re -i android.mp4 -c:v libx264 -loop -2 -b:a 160k -ar 44100 -strict -4 -f flv rtmp://192.168.1.19:1935/livestream
 
