# UTS-Turtlebot4-Multipoint
Lokalisasi dan Pemetaan/RE702 Midterm Exam 4222201041 Rahmat Hidayat RE 7 B Pagi

# RE702 Midterm – Localization & Mapping
Repositori ini disusun sebagai bagian dari pengerjaan tugas Ujian Tengah Semester mata kuliah Lokalisasi dan Pemetaan (RE702). Package ROS2 yang dibuat berfungsi untuk mengarahkan TurtleBot4 berpindah dari satu titik ke titik lainnya serta mengaktifkan buzzer sesuai instruksi asesmen.

# Persiapan Sebelum Menjalankan Package
Sebelum melakukan proses build dan menjalankan package ROS2, pastikan Anda telah membuat peta (map) sesuai dengan lingkungan yang digunakan. Peta hasil pemetaan harus disimpan di dalam folder maps/. Untuk membuat peta baru, silakan mengikuti panduan resmi TurtleBot4 pada tautan berikut:

https://turtlebot.github.io/turtlebot4-user-manual/tutorials/generate_map.html

Pastikan perangkat (laptop/PC) yang digunakan terhubung ke jaringan LAN atau WiFi yang sama dengan TurtleBot4. Setelah itu, lakukan koneksi ke robot melalui SSH.

# 1. Running Localization & Navigation
Di terminal TurtleBot4, jalankan:
```bash
ros2 launch turtlebot4_navigation localization.launch.py map:=path/ke/map.yaml
Pastikan path/ke/map.yaml diganti dengan path file map yang benar.
```
# 2. Jalankan Nav2 (di robot TurtleBot4)
Di terminal TurtleBot4 lainnya, jalankan:
```bash
ros2 launch turtlebot4_navigation nav2.launch.py
```
# 3. Jalankan visualisasi RViz2 (di laptop/PC)
Pada terminal laptop/PC yang terhubung dengan TurtleBot4, jalankan:
```bash
ros2 launch turtlebot4_viz view_navigation.launch.py
Pastikan pose robot di RViz sesuai dengan posisi fisik di lapangan.
```
# Build Package dari Repository Ini
Buat workspace:
```bash
mkdir -p ros2_ws/src
cd ros2_ws/src
```
Clone repository:
```bash
https://github.com/RahmatHidayat19/UTS-Turtlebot4-Multipoint.git
```
Build workspace:
```bash
cd ../
colcon build
source install/setup.bash
```
Menjalankan program:
```bash
ros2 run abdi_pkg abdinode
```
# Demo
https://youtu.be/b6Jc3NDo4qI?si=GejQVifirh4QoRAc
