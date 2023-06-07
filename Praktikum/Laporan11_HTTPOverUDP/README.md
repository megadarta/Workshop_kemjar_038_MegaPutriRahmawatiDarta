![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.001.png)![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.002.jpeg)

HTTP OVER**   

UDP/QUIC
**


**Mega Putri Rahmawati Darta (3122640038) Akhmad Mufti Ali Wafa (3122640048)**

Apa itu QUIC??![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.003.jpeg)

QUIC adalah protokol multiplexing baru Google. Ini dijalankan pada UDP.

QUIC sukses dengan fitur SPDY.

Fitur QUIC![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.003.jpeg)

- Streaming multiplexing melalui Koneksi UDP yang sama.
- Ketahanan UDP terhadap kerugian (QUIC menceraikan HOL memblokir !!)
- Ketahanan FEC terhadap kehilangan QUIC mengirimkan XORsum dari paket.
- Keamanan seperti TLS
- Biaya rendah, mulai 0-RTT, bukan jabat tangan TCP
- Kontrol kemacetan pluggable TCP-CUBIC dan berbasis Pacing

Multiplexing Protocols![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.003.jpeg)

- HTTP/1.1
- SPDY
- QUIC

Congestion Control Algorithms![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.003.jpeg)

- TCP-CUBIC
- WebRTC Inter-Arrival
- Sprout-EWMA

QUIC LAYER![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.003.jpeg)![](image/Aspose.Words.473aeb80-7179-42d2-90d0-05b118fe2570.004.png)

Multiplexing protocols

QUIC is proposed by Google. Which inherits SPDY. 

- QUIC runs over UDP 
- QUIC runs over UDP, NOT TCP. 

his means eliminate HOL blocking.
