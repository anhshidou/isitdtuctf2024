![image](https://github.com/user-attachments/assets/0b83d73e-1e2f-49e0-baaf-60308d246379)

ở đây, mình nhận được 1 user tên là **arlenzxje**. Mình tìm được profile twitter của người này. Tuy nhiên, vì tác giả bảo wrong ways thì có lẽ mình phải tìm cách khác.

![image](https://github.com/user-attachments/assets/322faf6a-7cc6-431f-8f56-0d72b9491070)

Lúc này, mình tìm được 1 repo github xuất hiện tên của arlen

![image](https://github.com/user-attachments/assets/4bc1b711-3a8a-459e-88f4-7aea9a7fdaae)

Mình biết được rằng tên của Arlen là Arlen Fenmaris

![image](https://github.com/user-attachments/assets/400a714e-6387-4bff-8633-7e279c7f3ccb)

Tới đây, có vẻ như tác giả lại mắc lỗi là để tên facebook trùng tên với Username github, điều này khiến cho challenge được đi tắt mà không cần phải tìm ra profile facebook trên github nữa.

![image](https://github.com/user-attachments/assets/001fc80b-b066-4398-8193-b93c3627dfec)

Lúc này, mình có 1 profile facebook và có vẻ như nó không có gì cả. 

Sau khi xem hint là ở phần bio, và hint tiếp theo là public post sẽ luôn tồn tại public. Điều này khiến mình nhớ lại thủ thuật post ID.

![image](https://github.com/user-attachments/assets/6c12484d-63be-457e-b107-a4eabde75e1b)

Lấy ví dụ như bio của mình, lúc này mình nhớ đến ngày mới lập facebook, bio khi set up cũng sẽ đều hiện ra như là 1 bài post public riêng và đều sẽ có ID post. Vậy ID ở đây là gì, thì mỗi bài post trên fb sẽ có 1 ID khác nhau. Ví dụ như:

![image](https://github.com/user-attachments/assets/0889bcf2-eb61-4fe4-bafc-b516c2a00513)

Đây chính là ví dụ cho post ID. 

![image](https://github.com/user-attachments/assets/e3c854c1-c773-4a15-a449-3b9a7d3bc181)

Như các bạn thấy, trên URL, mình đã sửa URI về dưới dạng fbid mà mình chụp ở lúc đầu và thêm một path khác là posts vì path này sẽ giúp cho fb xác định được đâu là bài đăng, đâu là ảnh. Vậy áp dụng nó, mình sử dụng ctrl + U để xem source, vì đây là cách duy nhất để có thể xem một bài post về bio.

![image](https://github.com/user-attachments/assets/cab41285-586b-4a95-bf74-1241157fa372)

Áp dụng kỹ thuật trên

![image](https://github.com/user-attachments/assets/c215657b-5316-4732-bb80-d83e997d93e5)

Vào link ở comment là mình sẽ ra được đáp án.

Để mà nói thì, nhờ vào việc Facebook sẽ lưu lại tất cả các post ID có tồn tại trên dòng thời gian, mà chúng ta có một challenge khá thú vị. Tuy nhiên, điều này chỉ áp dụng với các bài đăng công khai và chưa bị xóa khỏi dòng thời gian. Vậy nên tính ứng dụng theo mình thấy của bài này không cao, nhưng đây vẫn là 1 trick khá thú vị trong một bài ctf.



