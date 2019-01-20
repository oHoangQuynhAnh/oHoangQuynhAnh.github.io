---
layout: post
title:  "Things I do (not) know after 2 years being a developer"
date:   2020-02-27
excerpt: "There is a lot of things to tell after 2 years being a mediocre developer"
# image: "/images/post1.jpg"
---

Thế là hơn 2 tháng mình nghỉ việc, kết thúc 2 năm chạy loăng quăng ăn hại ở Sun. 2 tháng vừa rồi mình chưa viết thêm được dòng code nào, có lúc nghĩ hay đi làm barista ở quán cà phê cũng hay, nhưng nghĩ lại ngoài code ra mình không biết làm gì khác. Nhưng chính xác ngoài code ra thì mình đã làm những gì trong 2 năm vừa rồi.

Mình vào Sun thực tập từ lúc còn là đứa sinh viên năm ba không biết viết một câu query ra hồn. Từ đó tới lúc được sang keangnam làm dự án cũng học được kha khá thứ, và cũng nhận ra mình không biết kha khá thứ. 2 tháng hiện tại là thời gian đủ để mình nhìn lại knowledge gap và viết lại ở đây sau hơn 2 năm không viết cái gì về tech để promote bản thân lmao.

### Web Development
1. **Ruby on Rails**
   - **Ruby** là ngôn ngữ mình sử dụng thoải mái nhất. Thực ra ban đầu mình apply vào Sun vị trí thực tập PHP vì mình nghĩ PHP phổ biến hơn dễ dùng hơn. Nhưng sau 2 năm mình chỉ muốn nói là mình yêu Ruby, thế thôi. OOP trong Ruby, method lookup path, callbacks hay Eigen class là tỉ tỉ thứ mình phải đọc đi đọc lại trong quãng thời gian ôn để phỏng vấn join division bên Keangnam. Giờ nghĩ lại vẫn hãi một chút. Tuy vậy mình không biết chút gì về Java nên khá chật vật với việc học trên trường..
   - **Rails**: đi kèm với Ruby thì Rails là framework mình quen thuộc nhất, mình có thể init một project, dễ dàng trace lại các module code, thoải mái với việc viết API và unit test và ti tỉ thứ khác trong Rails với coding convention tử tế.
   - Trong năm vừa rồi mình cũng được setup môi trường một project Ruby on Rails hoàn chỉnh trên EC2 của aws :) Dù không có gì khó khăn lắm nhưng lần đầu tiên được ssh lên một con server và setup từ đầu mọi thứ cũng giúp mình học được nhiều thứ.
2. **Django và Flask - Python**
   - Lúc mới sang keangnam mình chơi dài cả tháng do không có dự án ruby, mình lại là ma mới chưa đi làm fulltime được. Xong đùng cái thì mình bị gọi hỏi có muốn thử code Python không. Trước đó chỉ nghĩ python toàn làm mấy cái cao siêu AI ML. Do ngồi chơi chán quá nên mình ok và được bảo sẽ training trong vài tuần. Được dẫn qua nói chuyện với chị L một trong những tech lead có tâm nhất quả đất.
   - Sau đó thì mình học python cơ bản, đủ dùng dù cứ đụng tới cái gì mình lại phải đi đọc doc. Sau đó chuyển sang học Django. Lúc này biết virtual environment là cái gì, pip là cái gì, init được project. Làm được 1 cái project nhỏ deploy lên heroku với Django.
   - Nhưng giờ hỏi import trong python hoạt động như thế nào hay xử lý multi threads trong python vẫn khó hiểu với mình.
   - Sau đó được gọi ra nói chuyện với 2 anh trong một dự án, hỏi mấy câu cơ bản về Python với xử lý trong web development nói chung. Bị quẳng vào một dự án dùng Flask. Mình kiểu the fuck. Nhưng đó cũng là dự án chính thức cho khách hàng đầu tiên mình được làm. Lần đầu tiên viết API docs, lần đầu tiên viết một cái CRUD API cơ bản, lần đầu tiên viết unit test python, lần đầu tiên dùng API Postman. Được học thêm về API Gateway. Làm được hơn tháng thì dự án pending :))
   - Sau đó mình lại bị đẩy sang một dự án khác dùng cả Python lẫn Rails. Sang dự án này mình học được nhiều thứ từ deploy tới viết doc. Rails API thì quen thuộc không có gì, python thuần dính tới xử lý ảnh thì sợ lắm vì mình không biết gì về xử lý ảnh cả, python cũng bập bõm. Nhưng cuối cùng thì cũng xoay xở được trong dự án cho tới lúc nghỉ việc.
