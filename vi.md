# Hiểu thuật toán `llama-3.3-70b-versatile`

- Các cuộc thử nghiệm đã được triển khai được vài tuần. Chúng ta có thể thấy rằng anh ấy trả lời một cách có hệ thống các câu 53 và 43 và đưa ra các biến thể, nhưng rất hiếm khi.  
Điều này đơn giản có nghĩa là nó sử dụng các câu trả lời soạn sẵn trong 90% thời gian. Vậy tại sao lại làm điều này?  
Nó rất hay nhưng cũng rất dễ đoán. Nếu làm như vậy, chúng ta không cần phải viết lại mọi thứ hoặc làm lại vòng lặp nếu bạn muốn.  
Nhờ đó, chúng ta có thể đáp ứng nhanh chóng, với chi phí thấp hơn, nhưng vấn đề là chúng ta không thể đổi mới.  
Nếu chúng ta muốn điều gì đó mới mẻ, chúng ta sẽ cố gắng lấy các đoạn mã và ghép chúng lại với nhau.  
Nhưng vấn đề với điều đó là chúng ta không thể có một giao diện người dùng hợp lý và sáng tạo vì nó dựa trên các mã đã được tạo :)

# Làm thế nào tôi có thể hiểu được

- Đơn giản là tôi đã tạo một chút `script` Python dùng để gửi nhiều yêu cầu.  
Nó hoạt động với API. Mọi thứ sẽ theo ý của bạn ngoại trừ API.  
Đây đại khái là một phần mã tạo ra vòng lặp gửi này:

BẢO VỆ_0

- Bạn định nói với tôi: "Có, một vòng lặp while đơn giản trong Python phải không?" Có, nhưng nó hoạt động rất tốt. Trong 2 tuần, chúng tôi đã đạt được kết quả đáng kinh ngạc.

# Nghiên cứu của xql.dev

<h1>Yêu AI và toán học</h1>