# MobileRobot-Basis-AraUco-Marker

Sistem ini dirancang untuk memberikan navigasi visual presisi pada mobile robot menggunakan deteksi ArUco Marker. Kamera berfungsi sebagai sensor utama yang menangkap video secara real-time. Setiap frame dikonversi ke skala abu-abu untuk mempermudah dan mempercepat proses deteksi.
Proses deteksi dilakukan menggunakan pustaka OpenCV. Marker yang terdeteksi akan dianalisis berdasarkan pola dan dicocokkan dengan kamus ArUco. Jika valid, sistem akan mengembalikan ID marker serta koordinat keempat sudutnya. Informasi ini digunakan untuk estimasi posisi marker dalam bidang pandang kamera, khususnya pada sumbu-x.
Jika posisi marker berada dalam toleransi yang telah ditentukan, Raspberry Pi 4B akan mengirimkan perintah ke ESP32 untuk mendekati marker. Jika tidak, sistem akan mengoreksi posisi robot terlebih dahulu. Setelah jarak marker kurang dari 35 cm, robot akan menjalankan perintah berdasarkan ID marker tersebut.
Komunikasi antara Raspberry Pi 4B dan ESP32 dilakukan secara nirkabel melalui protokol WiFi. Sistem ini memungkinkan navigasi visual yang efisien dan responsif dalam waktu nyata (real-time).

## 📌 Fitur

- Deteksi ArUco Marker secara real-time menggunakan kamera
- Estimasi posisi marker (fokus pada sumbu-x)
- Pengambilan keputusan berdasarkan ID marker
- Komunikasi nirkabel antara Raspberry Pi 4B dan ESP32
- Navigasi otomatis dan koreksi posisi robot

## 🧰 Kebutuhan

- Raspberry Pi 4B (atau setara)
- ESP32 (sebagai pengontrol motor)
- Kamera (USB Webcam atau Pi Camera)
- Python 3.7 atau lebih baru
- OpenCV (`opencv-contrib-python`)
- Koneksi WiFi antara Raspberry Pi dan ESP32

📄 Lisensi
Repositori ini menggunakan lisensi MIT. Silakan digunakan dan dimodifikasi untuk keperluan edukasi atau riset.
