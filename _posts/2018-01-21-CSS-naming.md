---
layout: post
title:  "Các qui tắc đặt tên trong CSS"
date:   2018-01-21
excerpt: "Vẫn là bài dịch từ FreeCodeCamp medium"
image: "https://cdn-images-1.medium.com/max/1000/1*YunI3ChUVMlpmFzo75FczQ.png"
---
Tôi đã nghe nhiều lập trình viên nói rằng họ ghét CSS. Bằng kinh nghiệm bản thân, tôi nghĩ những lời kêu gào đó chẳng qua chỉ là kết quả của việc không học CSS một cách cẩn thận.

CSS không phải thứ “ngôn ngữ” đẹp nhất, nhưng nó thực sự đã hoàn thành tốt nhiệm vụ của mình là “tô điểm” cho web suốt 20 năm qua. Không quá tệ, đúng không?

Tuy nhiên càng viết CSS nhiều bạn sẽ sớm nhận ra một khuyết điểm to lớn của nó.

Rất khó để bảo trì những dòng code CSS.

Những dòng code CSS bị viết một cách cẩu thả sẽ sớm trở thành cơn ác mộng khủng khiếp.

Dưới đây là một vài quy tắc đặt tên cho CSS sẽ giúp bạn bớt stress một chút và thoát khỏi hàng tiếng đồng hồ chìm trong những dòng code.<br>
<img src="https://davidwalsh.name/demo/css-comic.jpg">
<br>
<small>Bạn đã từng như thế này rồi đúng không?</small>

### Sử dụng gạch ngang giữa các từ
Nếu bạn đã viết Javascript, thì việc đặt tên biến theo kiểu “camelCase” khá thông dụng.
<pre><code>
var redBox = document.getElementById('...')
</code></pre>
Tuyệt, đúng không?

Vấn đề là việc đặt tên như vậy không phù hợp với CSS cho lắm.

Đừng làm như này:
<pre><code>
	<strong>.redBox</strong> {
	  border: 1px solid red;
	}
</code></pre>

Thay vào đó hãy viết:

<pre><code>
	<strong>.red-box</strong> {
	  border: 1px solid red;
	}
</code></pre>
Đây là một chuẩn đặt tên khá phổ biến trong CSS. Nó cũng khá dễ đọc.

Đồng thời việc đặt tên như vậy sẽ nhất quán hơn với tên các thuộc tính css
<pre><code>
	<em>//Đúng</em>
	.some-classe {
	  <strong>font-weight:</strong> 10em;
	}
	//Sai
	.some-class {
	  <strong>fontWeight:</strong> 10em;
	}
</code></pre>

### Chuẩn đặt tên BEM

Mỗi nhóm sẽ có những cách viết selectors của CSS khác nhau. Có nhóm sử dụng gạch nối, có nhóm sẽ thích sử dụng một chuẩn đặt tên quy củ hơn gọi là BEM.

Nhìn chung, có 3 vấn đề chính mà các chuẩn đặt tên CSS sẽ cố gắng giải quyết:

1. Biết selectors có chức năng gì dựa vào tên của nó.
2. Biết selectors được dùng ở chỗ nào dựa vào tên của nó.
3. Biết mối quan hệ giữa các tên class dựa vào tên của chúng.

Bạn đã bao giờ nhìn thấy những tên class được viết thế này chưa:
<pre><code>
  <strong>.nav--secondary </strong>{
    ...
  }
  <strong>.nav__header </strong>{
    ...
  }
</code></pre>

Đó chính là chuẩn BEM.

### Giải thích BEM cho một đứa trẻ 5 tuổi.

BEM cố gắng chia giao diện người dùng thành những mảnh nhỏ có thể tái sử dụng.

Cùng xem hình vẽ dưới đây nhé:<br>
<img src="https://cdn-images-1.medium.com/max/800/1*qFy4XIpxbWx4oaOA3TYqpQ.png"><br>
<small>Đây là một bức ảnh tuyệt đỉnh của một tên người que.</small>