3. **API**
   - Lúc thực tập mình chỉ làm các project theo dạng MVC thuần, controller xử lý logic rồi server render view, không dùng framework frontend gì luôn. Hồi đó không hiểu APIs là gì chỉ biết người người nhà nhà nói về APIs như một thứ gì đó thần kì lắm, *"chỉ cần gọi API để xử lý abcxyz"*. Cho tới lúc sang Keangnam mình mới thực sự hiểu API là gì và trong suốt quãng thời gian hơn năm đó mình chỉ toàn viết API mà không đụng gì tới phần view hết :))
   - RESTful APIs: biết cơ bản, từ requirement chức năng mình có thể viết được API, biết được cần trả về cái gì và xử lý logic như nào. API is not a myth anymore lmao.
   - Document: Sau khi biết API là gì mình cũng mới biết cách viết API docs. Dự án đầu tiên mình vào chỉ vỏn vẹn có hơn tháng, ticket đầu tiên là pair programming với một bạn nữa viết API docs bằng Swagger. Sau đó thì biết dùng google sheet. Rồi gần tới lúc nghỉ thì biết viết thêm deploy document. Và mình nhận ra viết document khó như nào khi lúc nào cũng có khả năng bị thiếu gì đó.
   - Microservice: 2 dự án Python với 1 dự án Rails mình tham gia đều có mùi microservices. Hiểu được kiến trúc và cách các API gọi tới nhau. Có đọc về API Gateway.
4. Database
   - Sau 2 năm mình vẫn chỉ sử dụng MySQL.
   - Đã biết viết query cơ bản dùng join, đụng tới subquery vẫn hơi lủng củng
   - Dự án đơn giản có thể tự vẽ vời xây dựng database.
   - Trước đó hồi đi học ở Techkids (giờ thành MindX rồi không biết có ăn theo gì TedX không) thì có được dạy NoSQL mà hồi đó mình còn chả hiểu query là cái gì database là cái gì ù ù cạc cạc :)) Chỉ nhớ dùng MongoDB với Robomongo.
5. Security
   - Chuyên ngành mình học trên trường là Information Security. Nhưng đi làm lại làm web developer nên mảng security mình khá lủng củng.
   - Authorization và Authentication là hai thứ mình phải đọc đi đọc lại từ lúc đi học cho tới lúc đi làm, nên nếu bị hỏi phỏng vấn chắc mình cũng trả lời được còn implement trong project thì tùy yêu cầu dự án mà mình phải google hay không, đi kèm với đó là hai thứ kinh điển cookie và session. Với Rails thì mình không có vấn đề gì lắm
   - OAuth2 và JWT: lại nhớ mấy tháng sang Keangnam chưa có dự án mình có được một anh bảo tìm hiểu về vấn đề này đi. Cũng đi đọc và có thể tự implement OAuth2 cho một project Rails mà không cần dùng tới gem.
   - Các thể loại injection. Học gạo để qua môn trên trường với SQL Injections,trong Rails thì để ý một chút lúc thao tác với models với check CI thôi.

### Others
#### 1. Version control - Git
  - Vẫn nhớ git là bài học đầu đời khi mình bước chân vào Sun. Tới giờ đã có thể push pull fetch merge rebase cherry pick thoải mái.
  - Các concept nâng cao hơn của git như git hoạt động như thế nào thì có nhớ nhưng bị hỏi chắc vẫn sẽ phải google.

#### Linux OS
  - Unix command và bash: đủ để dùng terminal cài đặt được môi trường deploy trên server. Nhưng vẫn chưa tự viết được một bash program phức tạp.

#### Docker
- Dự án nào cũng có docker nhưng mình chưa xử lý ticket nào dính tới cái này cả mà chỉ đọc code với đọc đi đọc lại concept về container. Hiểu được concept máy ảo, pros với một số practices của docker, dockerize một project Rails với django.
#### Infra
- **Network**: Hiểu các khái niệm về IP, DNS, TCP/UDP (dù mình trượt lập trình mạng với Java haha..). Nhưng giờ bảo mình ngồi tính subnet mask hay cấu hình thủ công một VPC trong thời điểm hiện tại thì mình chắc chắn phải học lại mạng máy tính.
- **Amazon Web Service**: dev nửa mùa như mình dĩ nhiên là không được cấp quyền vào account aws của dự án để nghịch rồi. Nhưng cũng le ve hóng hớt được một chút lúc dự án có incident. Được sờ vào mấy con EC2 của aws lúc deploy với đọc log để điều tra incident.

#### Frontend
- Sau hơn năm chỉ làm backend viết API thì giờ kiến thức Frontend của mình gần như bằng không? Nhớ được mấy tag html, css với javascript thì google.
- Cũng tự học Reac với Vue được một thời gian nhưng không làm được gì tử tế.

Sau 2 năm với kiến thức hổng lỗ chỗ khi tổng hợp lại như này mình nghĩ mình vẫn muốn đi làm barista.
