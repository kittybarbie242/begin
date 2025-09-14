## 2. Điều khiển ngắt ngoài EXTI 

### Cấu hình ngắt ngoài cho 1 nút nhấn. Khi nhấn nút, trạng thái của led sẽ đảo ngược. Trong quá trình đó, 1 led khác vẫn nhấp náy với chu kỳ 1HZ 

**Ý tưởng:**  
- Cấu hình **PA5** và **PA6** ở chế độ Output để điều khiển 2 LED.  
- Cấu hình **PB0** ở chế độ Input Pull-up để làm nút nhấn.  
- LED2 (PA6) nhấp nháy liên tục với chu kỳ ~1000ms bằng hàm `delay()`.  
- Sử dụng **EXTI Line0** cho PB0 để sinh ngắt ngoài, khi nhấn nút thì LED1 (PA5) sẽ đổi trạng thái (bật ↔ tắt).  
- Dùng **NVIC** để quản lý ưu tiên ngắt và đảm bảo chương trình xử lý đúng khi có sự kiện nút nhấn.  

**Phần cứng:**  

![alt text](Ex3.jpg)  

**Source code:** [Bài 3](main.c)  

**Video Demo:** [DEMO](https://drive.google.com/drive/u/0/folders/18WuSejkMz8G0gB_w4a7SlnFkfVLqn4w3)