Không, nó không được giải gì cả : (

Người que đại diện cho một mảnh, giống như một khối thiết kế.

Có lẽ tới lúc này bạn đã đoán ra B trong BEM đại diện cho "Block" (khối)

Trong thực tế, một block có thể đại diện cho một thanh điều hướng, header, footer, hay các khối khác.

Dựa theo ví dụ được giải thích ở trên, một tên class lý tưởng có thể được sử dụng cho thành phần “người que” trên sẽ là `stick-man`.

Mảnh này sẽ được thiết kế lại như sau:

<pre><code>
	.stick-man {

	}
</code></pre>

Chúng ta đã sử dụng gạch ngang ở đây!<br>
<img src="https://cdn-images-1.medium.com/max/800/1*US1EoM_lvYOeJabGDhV2Eg.png"><br>

### E cho Elements (phần tử)

E trong BEM đại diện cho Elements

Nhìn chung thì các khối hiếm khi được tạo thành một cách độc lập.

Ví dụ, một tên người que phải có 1 cái `đầu`, hai `cẳng tay`, và một `đôi chân`.

`đầu`, `tay`, `chân` là những phần tử nhỏ trong một mảnh lớn. Chúng có thể được coi là những mảnh con hay là con của các phần tử cha mẹ.

Sử dụng chuẩn đặt tên BEM, tên class của các phần tử con sẽ được ngăn cách bằng hai dấu gạch dưới, theo sau là tên phần tử đó.
Ví dụ
<pre><code>
	.stick-man__head {

  }
	.stick-man__arms {

  }
	.stick-man__feet {

  }
</code></pre>

### M cho Modifiers (bổ nghĩa)

M trong BEM là viết tắt của Modifiers
Nếu một tên người que bị thay đổi đi một chút và chúng ta sẽ có một tên người que `xanh`, một tên người que `đỏ` thì sao? <br>
<img src="https://cdn-images-1.medium.com/max/800/1*Uj4IOaEtYynnUUJm_hAdwQ.png">
<br>
Thực tế tình huống trên sẽ giống với việc chúng ta muốn có một button `đỏ` (hoặc `xanh` cũng được). Đây chính là trường hợp chúng ta sử dụng bổ nghĩa cho các thành phần.

Sử dụng BEM, tên một class sử dụng bổ nghĩa sẽ được ngăn cách bởi hai gạch ngang, theo sau là tên phần tử.

Ví dụ:
<pre><code>
	.stick-man--blue {

  }
	.stick-man--red {

  }
</code></pre>
Ví dụ này chỉ biểu diễn cách một thành phần cha mẹ bị thay đổi. Trong thực tế không phải lúc nào chúng ta cũng chỉ làm việc với những thành phần này.

Nếu chúng ta muốn mỗi tên người que lại có kích thước `đầu` khác nhau thì sao?<br>
<img src="https://cdn-images-1.medium.com/max/800/1*qTM1TfotfLSRNjZ_PnWtAg.png">
<br>
Lần này những phần tử  (element) sẽ được thay đổi. Nhớ lại nào, những phần tử là những mảnh con nằm trong khối chứa chúng.

Một `.stick-man` đại diện cho `khối`, `.stick-man__head` là phần tử.

Giống ví dụ trên thì hai gạch ngang cũng có thể được sử dụng như sau:
<pre><code>
	<strong>.stick-man__head--smal</strong> {

  }
	<strong>.stick-man__head--big</strong> {

  }
</code></pre>
Một lần nữa hãy chú ý tới cách sử dụng hai <strong>gạch ngang</strong> trong ví dụ trên. Nó thường thể hiện cho trường hợp bổ nghĩa.

Tới lúc này có lẽ bạn đã nắm được cơ bản cách mà chuẩn đặt tên BEM hoạt động rồi đấy.

Cá nhân tôi chỉ hay sử dụng một gạch ngang giữa các tên class cho những dự án đơn giản, BEM thì thường liên quan nhiều tới các dự án hướng tới giao diện người dùng hơn.

Bạn có thể đọc thêm về BEM ở <a href="ttp://getbem.com/naming">đây</a>

### Tại sao lại sử dụng các chuẩn đặt tên?

<i>Có hai vấn đề rất khó giải quyết trong ngành khoa học máy tính: vô hiệu hóa cache và đặt tên cho mọi thứ - Phil Karlton </i>

Trong lập trình đặt tên là một việc khó khăn. Chúng ta cố gắng làm cho mọi thứ dễ dàng hơn, tiết kiệm thời gian hơn với những dòng code dễ bảo trì.

Đặt tên chuẩn trong CSS sẽ giúp code bạn dễ đọc và bảo trì hơn.

Nếu bạn chọn sử dụng chuẩn BEM, việc nhìn ra mối quan hệ giữa những thành phần trong thiết kế của bạn sẽ dễ dàng hơn, chỉ cần nhìn vào các selectors thôi là bạn đã hiểu rồi.

Bạn đã đủ tự tin chưa?

### Các tên trong CSS với Javascript Hooks*

Hôm nay là ngày làm việc đầu tiên của John.

Anh ấy được đưa cho một đoạn code `HTML` như sau:
<xmp>
	<div class="siteNavigation">
	</div>
</xmp>

John đã đọc bài viết này và nhận ra đây không phải đoạn code có tên class được đặt phù hợp trong `CSS`. Vậy nên anh ta đã thay đổi lại đoạn code như sau:
<xmp>
	<div class="site-navigation">
	</div>
</xmp>

Trông có vẻ ổn đúng không?

Tuy nhiên John không biết rằng anh ta đã phá vỡ toàn bộ codebase.

Thế quái nào vậy?

Ở đâu đó trong những dòng code Javascript, có một đoạn sử dụng tới tên class `siteNavigation`:
<pre><code>
//the Javasript code
const nav = document.querySelector('.siteNavigation')
</code></pre>
Do đó khi thay đổi tên class, biến `nav` đã bị `null`.

Buồn ghê.

Để tránh những trường hợp như này, các lập trình viên đã tìm ra những phương pháp khác nhau.

<h4>1. Dùng tên class `js-`</h4>
Một cách để tránh những lỗi như trên là dùng một tên class <strong>`js-*`</strong> để chỉ ra mối quan hệ với phần tử DOM.
Ví dụ:
<xmp>
<div class="site-navigation js-site-navigation">
</div>
</xmp>
Và trong đoạn code Javascript:
<pre><code>
//the Javasript code
const nav = document.querySelector('.js-site-navigation')
</code></pre>
Theo chuẩn đặt tên, khi nhìn thấy một tên class `js-site-navigation`, mọi người sẽ hiểu có một mối quan hệ giữa phần tử DOM đó trong đoạn code Javascript.

<h4>2. Sử dụng Rel attribute</h4>
Tôi không hay sử dụng cách này lắm, nhưng tôi đã thấy có người dùng nó.

Bạn có nhận ra đoạn code này không?
<xmp>
	<link rel="stylesheet" type="text/css" href="main.css">
</xmp>
Đơn giản thì một <strong>rel attribute</strong> định nghĩa mối quan hệ giữa các tài nguyên được liên kết tới đoạn văn bản mà nó được gọi tới.

Trong ví dụ trước với John, kĩ thuật này có thể được sử dụng như sau:
<xmp>
	<div class="site-navigation" rel="js-site-navigation">
	</div>
</xmp>
Và trong đọan code javascript:
<pre><code>
const nav = document.querySelector("[rel='js-site-navigation']")
</code></pre>

Tôi vẫn không tin tưởng vào kỹ thuật này lắm, nhưng bạn có thể sẽ tình cờ nhìn thấy nó trong vài codebase. Mấu chốt ý tưởng ở đây là, <i>”Ồ có một mối quan hệ của phần tử này với Javascript, tôi phải sử dụng rel attribute để thể hiện nó.”</i>

Web là một xứ sở rộng lớn với nhiều kĩ thuật khác nhau để giải quyết cùng một vấn đề mà.

<h4>3. Đừng dùng data attributes</h4>
Một vài lập trình viên sử dụng data attributes như một Javascript hooks. Điều này không đúng. Theo đúng định nghĩa, data attributes chỉ được dùng cho việc lưu trữ những dữ liệu tùy biến.<br>
<img src="https://cdn-images-1.medium.com/max/800/1*wYSuEHKyr4gikmoEaq-9jw.png">
<br>
<small>Các dùng data attributes tốt ở twitter</small>
### Mẹo nhỏ: Viết nhiều comments cho CSS hơn.

Việc này không liên quan gì tới chuẩn đặt tên cả, nhưng nó cũng sẽ giúp bạn tiết kiệm thời gian.

Trong khi rất nhiều lập trình viên cố gắng không viết comment cho JavaScript hoặc chỉ viết rất ít, thì trong CSS tôi nghĩ bạn nên viết nhiều comments hơn.

Vì CSS không phải “ngôn ngữ” đẹp nhất, những comments có cấu trúc tốt sẽ giúp bạn tiết kiệm nhiều thời gian hơn khi bạn phải cố hiểu nó.

Việc này không gây ảnh hưởng gì đâu.

Cứ thử đọc xem <a href="https://github.com/twbs/bootstrap/blob/v4-dev/scss/_carousel.scss">source code</a> của Bootstrap đã được comment cẩn thận thế nào đi.

Bạn không phải viết comments cho dòng `color: red` chỉ để nói rằng nó sẽ cho ra một màu đỏ. Nhưng nếu bạn viết những kĩ thuật CSS khác không được tường minh cho lắm, hãy viết comment.

### Đã sẵn sàng lên mức chuyên nghiệp chưa?

Tôi có tạo một bài hướng dẫn CSS miễn phí để giúp bạn mài giũa kĩ năng CSS của mình.
Lấy cuốn tài liệu đó ở <a href="https://ohansemmanuel.us17.list-manage.com/subscribe?u=6fa63587721dce8a5eb987a2a&id=ba27bc2a77"> đây</a>.<br>
<img src="https://cdn-images-1.medium.com/max/800/1*fJabzNuhWcJVUXa3O5OlSQ.png">
<br>
<small>7 mẹo CSS bạn chưa biết</small>
<blockquote>
tài liệu: https://medium.freecodecamp.org/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849
</blockquote>
