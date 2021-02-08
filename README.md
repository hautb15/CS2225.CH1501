# Đồ án môn học CS2225: Nhận dạng thị giác và ứng dụng
## Tên đồ án: Nhận diện hình ảnh một số động vật - đồ vật và hiển thị tên tương ứng
### Thực hiện: Trần Bình Hậu (CH2001004) - Phạm Thái Duy (CH2001003)

# Giới thiệu
Đồ án nhằm mục tiêu xây dựng ứng dụng nhận diện thế giới xung quanh và đọc tên đối tượng đó. Do phạm vi đồ án môn học nên chỉ thực hiện 10 loại đối tượng trong bộ dữ liệu CIFAR-10, và đọc thành tiếng Việt tên đối tượng tương ứng.

Đồ án chỉ dừng lại ở mức "Back-end" chứ chưa xây dựng thành phần mềm có giao diện web front-end để mọi người dễ sử dụng.

**File thực thi**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hautb15/CS2225.CH1501/blob/main/run.ipynb)

**File cài đặt**
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hautb15/CS2225.CH1501/blob/main/img-class.ipynb)

# Các lần cập nhật
`2020-02-06:` Cập nhật đồ án lần đầu tiên.

# Khảo sát đề tài
Bài toán nhận diện hình ảnh đồ vật thuộc bài toán image classification, text regconition. Qua khảo sát tại thời điểm thực hiện đồ án, trên thị trường có rất nhiều giải pháp cho bài toán này, như Picai, DietCameraAI, vivino, plantnet, coinoscope, amazon, snapchat, pinterest, google lens,.. 

Nhóm mong muốn thực hiện nhận diện và chuyển thành giọng nói tiếng Việt.

# Mô tả bài toán
**Task:** Nhận diện hình ảnh động vật - đồ vật

**Input:** Hình ảnh được đưa vào bằng hình chụp hoặc hình lấy trên google.

**Output:** Tên tương ứng với động vật - đồ vật đó.

**Dataset:** bộ dữ liệu được đánh nhãn của CIFAR-10

**Tình hình bài toán:** việc nhận diện hình ảnh theo bộ dataset CIFAR-10 rất phổ biến, là cơ sở cho nhiều nghiên cứu, ứng dụng trong lĩnh vực Machine Learning. Hạn chế của nó là độ chính xác khá thấp (khoảng 60% - 70%), thời gian train model khá lâu (3 giờ trở lên).

**Công việc nhóm thực hiện:**
  - Train lại model để nâng cao độ chính xác, kỳ vọng trên 80%.
  - Giảm thời gian train, kỳ vọng 30 phút - 45 phút.
  - Tích hợp thêm text - to - speech để tăng mức độ ứng dụng.

**Hình ảnh bộ dataset:**
![Alt text](/image-material/cifar-10-dataset.jpg "CIFAR-10")

# Các bước thực hiện:
1. Thu thập dữ liệu

2. Import các libraries cần thiết

3. Chuẩn hóa và xử lý dữ liệu

4. Cấu hình, tạo model, tối ưu model

5. Train model, Retrain model

6. Đánh giá, đo lường các thông số Precision, Recall, F1 Score hoặc MAP

7. Tạo dictionary để ánh xạ kết quả đầu ra tương ứng với mô hình

8. Kiểm thử model từ dữ liệu bên ngoài

9. Cải tiến model và các phương pháp xử lý liên tục


# Một số thông tin đáng lưu ý trong đồ án:
**Độ chính xác khi train :** 82.77%

**Độ chính xác khi retrain data với augmentation :** 87.86%

![Alt text](/image-material/loss-function.png "Loss Function")


![Alt text](/image-material/accuracy.png "Accuracy")

![Alt text](/image-material/measure.png "Calculate Precision, Recall, F1")


# Hạn chế của đề tài
  - Độ chính xác vẫn chưa đạt 100%.
  - Chưa thử nghiệm thành công text-to-speech cho tiếng Việt, đã thực hiện thành công text-to-speech cho tiếng Anh.

# Hướng phát triển tiếp theo
  - Mở rộng ứng dụng NLP để thực hiện text-to-speech cho tiếng Việt (dùng fpt.ai để dịch sang).
  - Mở rộng phạm vi đối tượng trong model, hỗ trợ trẻ em nhận diện thế giới xung quanh.
  - Nhận diện đối tượng trong một số ứng dụng khác.

# Tài liệu tham khảo
  - Keras
  - TensorFlow
  - CIFAR-10, CIFAR-100
  - CNN, RCNN,..

# Liên hệ:
hautb.15@grad.uit.edu.vn
duypt.15@grad.uit.edu.vn

