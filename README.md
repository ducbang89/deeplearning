CS231n ConvNet for Visual Recognition (Vietnamese version)
<Bài viết được dịch từ http://cs231n.github.io/)

Phần 1: Mạng nơron
  1.	Phân lớp ảnh: các cách tiếp cận để điều khiển dữ liệu, thuật toán k-Nearest neighbor, huấn luyệnn/xác nhận/kiểm thử
  2.	Phân lớp tuyến tính: SVM, Softmax
  3.	Tối ưu: Stochastic Gradient Descent
  4.	Backpropagation, Intuitions
  5.	Mạng nơron phần 1: Cài đặt kiến trúc
  6.	Mạng nơron phần 2: Cài đặt dữ liệu và hàm mất mát
  7.	Mạng nơron phần 3: Học và đánh giá

Phần 2: ConvNets
  1.	ConvNets: kiến trúc, Lớp Convolution/Pooling
  2.	Hiểu và minh hoạ ConvNets
  3.	Học chuyển giao và tinh chỉnh ConvNet
 

Phân lớp ảnh
Ý nghĩa: ở đây chúng ta cùng nhau tìm hiểu bài toán phân lớp ảnh ở đó chúng ta sẽ gán cho mỗi bức ảnh đầu vào là 1 nhãn tương ứng từ một tập có sẵn. đây là một trong những bài toán cốt lõi của l nh vực Computer Vision, mặc dù đơn giản nhưng lại có ứng dụng thực tế rất rộng rãi. Các bài toán khác như nhận diện vật thể, hay phân tách vật thể c ũng có thể suy biến về bài toán phân lớp này

Ví dụ: như hình ảnh dưới đây, một mô hình phân lớp ảnh lấy một bức ảnh và gán xác xuất cho 4 nhãn (mèo, chó, mũ, cái mi ệng). đối v ới máy tính, 1 bức ảnh sẽ là 1 thể hiện của 1 ma trận 3 chièu. ở đây hình ảnh con mèo có 248 pixel chiều r ộng, 400 pixel chiều cao và 3 màu RGB. Do đó bức ảnh sẽ bao gồm 248 x400 x3 = 297600 số. mỗi con số sẽ là 1 số nguyên từ 0(black) đến 255(white)
