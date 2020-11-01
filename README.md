# video_streaming
Transmisión de video en tiempo real sobre un servidor http. Con FFMPEG, NGINX y HTTPS.

Pasos
1. Copiar la carpeta FFMPEG al disco local C  <br>
   C:\FFMPEG
2. Copiar la carpeta NGINX al disco local C <br>
   C:\NGINX
3. Copiar la carpeta onAir al escritorio <br>
   C:\...\DESKTOP\onAir
4. Abrir un terminal y colocar los siguientes comandos para activar el servidor rtmp <br>
   cd C:\nginx  <br>
   nginx.exe
   - Para finalizar el servidor rtmp abrir otro terminal y colocar <br>
      cd C:\nginx <br>
      nginx -s stop
5. Abrir otro terminal y colocar los siguientes comandos para transmitir el video almacenado <br>
   cd C:\ffmpeg <br>
   ffmpeg -re -i android.mp4 -c:v libx264 -loop -2 -b:a 160k -ar 44100 -strict -4 -f flv rtmp://192.168.1.19:1935/livestream
   - Para transmitir el video de la camara ejecutar el siguiente comando  <br>
      ffmpeg -re -f dshow -i video="HP Wide Vision HD" -video_size 300x200 -c:v libx264 -b:v 64k -bufsize 64k -loop -2 -strict -2 -f flv rtmp://192.168.1.19:1935/livestream
6. Abrir otro terminal y colocar los siguientes comandos para levantar el servidor http <br>
   cd C:\...\DESKTOP\onAir <br>
   npm run dev 
7. Abrir algun navegador y colocar <br>
   http://localhost:8000
   
  
  
 
 
