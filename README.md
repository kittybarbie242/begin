## 2. Cấu hình GPIO và nạp chương trình

### 2.1. Cấu hình 2 nhóm LED ở chế độ Output, LED nhấp nháy với chu kỳ 1000ms 

> Ý tưởng:

- Thực hiện cấu hình GPIO chọn port quan tâm về port, mode và speed

- Viết hàm delay tương đối sau có thể thay thế bằng `Systick` hoặc `Timer` cho các bài sau

- Sử dụng SetBits và ResetBits để đảo trạng thái LED

> Phần cứng:
