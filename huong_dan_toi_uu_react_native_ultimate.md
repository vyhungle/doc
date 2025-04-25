# HƯỚNG DẪN TỐI ƯU HÓA REACT NATIVE TỐI ĐA

**{callstack}**

**TỐI ƯU HÓA REACT NATIVE**
**HƯỚNG DẪN TỐI ĐA**

---

## MỤC LỤC

### Lời Giới Thiệu

- Lời Nói Đầu (Trang 4)
- Cách Đọc Sách Này (Trang 5)
- Tại Sao Hiệu Suất Quan Trọng (Trang 7)

### Phần 1: JavaScript

- Cách Phân Tích Hiệu Suất Mã JS và React (Trang 14)
- Cách Đo FPS của JS (Trang 21)
- Cách Tìm Rò Rỉ Bộ Nhớ JS (Trang 24)
- Thành Phần Không Kiểm Soát (Trang 30)
- Thành Phần Chuyên Biệt Bậc Cao (Trang 34)
- Quản Lý Trạng Thái Nguyên Tử (Trang 42)
- React Đồng Thời (Trang 46)
- Trình Biên Dịch React (Trang 52)
- Hoạt Ảnh Hiệu Suất Cao Không Bị Giật Khung Hình (Trang 59)

### Phần 2: Native

- Hiểu Sự Khác Biệt Giữa Các Nền Tảng (Trang 67)
- Cách Phân Tích Hiệu Suất Các Phần Native của React Native (Trang 76)
- Cách Đo TTI (Trang 85)
- Hiểu Quản Lý Bộ Nhớ Native (Trang 93)
- Hiểu Mô Hình Luồng của Turbo Modules và Fabric (Trang 105)
- Sử Dụng Làm Phẳng Giao Diện (Trang 113)
- Sử Dụng SDK React Native Chuyên Dụng Thay Vì Web (Trang 117)
- Làm Cho Các Mô-đun Native Nhanh Hơn (Trang 122)
- Cách Tìm Rò Rỉ Bộ Nhớ (Trang 130)

### Phần 3: Gói Ứng Dụng

- Cách Phân Tích Kích Thước Gói JS (Trang 142)
- Cách Phân Tích Kích Thước Gói Ứng Dụng (Trang 148)
- Xác Định Kích Thước Thực Sự của Thư Viện Bên Thứ Ba (Trang 154)
- Tránh Xuất Barrel (Trang 156)
- Thử Nghiệm Với Tree Shaking (Trang 159)
- Tải Mã Từ Xa Khi Cần (Trang 163)
- Thu Nhỏ Mã Với R8 Android (Trang 167)
- Sử Dụng Thư Mục Tài Nguyên Native (Trang 170)
- Tắt Nén Gói JS (Trang 175)

### Lời Cảm Ơn

- Về Các Tác Giả (Trang 177)
- Các Thư Viện và Công Cụ Được Đề Cập Trong Hướng Dẫn Này (Trang 179)

---

## LỜI NÓI ĐẦU

React Native đã trải qua một hành trình dài. Từ những ngày đầu như một thử nghiệm đầy triển vọng trong phát triển đa nền tảng đến việc được các doanh nghiệp lớn nhất thế giới áp dụng, sự phát triển của nó thật sự đáng chú ý. Khung công tác này đã trưởng thành, chứng minh khả năng xử lý các yêu cầu của các ứng dụng quy mô lớn trong khi tiếp tục tinh chỉnh và mở rộng giới hạn kỹ thuật của mình.

Trong nhiều năm, chúng ta đã chứng kiến React Native giới thiệu các tính năng mới, thường là đột phá, với mỗi phiên bản phát hành. Ngày nay, chúng ta thấy những cải tiến cấp thấp ổn định, thường nâng cao hiệu suất, độ ổn định và khả năng mở rộng. Những cải tiến này phản ánh việc React Native đang được áp dụng rộng rãi hơn, củng cố vai trò của nó như một khung công tác trưởng thành và sẵn sàng cho doanh nghiệp.

Một cột mốc quan trọng trong hành trình này là sự ra đời của Kiến Trúc Mới, đã định nghĩa lại nhiều khía cạnh cốt lõi của khung, bao gồm cách chúng ta nghĩ về phát triển nói chung và tối ưu hóa hiệu suất. Nó mang lại các tính năng và thực tiễn tốt nhất mới, giúp các nhà phát triển xây dựng các ứng dụng hiệu quả và mở rộng hơn.

Vì vậy, chúng tôi quyết định đại tu hoàn toàn hướng dẫn tối ưu hóa của mình. Bối cảnh đã thay đổi, và cách tiếp cận của chúng tôi cũng phải thay đổi. Một số kỹ thuật từng là thiết yếu nay không còn phù hợp; những kỹ thuật khác đã trở nên quan trọng hơn. Trong phiên bản mới này, chúng tôi mong muốn trang bị cho các nhà phát triển những hiểu biết, công cụ và chiến lược mới nhất để tận dụng tối đa khả năng đang phát triển của React Native.

Dù bạn là một kỹ sư React Native dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn này không chỉ cung cấp các thực tiễn tốt nhất về hiệu suất mà còn cung cấp kiến thức thiết yếu để giúp bạn hiểu React Native nói chung, bao gồm những gì diễn ra bên dưới. Chúng tôi dựa vào kiến thức này hàng ngày để xây dựng các ứng dụng tốt hơn, hiệu quả hơn và có khả năng mở rộng, và chúng tôi hy vọng nó sẽ giúp bạn làm điều tương tự.

- **Mike Grabowski**, Nhà sáng lập & CTO của Callstack

---

## CÁCH ĐỌC SÁCH NÀY

Cuốn sách này dành cho các nhà phát triển React Native ở nhiều cấp độ kinh nghiệm khác nhau. Chúng tôi tin rằng cả những người mới bắt đầu và các nhà phát triển React Native dày dạn kinh nghiệm, bất kể họ đến từ nền tảng phát triển ứng dụng web hay native, đều sẽ tìm thấy điều gì đó có giá trị và áp dụng được trong ứng dụng của họ.

Chúng tôi thừa nhận rằng tại một thời điểm nhất định, bạn có thể không quan tâm đến tất cả các tối ưu hóa được trình bày trong cuốn sách này. Thường thì, bạn sẽ tập trung vào một lĩnh vực cụ thể, chẳng hạn như tối ưu hóa việc render lại của React. Vì vậy, mặc dù bạn có thể đọc toàn bộ cuốn sách theo trình tự, chúng tôi đã đảm bảo rằng bạn có thể dễ dàng mở bất kỳ chương nào và đi thẳng vào chủ đề bạn quan tâm.

### Có gì đang chờ bạn bên trong?
Để mọi người dễ dàng tìm thấy thông tin liên quan, chúng tôi đã chia hướng dẫn này thành ba phần tập trung vào các loại tối ưu hóa khác nhau mà bạn có thể đặc biệt quan tâm: phía React, phía Native, và các tối ưu hóa thời gian xây dựng tổng thể. Cả ba phần đều chứa phần giới thiệu về chủ đề chính, các hướng dẫn chi tiết, và các thực tiễn tốt nhất để giúp bạn cải thiện các chỉ số quan trọng nhất mô tả hiệu suất ứng dụng của bạn: FPS (Khung Hình Mỗi Giây) và TTI (Thời Gian Tương Tác).

Dưới đây là những gì bạn có thể mong đợi ở mỗi phần:

- **Giới thiệu** - nơi chúng tôi trình bày các chủ đề, thuật ngữ và ý tưởng chính liên quan đến chủ đề chính.
- **Hướng dẫn** - nơi chúng tôi giải thích cách sử dụng các công cụ chuyên biệt và đo lường các chỉ số quan trọng.
- **Thực tiễn tốt nhất** - nơi chúng tôi chỉ cho bạn cách làm để ứng dụng của bạn chạy và khởi tạo nhanh hơn.

---

## TẠI SAO HIỆU SUẤT QUAN TRỌNG

Khi xây dựng các ứng dụng di động, hiệu suất không chỉ là một vấn đề kỹ thuật - mà còn là ưu tiên trải nghiệm người dùng. Một ứng dụng nhanh, phản hồi tốt có thể tạo ra sự khác biệt giữa một người dùng hài lòng và một người bỏ rơi ứng dụng của bạn hoàn toàn. Nhưng "nhanh" thực sự có nghĩa là gì? Đó là về các con số thô hay cảm nhận của người dùng?

### Góc nhìn của người dùng
Hiệu suất cảm nhận là tất cả về việc ứng dụng của bạn cảm thấy nhanh như thế nào đối với người dùng. Nó không chỉ là về các con số hay điểm chuẩn - mà là tạo ra ảo giác về tốc độ.

Vào những năm 1940, một tòa nhà văn phòng ở New York nhận được khiếu nại về thang máy chậm. Để giải quyết vấn đề này, thay vì tăng tốc độ thang máy, người quản lý tòa nhà đã lắp đặt gương gần thang máy. Sự thay đổi đơn giản này làm người dùng mất tập trung bằng cách cho họ việc gì đó để làm (nhìn vào chính mình), giảm thời gian chờ cảm nhận, và giải quyết vấn đề một cách hiệu quả. Mặc dù câu chuyện này có thể chỉ là một truyền thuyết đô thị, khái niệm này dựa trên các nguyên tắc tâm lý hợp lệ về thời gian cảm nhận và sự phân tâm, ảnh hưởng đến cảm giác về tốc độ của một sự kiện cụ thể.

Khi một ứng dụng di động mất vài giây để tải, việc hiển thị một màn hình khởi động, giao diện khung (skeleton UI), hoặc thậm chí một trò chơi nhỏ có thể khiến người dùng cảm thấy ứng dụng phản hồi nhanh và sẵn sàng sử dụng. Đó là lý do tại sao hiệu suất cảm nhận thường quan trọng hơn hiệu suất thực tế trong việc định hình sự hài lòng của người dùng.

Tuy nhiên, chỉ tập trung vào hiệu suất cảm nhận có thể gây hiểu lầm. Mặc dù các thủ thuật như hoạt ảnh, giao diện giữ chỗ, hoặc tải trước nội dung có thể cải thiện cảm nhận của người dùng, chúng không giải quyết các vấn đề hiệu suất cơ bản. Đó là lúc các chỉ số đo lường được như TTI và FPS thể hiện giá trị của chúng.

### Các chỉ số quan trọng: TTI và FPS
Trong số nhiều chỉ số bạn có thể đo lường và theo dõi, hai chỉ số có tác động lớn nhất đến cách người dùng cảm nhận tốc độ của ứng dụng. Đó là tốc độ mà họ có thể tương tác với ứng dụng, được mô tả bởi TTI, và cảm giác mượt mà của ứng dụng khi tương tác, được mô tả bởi FPS tại một thời điểm nhất định.

#### Thời Gian Tương Tác (TTI)
Việc đo lường hiệu suất khởi động của ứng dụng được mô tả bởi chỉ số TTI. Nó đo lường thời gian mà ứng dụng của bạn trở nên có thể sử dụng được sau khi khởi chạy. Đây là khoảnh khắc mà người dùng có thể bắt đầu tương tác với ứng dụng mà không gặp độ trễ hoặc giật. Nhưng TTI không chỉ là về tải ban đầu của ứng dụng. Các công ty thường theo dõi các biến thể của chỉ số này, chẳng hạn như Thời Gian Tới Màn Hình Chính (thời gian để tải màn hình chính) hoặc Thời Gian Tới Màn Hình Cụ Thể (thời gian để điều hướng đến một tính năng chính). Các chỉ số này đặc biệt quan trọng đối với các ứng dụng có luồng điều hướng phức tạp hoặc tải dữ liệu ban đầu nặng.

Nếu ứng dụng của bạn mất quá nhiều thời gian để tải, người dùng có thể bỏ rơi nó trước khi họ có cơ hội khám phá các tính năng hoặc cảm thấy khó chịu vì nó chậm mỗi khi họ cố gắng làm điều gì đó, khiến họ cảm thấy không thoải mái và bắt đầu liên kết ứng dụng của bạn, đôi khi cả thương hiệu của nó, với cảm giác đó.

#### Khung Hình Mỗi Giây (FPS)
Khi ứng dụng của bạn đã khởi động và chạy, FPS trở thành chỉ số chính cho hiệu suất thời gian chạy. FPS đo lường mức độ mượt mà mà ứng dụng của bạn phản hồi các tương tác của người dùng, chẳng hạn như cuộn, vuốt, hoặc nhấn vào các nút. FPS cao (lý tưởng là 60 khung hình mỗi giây hoặc hơn) đảm bảo rằng các hoạt ảnh và chuyển đổi cảm thấy mượt mà và tự nhiên. Khi FPS giảm, trải nghiệm người dùng bị lag, và các hoạt ảnh bắt đầu bị giật, khiến ứng dụng của bạn cảm thấy không được trau chuốt hoặc phản hồi chậm. Điều này đặc biệt quan trọng đối với các ứng dụng có nội dung hình ảnh phong phú hoặc các tương tác phức tạp.

#### Nhanh thực sự là gì?
Dù chúng ta yêu thích dữ liệu và cách tiếp cận khoa học để xác nhận các giả thuyết của mình, chúng tôi nhận ra rằng có rất ít nghiên cứu độc lập và chất lượng cao về việc "nhanh" có ý nghĩa gì đối với người dùng di động. Thông thường, đó là các công ty công nghệ lớn khoe khoang về số liệu chuyển đổi của họ hoặc các báo cáo trả phí dựa trên khảo sát.

Tuy nhiên, điều quan trọng hơn là cảm giác về tốc độ là một mục tiêu di động. Với việc tiếp cận các thiết bị cao cấp và hoạt động tốt hơn, trong khi sử dụng nhiều ứng dụng khác nhau trên một chiếc điện thoại thông minh, kỳ vọng của người dùng ngày càng cao. Cũng cần nhớ rằng những kỳ vọng này phụ thuộc rất nhiều vào nhân khẩu học - ví dụ, các thế hệ trẻ thường mong đợi ứng dụng tải và hoạt động nhanh hơn so với cha mẹ và ông bà của họ, những người đã quen với việc mọi thứ mất nhiều thời gian hơn. Kỳ vọng và động lực để cải thiện cũng khác nhau đối với người dùng ứng dụng doanh nghiệp nội bộ so với khách hàng cá nhân.

Điều thường sẽ cung cấp cho bạn chỉ báo đáng tin cậy nhất về việc ứng dụng của bạn có đủ nhanh hay không là hiểu người dùng của bạn và đối thủ cạnh tranh của bạn. Các phân tích bạn thu thập về hành vi của người dùng sẽ cung cấp cho bạn những hiểu biết cá nhân hóa về những nơi họ có xu hướng rời bỏ. Việc phân tích xem ứng dụng của đối thủ cạnh tranh có nhanh hơn hay chậm hơn một cách khách quan, mặt khác, sẽ gợi ý liệu hiệu suất có thể là lý do bạn đang mất người dùng hay không.

Trong hai phần đầu của cuốn sách này, chúng tôi sẽ tập trung vào cách bạn có thể cải thiện hiệu suất thời gian chạy thông qua các tối ưu hóa JavaScript, React, và native. Chúng tôi sẽ hướng dẫn bạn qua tất cả các công cụ và kỹ thuật cần thiết mà bạn có thể sử dụng để hiểu rõ hơn những gì ảnh hưởng đến FPS để bạn có thể sửa chữa nó ở bất kỳ đâu.

---

## PHẦN 1: JAVASCRIPT

### Giới Thiệu

Trong phần đầu tiên của hướng dẫn này, chúng tôi sẽ tập trung vào phần JavaScript của hệ sinh thái React Native. Như bạn có lẽ đã nhận ra, React Native tận dụng các nguyên tố nền tảng native và gắn kết nhiều công nghệ khác nhau: Kotlin hoặc Java cho Android, Swift hoặc Objective-C cho iOS, C++ cho lõi thời gian chạy của React Native, và JavaScript được thực thi bởi động cơ Hermes. Đó là rất nhiều thứ để tiếp nhận, vì vậy hãy phân tích một chút và tập trung vào một nền tảng để đơn giản hóa: Android.

Khi người dùng mở một ứng dụng Android native, nó thường đi qua một lộ trình khởi tạo tương tự: ứng dụng mở trên luồng chính, nó tải mã native - thường được viết bằng Kotlin, Java, hoặc C++ - vào bộ nhớ, và sau đó thực thi mã này, thường dẫn đến việc hiển thị một số loại giao diện người dùng cho người dùng. Điều này không khác nhiều đối với một ứng dụng Android được tạo bằng React Native. Sau tất cả, đó là một ứng dụng native nhưng với một sự thay đổi: một phần của mã native được thực thi đến từ React Native.

#### Lộ trình khởi tạo JavaScript
- **Luồng UI**: Khởi tạo native (chi tiết trong Phần 2), khởi tạo mô-đun native, xử lý sự kiện.
- **Luồng JS**: Khởi tạo, đăng ký, thực thi, render thành phần.

Lưu ý cách logic render (Kotlin, C++) và cái gọi là "logic kinh doanh" được thiết kế để chạy trên các luồng riêng biệt - luồng chính so với luồng JS. Vì phần này tập trung vào JavaScript và React, chúng tôi sẽ tập trung vào phía JavaScript, cho phép React chạy trên một luồng JS chuyên dụng và cách mô hình này ảnh hưởng đến hiệu suất của các ứng dụng React Native của bạn.

Theo một cuộc khảo sát nội bộ của 100 nhà phát triển React Native tại Callstack, 80% các thách thức hiệu suất mà họ gặp phải trong các ứng dụng React Native trên di động, TV, và máy tính để bàn bắt nguồn từ phía JavaScript. Mẫu này có thể không đại diện cho thế giới thực do kích thước nhỏ của nó. Tuy nhiên, nhìn vào những gì cộng đồng React Native đang vật lộn, có thể giả định một cách an toàn rằng hầu hết các vấn đề hiệu suất liên quan đến JavaScript. Do đó, việc tập trung vào những vấn đề này trước khi chuyển sang các tối ưu hóa native nâng cao được mô tả trong Phần 2: Native là điều khôn ngoan.

#### Mô hình render lại của React
React chịu trách nhiệm render và cập nhật giao diện người dùng của ứng dụng dựa trên trạng thái của nó cho bạn, bất kể môi trường (hoặc nền tảng): web, iOS, Android, hoặc bất kỳ thứ gì khác. Thư viện react tự nó rất nhỏ và chủ yếu bao gồm các định nghĩa API công khai, một số chức năng đa nền tảng, và một thuật toán hòa giải, chịu trách nhiệm cập nhật giao diện người dùng một cách hiệu quả để phản ánh các thay đổi trạng thái thành phần, mô tả một cách hiệu quả "phải làm gì".

Điều làm cho mô hình này mạnh mẽ là việc tách biệt "cái gì" khỏi "cách làm" và trì hoãn cái sau cho các trình render chuyên biệt, quản lý cách các cập nhật này được áp dụng cho các môi trường khác nhau: **react-dom** cho web, **react-native** cho iOS và Android, hoặc **react-native-windows** cho Windows, để kể tên một vài. Mô hình này cho phép bạn định nghĩa các thành phần của ứng dụng một cách thống nhất cho tất cả các nền tảng được hỗ trợ đồng thời, và tạo ra giao diện cuối cùng từ những khối xây dựng nhỏ hơn này. Với cách tiếp cận như vậy, bạn không kiểm soát vòng đời render của ứng dụng; React và trình render của nó làm việc đó cho bạn.

#### DOM ảo
Mô tả trực quan về thuật toán hòa giải của React.

Nói cách khác, việc quyết định khi nào cần vẽ lại các thứ trên màn hình là trách nhiệm thuần túy của React, trong khi quyết định về "cách làm" là trách nhiệm của trình render. React theo dõi các thay đổi bạn đã thực hiện đối với các thành phần của mình, so sánh chúng, và theo thiết kế, chỉ thực hiện số lượng cập nhật thực tế cần thiết và nhỏ nhất.

React render lại thành phần trong các trường hợp sau:

- Thành phần cha render lại.
- Trạng thái (bao gồm hooks) thay đổi.
- Props thay đổi.
- Context thay đổi.
- Buộc cập nhật (lối thoát khẩn cấp).

Trước khi chúng ta chuyển sang các thực tiễn có thể hoặc không liên quan đến trường hợp sử dụng cụ thể của ứng dụng của bạn, hãy bắt đầu với một thứ mà bạn sẽ thấy hữu ích trong mọi ứng dụng bạn xây dựng: phân tích và đo lường hiệu suất.

---

### HƯỚNG DẪN: CÁCH PHÂN TÍCH HIỆU SUẤT MÃ JS VÀ REACT

Khi tối ưu hóa hiệu suất, chúng ta muốn biết chính xác đoạn mã nào là nguồn gốc của sự chậm trễ. Với một số kinh nghiệm và kiến thức về mã nguồn và các cạm bẫy hiệu suất phổ biến, các nhà phát triển thường có thể xác định vấn đề một cách trực giác và kỳ vọng ứng dụng sẽ chạy nhanh hơn. Tuy nhiên, trong thực tế, các ứng dụng thường quá phức tạp để bất kỳ ai có thể hiểu toàn bộ hệ thống một cách chi tiết. Các tối ưu hóa mù quáng mà chúng ta thực hiện thường có ít tác động đến hiệu suất tổng thể. Để chính xác trong hành động của mình, chúng ta phải đưa ra quyết định dựa trên dữ liệu.

Dữ liệu đến từ việc đo lường hiệu suất bằng các công cụ chuyên biệt. Quá trình này thường được gọi là "phân tích hiệu suất" (profiling), vì nó liên quan đến việc phân tích một chương trình để tạo ra một "hồ sơ" về quá trình thực thi của nó. Hồ sơ này thường bao gồm thông tin về các phần của chương trình tiêu thụ nhiều tài nguyên nhất, chẳng hạn như thời gian CPU hoặc bộ nhớ, giúp xác định các nút thắt hiệu suất.

#### Phân tích hiệu suất với React Native DevTools
Trong bối cảnh của một ứng dụng React Native, việc có thể phân tích chính React để kiểm tra các lần render lại không cần thiết là rất hữu ích. Công cụ tốt nhất để phân tích hiệu suất React chạy trong một ứng dụng di động là **React Native DevTools**, và đó là thứ chúng tôi sẽ tập trung trong hướng dẫn này.

**React Profiler** được tích hợp như một plugin mặc định trong React Native DevTools và có thể tạo ra một biểu đồ flame graph của quy trình render React như là kết quả của việc phân tích hiệu suất. Chúng ta có thể tận dụng dữ liệu này để phân tích các vấn đề render lại của ứng dụng.

Dưới đây là đoạn mã chúng ta sẽ phân tích:

```javascript
export const App = () => {
  const [count, setCount] = React.useState(0);
  const [second, setSecond] = React.useState(0);
  return (
    <View style={styles.container}>
      <Text>Chào mừng!</Text>
      <Text>{count}</Text>
      <Text>{second}</Text>
      <Button onPress={() => setCount(count + 1)} title="Nhấn một" />
      <Button onPress={() => setSecond(second + 1)} title="Nhấn hai" />
    </View>
  );
};

const Button = ({ onPress, title }) => {
  return (
    <Pressable style={styles.button} onPress={onPress}>
      <Text>{title}</Text>
    </Pressable>
  );
};
```

Khi được render, thành phần `<App />` sẽ hiển thị một thông điệp chào mừng với hai bộ đếm và các nút được điều khiển bởi hai trình xử lý trạng thái riêng biệt. Bây giờ chúng ta sẵn sàng để phân tích mã React này với **React Native DevTools**.

Bạn có thể truy cập nó bằng cách nhấn `j` trong máy chủ phát triển Metro hoặc từ ứng dụng bằng **React Native Dev Menu** – được truy cập thông qua cử chỉ lắc trên thiết bị, `Cmd+M` trên Android hoặc `Cmd+D` trên iOS – và nhấn "Mở DevTools". Nó sẽ hiển thị một màn hình chào mừng, hướng dẫn đến các tài nguyên học tập về các kiến thức cơ bản gỡ lỗi, các tính năng của DevTools, và gỡ lỗi native. Chúng tôi khuyên bạn nên làm quen với các tài nguyên này, một số trong đó trùng lặp với các tài liệu được trình bày trong hướng dẫn này.

#### Sử dụng React Native DevTools
Mở **React Native DevTools**. Chuyển đến tab **Profiler** ở trên cùng. Nhấn nút "bánh răng" để cấu hình nó thành "Làm nổi bật các cập nhật khi thành phần render" và "Ghi lại lý do mỗi thành phần render trong khi phân tích hiệu suất".

Cuối cùng, nhấn nút "Bắt đầu phân tích" hoặc "Tải lại và bắt đầu phân tích" ở góc trên bên trái của màn hình để bắt đầu phân tích. Trong trường hợp sử dụng của chúng ta, điều này không quan trọng vì chúng ta đang kiểm tra phản ứng với đầu vào của người dùng. Tuy nhiên, khi phân tích khởi động ứng dụng, "Tải lại và bắt đầu phân tích" là một công cụ cứu cánh.

Trong ứng dụng mẫu của chúng ta, nhấp vào cả hai nút vài lần và quan sát phản hồi thời gian thực từ DevTools làm nổi bật các thành phần đang được render lại. Các ảnh chụp màn hình phản ánh một hồ sơ được tạo ra bằng cách nhấn "Nhấn một" hai lần và sau đó "Nhấn hai" hai lần, tạo ra bốn "commit" liên tiếp bởi trình render React.

Bạn có thể tìm hiểu thêm về quy trình render và commit của React trong tài liệu chính thức.

#### Phân tích biểu đồ Flame Graph
Nhấn vào thành phần màu xanh trên biểu đồ flame graph để "phóng to" vào các thành phần con của nó. Đây là một mô hình UX thiết yếu được triển khai bởi Profiler, và hy vọng bạn sẽ sớm học cách tận hưởng nó. Trong trường hợp này, bạn sẽ nhận thấy rằng cả hai nút đều được render trong mỗi commit, điều này có vẻ dư thừa vì không có props nào thay đổi. Nhưng thực sự có phải vậy không?

Để có một góc nhìn khác về tình huống, chúng ta có thể truy cập chế độ xem **Ranked**, hiển thị các thành phần từ chậm nhất (màu vàng) đến nhanh nhất (màu xanh). Nó khá giống với chế độ xem "Bottom-up" mà bạn có thể biết từ các công cụ phân tích khác, như Chrome DevTools hoặc các trình phân tích native.

Trong mỗi chế độ xem, chúng ta có thể thấy rằng một thành phần Button được render hai lần, điều này phản ánh hai nút của chúng ta được render lại với mỗi cập nhật trạng thái.

Nhìn vào mã của chúng ta, điều này là điều được mong đợi - trừ khi chúng ta sử dụng **React Compiler**, điều này sẽ tự động memoize mã để tạo ra ít render lại hơn. Vì vậy, hãy memoize nó bằng tay:

```javascript
// Bao bọc các hàm nội tuyến với 'useCallback'
const onPressHandler = React.useCallback(() => setCount(count + 1), [count]);
const secondHandler = React.useCallback(() => setSecond(second + 1), [second]);

// Bao bọc thành phần Button với 'memo'
const Button = React.memo(({ onPress, title }) => {
  return (
    <Pressable style={styles.button} onPress={onPress}>
      <Text>{title}</Text>
    </Pressable>
  );
});

// Sử dụng trong App
<Button onPress={onPressHandler} title="Nhấn một" />
<Button onPress={secondHandler} title="Nhấn hai" />
```

Sau khi bao bọc **Button** với **React.memo** và các trình xử lý **onPress** với **React.useCallback**, chúng ta nhận được một bức tranh khác từ trình phân tích, hiển thị cùng số lượng 4 commit của React. Tuy nhiên, bây giờ, chỉ nút thực sự được nhấn mới được render lại, trong khi nút kia được memoized (với tên tự động sinh `_c2`), được chỉ định bởi màu xanh của thành phần này và các thành phần con của nó.

Bây giờ, bạn đã được trang bị tốt để bắt đầu cuộc phiêu lưu phân tích bất kỳ ứng dụng React nào - dù là ứng dụng web hay di động. Chúng tôi khuyên bạn nên tạm dừng đọc ngay bây giờ và thử nó trong các ứng dụng bạn phát triển hàng ngày. Bạn sẽ nhận thấy đầu ra biểu đồ flame graph sẽ ồn ào hơn nhiều do độ phức tạp lớn hơn của ứng dụng React của bạn.

Hãy nhớ tập trung vào các thành phần được đánh dấu màu vàng là những nơi React dành nhiều thời gian nhất. Và tận dụng thông tin "Tại sao thành phần này render lại?".

---

### HƯỚNG DẪN: CÁCH ĐO FPS CỦA JS

Khung Hình Mỗi Giây (FPS) là một chỉ số quan trọng để đánh giá mức độ mượt mà của ứng dụng React Native, đặc biệt khi người dùng tương tác với giao diện như cuộn, nhấn nút, hoặc chạy hoạt ảnh. Trong React Native, FPS thường bị ảnh hưởng bởi hiệu suất của luồng JavaScript (JS), nơi xử lý logic kinh doanh và render của React. Việc đo FPS giúp bạn xác định các điểm nghẽn trong mã JS và cải thiện trải nghiệm người dùng.

#### Tại sao cần đo FPS?
FPS thấp (dưới 60 khung hình mỗi giây) có thể dẫn đến giao diện bị giật, làm giảm trải nghiệm người dùng. Các nguyên nhân phổ biến bao gồm:
- Các hàm JS nặng (ví dụ: vòng lặp phức tạp, xử lý dữ liệu lớn).
- Render lại không cần thiết trong React.
- Tương tác chậm giữa luồng JS và luồng native.

#### Công cụ đo FPS
React Native cung cấp các công cụ tích hợp và bên thứ ba để đo FPS:
- **React Native DevTools**: Hiển thị FPS thời gian thực trong tab Performance.
- **Flipper**: Một công cụ gỡ lỗi mạnh mẽ với plugin Performance để theo dõi FPS.
- **Thư viện bên thứ ba**: Ví dụ, `react-native-fps-meter` để hiển thị FPS trực tiếp trên giao diện.

#### Hướng dẫn đo FPS với Flipper
1. **Cài đặt Flipper**:
   - Tải Flipper từ [trang chính thức](https://fbflipper.com/) và cài đặt.
   - Thêm plugin `react-native-performance` vào Flipper:
     ```bash
     npm install --save-dev react-native-flipper
     ```
   - Liên kết Flipper với ứng dụng React Native của bạn bằng cách thêm mã sau vào `index.js`:
     ```javascript
     import { Flipper } from 'react-native-flipper';
     if (__DEV__) {
       Flipper.initialize();
     }
     ```

2. **Kích hoạt plugin Performance**:
   - Mở Flipper, chọn ứng dụng React Native của bạn.
   - Trong tab Plugins, bật plugin **Performance**.
   - Chuyển sang tab **FPS** để xem biểu đồ FPS thời gian thực.

3. **Thực hiện kiểm tra**:
   - Chạy ứng dụng trên thiết bị hoặc trình giả lập.
   - Thực hiện các hành động như cuộn danh sách, nhấn nút, hoặc chạy hoạt ảnh.
   - Quan sát biểu đồ FPS trong Flipper. FPS lý tưởng là 60; nếu dưới 30, bạn cần tối ưu hóa.

4. **Phân tích kết quả**:
   - Nếu FPS giảm trong một hành động cụ thể (ví dụ: cuộn danh sách), kiểm tra mã JS liên quan.
   - Sử dụng **React Profiler** (như đã đề cập ở chương trước) để tìm các lần render lại không cần thiết.
   - Kiểm tra các hàm JS nặng bằng cách thêm console.time:
     ```javascript
     console.time('heavyFunction');
     heavyFunction();
     console.timeEnd('heavyFunction');
     ```

#### Thực tiễn tốt nhất để cải thiện FPS
- **Tránh vòng lặp phức tạp**: Di chuyển các phép tính nặng sang Web Workers hoặc mô-đun native.
- **Sử dụng memoization**: Áp dụng `React.memo`, `useMemo`, và `useCallback` để giảm render lại.
- **Tối ưu hóa danh sách**: Sử dụng `FlatList` thay vì `ScrollView` cho danh sách dài, và bật `removeClippedSubviews`:
  ```javascript
  <FlatList
    data={data}
    renderItem={renderItem}
    removeClippedSubviews={true}
  />
  ```

---

### HƯỚNG DẪN: CÁCH TÌM RÒ RỈ BỘ NHỚ JS

Rò rỉ bộ nhớ xảy ra khi ứng dụng giữ lại các tham chiếu đến các đối tượng không còn cần thiết, khiến bộ nhớ không được giải phóng. Trong React Native, rò rỉ bộ nhớ JS có thể làm chậm ứng dụng hoặc gây crash, đặc biệt trên các thiết bị có bộ nhớ thấp.

#### Dấu hiệu của rò rỉ bộ nhớ
- Ứng dụng chậm dần theo thời gian.
- Crash do hết bộ nhớ (OOM - Out of Memory).
- Bộ nhớ heap JS tăng liên tục trong các công cụ phân tích.

#### Công cụ tìm rò rỉ bộ nhớ
- **Flipper (Memory Plugin)**: Theo dõi heap JS và phát hiện các đối tượng không được thu gom.
- **Chrome DevTools**: Kết nối với Hermes để phân tích heap snapshots.
- **React Native DevTools**: Kiểm tra các thành phần không được unmount đúng cách.

#### Hướng dẫn sử dụng Flipper để tìm rò rỉ
1. **Cài đặt plugin Memory**:
   - Trong Flipper, cài đặt plugin **Memory** từ Plugin Manager.
   - Đảm bảo ứng dụng của bạn đã tích hợp Flipper (xem hướng dẫn ở trên).

2. **Chụp heap snapshot**:
   - Mở Flipper, chọn tab **Memory**.
   - Nhấn "Take Heap Snapshot" để chụp ảnh trạng thái bộ nhớ hiện tại.
   - Thực hiện một số hành động trong ứng dụng (ví dụ: điều hướng qua lại giữa các màn hình).
   - Chụp một snapshot khác để so sánh.

3. **Phân tích snapshot**:
   - So sánh hai snapshot để tìm các đối tượng tăng lên bất thường (ví dụ: các instance của thành phần hoặc đối tượng dữ liệu).
   - Kiểm tra các tham chiếu giữ lại đối tượng (retaining references) trong Flipper.
   - Các nguyên nhân phổ biến bao gồm:
     - **Subscriptions không được hủy**: Ví dụ, `setInterval` hoặc sự kiện listeners.
     - **Thành phần không unmount**: Thành phần giữ trạng thái hoặc tham chiếu đến DOM.

4. **Khắc phục rò rỉ**:
   - Hủy subscriptions trong `useEffect`:
     ```javascript
     useEffect(() => {
       const timer = setInterval(() => console.log('Tick'), 1000);
       return () => clearInterval(timer);
     }, []);
     ```
   - Đảm bảo thành phần được unmount đúng cách bằng cách kiểm tra vòng đời trong React Profiler.
   - Sử dụng công cụ như `why-did-you-render` để phát hiện các render không cần thiết:
     ```bash
     npm install @welldone-software/why-did-you-render
     ```

#### Thực tiễn tốt nhất
- Luôn hủy các subscriptions và listeners trong `useEffect`.
- Sử dụng `React.memo` để tránh tạo lại các đối tượng lớn không cần thiết.
- Theo dõi bộ nhớ định kỳ trên thiết bị thực tế, đặc biệt là các thiết bị cấp thấp.

---

### THỰC TIỄN TỐT NHẤT: THÀNH PHẦN KHÔNG KIỂM SOÁT

Thành phần không kiểm soát (uncontrolled components) là các thành phần React không dựa vào trạng thái (state) để quản lý giá trị của chúng, mà thay vào đó sử dụng tham chiếu (refs) hoặc giá trị DOM trực tiếp. Chúng hữu ích trong việc giảm render lại và cải thiện hiệu suất, đặc biệt trong các biểu mẫu lớn.

#### Tại sao sử dụng thành phần không kiểm soát?
- **Giảm render lại**: Không cần cập nhật trạng thái mỗi khi người dùng nhập.
- **Hiệu suất tốt hơn**: Đặc biệt trong các biểu mẫu với nhiều trường nhập liệu.
- **Đơn giản hóa mã**: Trong các trường hợp không cần đồng bộ hóa trạng thái liên tục.

#### Ví dụ thành phần không kiểm soát
Dưới đây là một biểu mẫu sử dụng `useRef` thay vì `useState`:

```javascript
import React, { useRef } from 'react';
import { View, TextInput, Button } from 'react-native';

const UncontrolledForm = () => {
  const nameRef = useRef(null);
  const emailRef = useRef(null);

  const handleSubmit = () => {
    console.log({
      name: nameRef.current?.value,
      email: emailRef.current?.value,
    });
  };

  return (
    <View>
      <TextInput
        ref={nameRef}
        placeholder="Tên"
        style={{ height: 40, borderColor: 'gray', borderWidth: 1 }}
      />
      <TextInput
        ref={emailRef}
        placeholder="Email"
        style={{ height: 40, borderColor: 'gray', borderWidth: 1 }}
      />
      <Button title="Gửi" onPress={handleSubmit} />
    </View>
  );
};

export default UncontrolledForm;
```

#### Khi nào nên sử dụng?
- Biểu mẫu đơn giản, không cần xác thực thời gian thực.
- Các trường nhập liệu không cần đồng bộ hóa với trạng thái khác.
- Ứng dụng ưu tiên hiệu suất hơn tính năng phức tạp.

#### Hạn chế
- Không phù hợp với biểu mẫu cần xác thực ngay lập tức.
- Khó tích hợp với các thư viện quản lý biểu mẫu như Formik hoặc React Hook Form.

---

### THỰC TIỄN TỐT NHẤT: THÀNH PHẦN CHUYÊN BIỆT BẬC CAO

Thành phần chuyên biệt bậc cao (Higher-Order Components - HOCs) là một mẫu thiết kế trong React để tái sử dụng logic giữa các thành phần. Trong React Native, HOCs có thể cải thiện hiệu suất bằng cách tách logic phức tạp ra khỏi thành phần render.

#### Ví dụ HOC
Dưới đây là một HOC để theo dõi thời gian render của một thành phần:

```javascript
import React from 'react';

const withRenderTime = (WrappedComponent) => {
  return (props) => {
    const start = performance.now();
    console.log(`Bắt đầu render ${WrappedComponent.name}`);
    
    return (
      <>
        <WrappedComponent {...props} />
        {console.log(
          `Kết thúc render ${WrappedComponent.name}: ${
            performance.now() - start
          }ms`
        )}
      </>
    );
  };
};

// Sử dụng HOC
const MyComponent = ({ text }) => <Text>{text}</Text>;
const EnhancedComponent = withRenderTime(MyComponent);

// Trong App
<EnhancedComponent text="Chào thế giới" />;
```

#### Lợi ích của HOCs
- **Tái sử dụng logic**: Ví dụ, thêm phân tích, xác thực, hoặc xử lý lỗi.
- **Tách biệt mối quan tâm**: Giữ thành phần UI sạch sẽ, tập trung vào giao diện.
- **Cải thiện hiệu suất**: Bằng cách áp dụng memoization hoặc logic tối ưu hóa trong HOC.

#### Thực tiễn tốt nhất
- Kết hợp HOCs với `React.memo` để tránh render lại không cần thiết.
- Tránh lạm dụng HOCs, vì chúng có thể làm tăng độ phức tạp của mã.
- Sử dụng các thư viện như `recompose` để tạo HOCs dễ dàng hơn.

---

### QUẢN LÝ TRẠNG THÁI NGUYÊN TỬ

Quản lý trạng thái nguyên tử (atomic state management) là cách tiếp cận sử dụng các trạng thái nhỏ, độc lập thay vì một trạng thái lớn, tập trung. Trong React Native, các thư viện như **Recoil** hoặc **Jotai** hỗ trợ quản lý trạng thái nguyên tử, giúp giảm render lại và cải thiện hiệu suất.

#### Ví dụ với Jotai
```javascript
import { atom, useAtom } from 'jotai';

const countAtom = atom(0);
const doubleAtom = atom((get) => get(countAtom) * 2);

const Counter = () => {
  const [count, setCount] = useAtom(countAtom);
  const [double] = useAtom(doubleAtom);

  return (
    <View>
      <Text>Đếm: {count}</Text>
      <Text>Gấp đôi: {double}</Text>
      <Button onPress={() => setCount(count + 1)} title="Tăng" />
    </View>
  );
};
```

#### Lợi ích
- **Render lại tối thiểu**: Chỉ các thành phần sử dụng atom cụ thể mới render lại.
- **Dễ mở rộng**: Thêm atom mới mà không làm phức tạp trạng thái toàn cục.
- **Hiệu suất cao**: Đặc biệt trong các ứng dụng lớn với trạng thái phức tạp.

#### Thực tiễn tốt nhất
- Chia trạng thái thành các atom nhỏ, có mục đích rõ ràng.
- Sử dụng các atom dẫn xuất (derived atoms) để tính toán giá trị dựa trên atom khác.
- Kết hợp với `React.memo` để tối ưu hóa thêm.

---

### REACT ĐỒNG THỜI

React Đồng Thời (Concurrent React) là một tập hợp các tính năng mới trong React 18, cho phép render không chặn và ưu tiên các cập nhật theo mức độ quan trọng. Trong React Native, các tính năng như `useTransition` và `useDeferredValue` giúp cải thiện hiệu suất giao diện.

#### Ví dụ với useTransition
```javascript
import React, { useState, useTransition } from 'react';
import { View, TextInput, Text, FlatList } from 'react-native';

const SearchList = () => {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState([]);
  const [isPending, startTransition] = useTransition();

  const handleSearch = (text) => {
    setQuery(text);
    startTransition(() => {
      // Giả lập tìm kiếm nặng
      const filtered = heavySearchFunction(text);
      setResults(filtered);
    });
  };

  return (
    <View>
      <TextInput
        value={query}
        onChangeText={handleSearch}
        placeholder="Tìm kiếm..."
      />
      {isPending && <Text>Đang tải...</Text>}
      <FlatList
        data={results}
        renderItem={({ item }) => <Text>{item}</Text>}
      />
    </View>
  );
};
```

#### Lợi ích
- **Ưu tiên giao diện**: Các cập nhật ít quan trọng (như tìm kiếm) không chặn giao diện.
- **Trải nghiệm mượt mà**: Giảm cảm giác giật khi xử lý các tác vụ nặng.
- **Tương lai bền vững**: Chuẩn bị ứng dụng cho các tính năng mới của React.

#### Thực tiễn tốt nhất
- Sử dụng `useTransition` cho các tác vụ không cần phản hồi ngay lập tức.
- Kết hợp với `Suspense` để hiển thị giao diện chờ (fallback UI).
- Kiểm tra hiệu suất trên thiết bị thực để đảm bảo cải thiện.

---

### TRÌNH BIÊN DỊCH REACT

Trình Biên Dịch React (React Compiler) là một công cụ tự động tối ưu hóa mã React bằng cách memoize các thành phần và hooks, giảm render lại không cần thiết. Trong React Native, nó giúp cải thiện hiệu suất mà không cần thay đổi mã thủ công.

#### Cách sử dụng
1. **Cài đặt Trình Biên Dịch React**:
   - Hiện tại (2025), Trình Biên Dịch React là một phần thử nghiệm. Theo dõi kho GitHub của React để cập nhật.
   - Cài đặt plugin Babel:
     ```bash
     npm install babel-plugin-react-compiler
     ```

2. **Cấu hình Babel**:
   ```javascript
   module.exports = {
     presets: ['module:metro-react-native-babel-preset'],
     plugins: ['react-compiler'],
   };
   ```

3. **Kiểm tra hiệu suất**:
   - Chạy ứng dụng và sử dụng React Profiler để so sánh số lần render trước và sau khi sử dụng compiler.
   - Kiểm tra FPS để xác nhận cải thiện.

#### Lợi ích
- **Tự động memoization**: Không cần thêm `useMemo` hoặc `useCallback` thủ công.
- **Hiệu suất cao**: Giảm đáng kể render lại trong các ứng dụng phức tạp.
- **Dễ tích hợp**: Chỉ cần cấu hình Babel, không cần thay đổi mã.

#### Thực tiễn tốt nhất
- Sử dụng trong các ứng dụng lớn với nhiều thành phần phức tạp.
- Kết hợp với các công cụ phân tích như Flipper để đo lường cải thiện.
- Theo dõi các cập nhật từ đội ngũ React để sử dụng phiên bản ổn định.

---

### HOẠT ẢNH HIỆU SUẤT CAO KHÔNG BỊ GIẬT KHUNG HÌNH

Hoạt ảnh là một phần quan trọng của trải nghiệm người dùng, nhưng chúng có thể gây ra giật khung hình nếu không được tối ưu hóa. Trong React Native, việc sử dụng **Animated API** và **Reanimated** giúp tạo hoạt ảnh mượt mà, chạy trên luồng native.

#### Ví dụ với Reanimated
```javascript
import React from 'react';
import { View, Button } from 'react-native';
import Animated, {
  useSharedValue,
  useAnimatedStyle,
  withSpring,
} from 'react-native-reanimated';

const AnimatedBox = () => {
  const offset = useSharedValue(0);

  const animatedStyle = useAnimatedStyle(() => ({
    transform: [{ translateX: offset.value }],
  }));

  const moveBox = () => {
    offset.value = withSpring(Math.random() * 100);
  };

  return (
    <View>
      <Animated.View
        style={[{ width: 100, height: 100, backgroundColor: 'blue' }, animatedStyle]}
      />
      <Button title="Di chuyển" onPress={moveBox} />
    </View>
  );
};

export default AnimatedBox;
```

#### Lợi ích của Reanimated
- **Chạy trên luồng native**: Giảm tải cho luồng JS, đảm bảo 60 FPS.
- **Hiệu suất cao**: Hỗ trợ các hoạt ảnh phức tạp như chuyển đổi 3D.
- **Dễ tích hợp**: API tương tự Animated, nhưng mạnh mẽ hơn.

#### Thực tiễn tốt nhất
- Sử dụng `useSharedValue` và `useAnimatedStyle` để quản lý trạng thái hoạt ảnh.
- Tránh chạy logic nặng trong luồng JS khi hoạt ảnh đang chạy.
- Kiểm tra hiệu suất trên thiết bị cấp thấp để đảm bảo hoạt ảnh mượt mà.

---

## PHẦN 2: NATIVE

### GIỚI THIỆU

Phần này tập trung vào các tối ưu hóa ở phía native của React Native, bao gồm các thành phần được viết bằng Kotlin/Java (Android), Swift/Objective-C (iOS), và C++ (lõi React Native). Tối ưu hóa native đặc biệt quan trọng khi bạn cần:
- Tăng tốc khởi động ứng dụng (TTI).
- Giảm sử dụng bộ nhớ native.
- Tối ưu hóa các tương tác phức tạp giữa luồng JS và luồng native.

#### Tại sao cần tối ưu hóa native?
- **Hiệu suất khởi động**: Các mô-đun native ảnh hưởng trực tiếp đến TTI.
- **Tương tác luồng**: Các nút thắt trong cầu nối (bridge) có thể làm chậm ứng dụng.
- **Khả năng mở rộng**: Ứng dụng lớn cần quản lý bộ nhớ và luồng hiệu quả.

#### Tổng quan về Kiến Trúc Mới
Kiến Trúc Mới của React Native (giới thiệu từ 2023) thay đổi cách ứng dụng tương tác với các thành phần native:
- **Turbo Modules**: Thay thế cầu nối cũ bằng các mô-đun native được tải theo nhu cầu.
- **Fabric**: Trình render mới, cải thiện hiệu suất render và đồng bộ hóa giao diện.
- **JSI (JavaScript Interface)**: Cho phép gọi trực tiếp mã native từ JS, giảm chi phí cầu nối.

Trong phần này, chúng tôi sẽ hướng dẫn cách sử dụng các công cụ như Android Studio, Xcode, và Flipper để phân tích hiệu suất native, cũng như các thực tiễn tốt nhất để tận dụng Kiến Trúc Mới.

---

### HƯỚNG DẪN: HIỂU SỰ KHÁC BIỆT GIỮA CÁC NỀN TẢNG

React Native cho phép viết mã một lần và chạy trên cả iOS và Android, nhưng mỗi nền tảng có những đặc điểm riêng ảnh hưởng đến hiệu suất. Hiểu sự khác biệt này giúp bạn tối ưu hóa ứng dụng hiệu quả hơn.

#### Sự khác biệt chính
1. **Ngôn ngữ lập trình**:
   - **Android**: Sử dụng Kotlin hoặc Java.
   - **iOS**: Sử dụng Swift hoặc Objective-C.
   - Cả hai nền tảng đều sử dụng C++ cho lõi React Native.

2. **Quản lý bộ nhớ**:
   - **Android**: Sử dụng ART (Android Runtime) với cơ chế thu gom rác (garbage collection).
   - **iOS**: Sử dụng ARC (Automatic Reference Counting) để quản lý bộ nhớ.

3. **Hiệu suất giao diện**:
   - **Android**: Có thể chậm hơn trên thiết bị cấp thấp do sự phân mảnh phần cứng.
   - **iOS**: Thường mượt mà hơn nhờ phần cứng đồng nhất.

4. **Cầu nối (Bridge)**:
   - Trước Kiến Trúc Mới, cầu nối JS-native là nút thắt chính, đặc biệt trên Android do độ trễ cao hơn.

#### Thực tiễn tốt nhất
- **Kiểm tra trên cả hai nền tảng**: Sử dụng thiết bị thực tế (đặc biệt là thiết bị cấp thấp) để phát hiện sự khác biệt về hiệu suất.
- **Tối ưu hóa riêng cho từng nền tảng**: Sử dụng các điều kiện nền tảng trong mã:
  ```javascript
  import { Platform } from 'react-native';

  const styles = StyleSheet.create({
    container: {
      padding: Platform.OS === 'ios' ? 10 : 5,
    },
  });
  ```
- **Sử dụng Turbo Modules**: Giảm chi phí cầu nối bằng cách chuyển sang Kiến Trúc Mới.

#### Công cụ phân tích
- **Android Studio**: Phân tích CPU, bộ nhớ, và hiệu suất native trên Android.
- **Xcode Instruments**: Phân tích hiệu suất và rò rỉ bộ nhớ trên iOS.
- **Flipper**: Cung cấp cái nhìn tổng quan về hiệu suất trên cả hai nền tảng.

---

### HƯỚNG DẪN: CÁCH PHÂN TÍCH HIỆU SUẤT CÁC PHẦN NATIVE CỦA REACT NATIVE

Phân tích hiệu suất native là bước quan trọng để xác định các nút thắt trong các thành phần native của ứng dụng React Native, chẳng hạn như mô-đun native, cầu nối (bridge), hoặc quản lý bộ nhớ. Các công cụ như Android Studio, Xcode Instruments, và Flipper giúp bạn đo lường và tối ưu hóa hiệu suất native.

#### Công cụ phân tích hiệu suất native
- **Android Studio Profiler**: Theo dõi CPU, bộ nhớ, mạng, và năng lượng trên Android.
- **Xcode Instruments**: Phân tích hiệu suất, rò rỉ bộ nhớ, và luồng trên iOS.
- **Flipper (Native Performance Plugin)**: Cung cấp cái nhìn tổng quan về hiệu suất trên cả iOS và Android.

#### Hướng dẫn sử dụng Android Studio Profiler
1. **Chuẩn bị ứng dụng**:
   - Đảm bảo ứng dụng của bạn được xây dựng ở chế độ debug hoặc profile.
   - Kết nối thiết bị Android thực tế hoặc sử dụng trình giả lập.

2. **Mở Profiler**:
   - Trong Android Studio, mở **View > Tool Windows > Profiler**.
   - Chọn ứng dụng React Native của bạn từ danh sách các tiến trình.

3. **Phân tích hiệu suất**:
   - **CPU**: Kiểm tra các hàm native (Kotlin/Java) hoặc C++ tiêu tốn nhiều thời gian CPU. Tìm các hàm liên quan đến cầu nối (bridge) hoặc mô-đun native.
   - **Bộ nhớ**: Theo dõi phân bổ bộ nhớ để phát hiện rò rỉ hoặc sử dụng bộ nhớ quá mức.
   - **Mạng**: Đảm bảo các yêu cầu mạng từ mô-đun native không gây độ trễ.
   - **Năng lượng**: Kiểm tra mức tiêu thụ pin, đặc biệt trên thiết bị cấp thấp.

4. **Tối ưu hóa**:
   - Nếu cầu nối bị tắc nghẽn, chuyển sang **Turbo Modules** để giảm chi phí giao tiếp JS-native.
   - Tối ưu hóa các hàm C++ trong lõi React Native bằng cách sử dụng các công cụ như Clang Static Analyzer.
   - Giảm kích thước mô-đun native bằng cách loại bỏ mã không sử dụng.

#### Hướng dẫn sử dụng Xcode Instruments
1. **Chuẩn bị ứng dụng**:
   - Xây dựng ứng dụng ở chế độ debug và chạy trên thiết bị iOS hoặc trình mô phỏng.

2. **Mở Instruments**:
   - Trong Xcode, chọn **Xcode > Open Developer Tool > Instruments**.
   - Chọn template **Time Profiler** để phân tích CPU hoặc **Leaks** để tìm rò rỉ bộ nhớ.

3. **Phân tích hiệu suất**:
   - **Time Profiler**: Xác định các hàm Swift/Objective-C hoặc C++ tiêu tốn nhiều thời gian. Tập trung vào các hàm liên quan đến **ReactBridge**.
   - **Leaks**: Phát hiện các đối tượng native không được giải phóng, chẳng hạn như view controllers hoặc mô-đun native.
   - **Allocations**: Theo dõi phân bổ bộ nhớ để tìm các đối tượng tích lũy bất thường.

4. **Tối ưu hóa**:
   - Sử dụng **Fabric** để cải thiện hiệu suất render giao diện.
   - Kiểm tra các mô-đun native tùy chỉnh để đảm bảo chúng được giải phóng đúng cách.
   - Tối ưu hóa các hàm C++ bằng cách giảm chi phí tính toán hoặc sử dụng các thư viện hiệu suất cao như **libdispatch**.

#### Thực tiễn tốt nhất
- Kiểm tra hiệu suất trên thiết bị thực tế, đặc biệt là thiết bị cấp thấp, để phát hiện các vấn đề thực tế.
- Sử dụng **Flipper** để có cái nhìn tổng quan trước khi đi sâu vào Android Studio hoặc Xcode.
- Tận dụng **JSI (JavaScript Interface)** để gọi trực tiếp mã native, giảm chi phí cầu nối.

---

### HƯỚNG DẪN: CÁCH ĐO TTI

Thời Gian Tương Tác (TTI - Time to Interactive) đo lường thời gian từ khi ứng dụng khởi động đến khi người dùng có thể tương tác đầy đủ với giao diện. Trong React Native, TTI bị ảnh hưởng bởi thời gian khởi tạo native, tải mô-đun JS, và render ban đầu.

#### Tại sao TTI quan trọng?
- TTI cao (trên 5 giây) có thể khiến người dùng bỏ rơi ứng dụng.
- TTI ảnh hưởng đến trải nghiệm người dùng, đặc biệt trong các ứng dụng có màn hình khởi động phức tạp.

#### Công cụ đo TTI
- **Flipper (Startup Plugin)**: Theo dõi thời gian khởi động và các giai đoạn khởi tạo.
- **React Native Performance**: Một thư viện để đo lường TTI và các chỉ số khởi động khác.
- **Công cụ tùy chỉnh**: Sử dụng `console.time` để đo lường các giai đoạn cụ thể.

#### Hướng dẫn đo TTI với Flipper
1. **Cài đặt Flipper Startup Plugin**:
   - Thêm plugin `react-native-performance` vào Flipper (xem hướng dẫn trong Phần 1).
   - Đảm bảo ứng dụng được tích hợp với Flipper.

2. **Theo dõi khởi động**:
   - Mở Flipper, chọn tab **Startup**.
   - Khởi động ứng dụng và quan sát các giai đoạn:
     - **Native Initialization**: Thời gian khởi tạo native (Kotlin/Swift).
     - **JS Bundle Loading**: Thời gian tải gói JS.
     - **React Render**: Thời gian render giao diện ban đầu.

3. **Phân tích kết quả**:
   - Nếu **Native Initialization** mất quá nhiều thời gian, kiểm tra các mô-đun native tùy chỉnh hoặc các thư viện bên thứ ba.
   - Nếu **JS Bundle Loading** chậm, tối ưu hóa kích thước gói JS (xem Phần 3).
   - Nếu **React Render** chậm, sử dụng React Profiler để tìm các thành phần render lại không cần thiết.

4. **Tối ưu hóa TTI**:
   - **Giảm thời gian khởi tạo native**:
     - Trì hoãn tải các mô-đun native không cần thiết bằng **Turbo Modules**.
     - Loại bỏ các thư viện native không sử dụng.
   - **Tối ưu hóa gói JS**:
     - Sử dụng **Hermes** để cải thiện tốc độ thực thi JS.
     - Tách gói JS thành các phần nhỏ hơn (code splitting).
   - **Cải thiện render ban đầu**:
     - Sử dụng giao diện khung (skeleton UI) để cải thiện hiệu suất cảm nhận.
     - Tránh render các thành phần phức tạp trong màn hình khởi động.

#### Thực tiễn tốt nhất
- Đo lường TTI trên thiết bị thực tế, đặc biệt là thiết bị cấp thấp.
- Sử dụng **React Navigation** với lazy loading để trì hoãn render các màn hình không cần thiết:
  ```javascript
  const Stack = createStackNavigator();
  <Stack.Screen name="Home" component={HomeScreen} options={{ lazy: true }} />
  ```
- Theo dõi TTI định kỳ trong suốt quá trình phát triển để phát hiện hồi quy.

---

### HƯỚNG DẪN: HIỂU QUẢN LÝ BỘ NHỚ NATIVE

Quản lý bộ nhớ native là yếu tố then chốt để đảm bảo ứng dụng React Native chạy mượt mà và không bị crash do hết bộ nhớ (OOM). Mỗi nền tảng (iOS và Android) có cơ chế quản lý bộ nhớ riêng, và React Native cần tích hợp tốt với cả hai.

#### Quản lý bộ nhớ trên Android
- **Cơ chế**: Android sử dụng ART (Android Runtime) với thu gom rác (garbage collection).
- **Thách thức**:
  - Các mô-đun native (Kotlin/Java) có thể giữ tham chiếu đến các đối tượng lớn, gây rò rỉ bộ nhớ.
  - Cầu nối JS-native có thể tạo ra các đối tượng tạm thời tiêu tốn bộ nhớ.

#### Quản lý bộ nhớ trên iOS
- **Cơ chế**: iOS sử dụng ARC (Automatic Reference Counting) để quản lý bộ nhớ.
- **Thách thức**:
  - Các view controllers hoặc mô-đun native (Swift/Objective-C) không được giải phóng đúng cách có thể gây rò rỉ.
  - Các đối tượng C++ trong lõi React Native cần được quản lý thủ công.

#### Công cụ phân tích bộ nhớ
- **Android Studio Memory Profiler**: Theo dõi phân bổ bộ nhớ và phát hiện rò rỉ.
- **Xcode Instruments (Leaks và Allocations)**: Phát hiện rò rỉ và phân bổ bất thường trên iOS.
- **Flipper Memory Plugin**: Cung cấp cái nhìn tổng quan về bộ nhớ native và JS.

#### Hướng dẫn tìm rò rỉ bộ nhớ native
1. **Sử dụng Android Studio**:
   - Mở **Memory Profiler** và chạy ứng dụng.
   - Thực hiện các hành động như điều hướng qua lại giữa các màn hình.
   - Tìm các đối tượng Java/Kotlin tích lũy bất thường, đặc biệt là các instance của `ReactContext` hoặc `NativeModule`.

2. **Sử dụng Xcode Instruments**:
   - Mở **Leaks** trong Instruments.
   - Chạy ứng dụng và điều hướng qua các màn hình.
   - Tìm các đối tượng Swift/Objective-C hoặc C++ không được giải phóng, chẳng hạn như `RCTView` hoặc `RCTBridge`.

3. **Khắc phục rò rỉ**:
   - Đảm bảo các mô-đun native được giải phóng đúng cách trong `onCatalystInstanceDestroy`:
     ```java
     @Override
     public void onCatalystInstanceDestroy() {
       // Giải phóng tài nguyên
       myNativeResource = null;
     }
     ```
   - Sử dụng **JSI** để quản lý bộ nhớ hiệu quả hơn, giảm sự phụ thuộc vào cầu nối.
   - Kiểm tra các thư viện bên thứ ba để đảm bảo chúng không giữ tham chiếu không cần thiết.

#### Thực tiễn tốt nhất
- Tránh tải các mô-đun native lớn trong giai đoạn khởi động.
- Sử dụng **Turbo Modules** để quản lý tài nguyên native theo nhu cầu.
- Theo dõi bộ nhớ định kỳ trên thiết bị cấp thấp để phát hiện vấn đề sớm.

---

### HƯỚNG DẪN: HIỂU MÔ HÌNH LUỒNG CỦA TURBO MODULES VÀ FABRIC

Kiến Trúc Mới của React Native giới thiệu **Turbo Modules** và **Fabric**, thay đổi cách luồng JS và native tương tác. Hiểu mô hình luồng này giúp bạn tối ưu hóa hiệu suất và giảm độ trễ.

#### Turbo Modules
- **Khái niệm**: Turbo Modules thay thế cầu nối JS-native cũ bằng cách cho phép gọi trực tiếp mã native từ JS thông qua **JSI**.
- **Lợi ích**:
  - Giảm chi phí giao tiếp giữa JS và native.
  - Tải mô-đun theo nhu cầu, cải thiện TTI.
- **Mô hình luồng**:
  - Các hàm native được gọi đồng bộ hoặc bất đồng bộ trên luồng JS hoặc native.
  - JSI quản lý giao tiếp, tránh hàng đợi cầu nối.

#### Fabric
- **Khái niệm**: Fabric là trình render mới, đồng bộ hóa giao diện giữa JS và native hiệu quả hơn.
- **Lợi ích**:
  - Render giao diện trên luồng native, giảm tải cho luồng JS.
  - Hỗ trợ render đồng thời, cải thiện FPS.
- **Mô hình luồng**:
  - Luồng JS: Xử lý logic kinh doanh và tính toán trạng thái.
  - Luồng native: Render giao diện và xử lý sự kiện native.
  - Luồng render: Một luồng riêng biệt để đồng bộ hóa cây giao diện.

#### Hướng dẫn tối ưu hóa với Turbo Modules và Fabric
1. **Chuyển sang Turbo Modules**:
   - Cập nhật các mô-đun native tùy chỉnh để tương thích với Turbo Modules:
     ```javascript
     import { TurboModuleRegistry } from 'react-native';
     const MyModule = TurboModuleRegistry.get('MyModule');
     ```
   - Trì hoãn tải các mô-đun không cần thiết:
     ```javascript
     const LazyModule = TurboModuleRegistry.getEnforcing('LazyModule');
     ```

2. **Sử dụng Fabric**:
   - Kích hoạt Fabric trong ứng dụng bằng cách cập nhật `react-native` lên phiên bản mới nhất (2025).
   - Sử dụng **Shadow Tree** để tối ưu hóa render:
     ```javascript
     import { enableFabric } from 'react-native';
     enableFabric();
     ```

3. **Phân tích hiệu suất**:
   - Sử dụng Flipper để theo dõi thời gian giao tiếp giữa JS và native.
   - Kiểm tra FPS và TTI để đảm bảo cải thiện sau khi áp dụng Turbo Modules và Fabric.

#### Thực tiễn tốt nhất
- Chỉ tải các Turbo Modules cần thiết trong giai đoạn khởi động.
- Sử dụng các API đồng thời của Fabric để ưu tiên render giao diện.
- Kiểm tra hiệu suất trên cả iOS và Android để đảm bảo tính tương thích.

---

### SỬ DỤNG LÀM PHẲNG GIAO DIỆN

Làm phẳng giao diện (UI flattening) là kỹ thuật giảm số lượng view được render trong cây giao diện, giúp cải thiện hiệu suất render và FPS, đặc biệt trên Android.

#### Tại sao cần làm phẳng giao diện?
- Cây giao diện phức tạp (nhiều view lồng nhau) làm tăng chi phí render.
- Android đặc biệt nhạy cảm với số lượng view do giới hạn phần cứng.

#### Hướng dẫn làm phẳng giao diện
1. **Kiểm tra cây giao diện**:
   - Sử dụng **React Native DevTools** hoặc **Flipper Layout Plugin** để kiểm tra số lượng view.
   - Tìm các thành phần lồng nhau không cần thiết, chẳng hạn như nhiều `<View>` không có style.

2. **Tối ưu hóa mã**:
   - Gộp các `<View>` không cần thiết:
     ```javascript
     // Trước
     <View style={styles.outer}>
       <View style={styles.inner}>
         <Text>Hello</Text>
       </View>
     </View>

     // Sau
     <View style={[styles.outer, styles.inner]}>
       <Text>Hello</Text>
     </View>
     ```
   - Sử dụng `StyleSheet.flatten` để hợp nhất các style:
     ```javascript
     import { StyleSheet } from 'react-native';
     const flattenedStyle = StyleSheet.flatten([styles.outer, styles.inner]);
     ```

3. **Sử dụng FlatList**:
   - Thay `<ScrollView>` bằng `<FlatList>` để render danh sách hiệu quả hơn:
     ```javascript
     <FlatList
       data={data}
       renderItem={({ item }) => <Text>{item}</Text>}
       keyExtractor={(item) => item.id}
     />
     ```

#### Thực tiễn tốt nhất
- Giữ cây giao diện càng phẳng càng tốt, đặc biệt trên Android.
- Sử dụng **shouldComponentUpdate** hoặc `React.memo` để tránh render lại các view không thay đổi.
- Kiểm tra hiệu suất sau khi làm phẳng bằng Flipper hoặc Android Studio.

---

### SỬ DỤNG SDK REACT NATIVE CHUYÊN DỤNG THAY VÌ WEB

Nhiều thư viện phổ biến (như Firebase, Analytics) có phiên bản web và native. Trong React Native, sử dụng SDK native thay vì web giúp cải thiện hiệu suất và tích hợp tốt hơn với nền tảng.

#### Ví dụ với Firebase
- **Web SDK**:
  ```javascript
  import firebase from 'firebase/app';
  import 'firebase/analytics';
  ```
- **Native SDK**:
  ```javascript
  import firebase from '@react-native-firebase/app';
  import analytics from '@react-native-firebase/analytics';
  ```

#### Lợi ích của SDK native
- **Hiệu suất cao**: Truy cập trực tiếp vào API native, giảm chi phí cầu nối.
- **Tích hợp tốt hơn**: Hỗ trợ các tính năng như thông báo đẩy, lưu trữ ngoại tuyến.
- **Tiết kiệm tài nguyên**: Giảm kích thước gói JS so với các polyfill web.

#### Thực tiễn tốt nhất
- Kiểm tra tài liệu của thư viện để tìm phiên bản native (ví dụ: `@react-native-firebase`, `@react-native-community`).
- Sử dụng các điều kiện nền tảng để tải SDK phù hợp:
  ```javascript
  import { Platform } from 'react-native';
  const Analytics = Platform.OS === 'web' ? WebAnalytics : NativeAnalytics;
  ```
- Tối ưu hóa khởi tạo SDK bằng cách trì hoãn tải đến khi cần thiết.

---

### HƯỚNG DẪN: LÀM CHO CÁC MÔ-ĐUN NATIVE NHANH HƠN

Các mô-đun native (viết bằng Kotlin/Java cho Android hoặc Swift/Objective-C cho iOS) là thành phần quan trọng trong ứng dụng React Native, đặc biệt khi bạn cần truy cập các tính năng nền tảng như camera, GPS, hoặc thông báo đẩy. Tuy nhiên, các mô-đun native không được tối ưu hóa có thể làm chậm ứng dụng, tăng TTI, hoặc gây ra độ trễ trong giao tiếp JS-native. Dưới đây là cách làm cho các mô-đun native nhanh hơn.

#### Tại sao mô-đun native có thể chậm?
- **Khởi tạo nặng**: Tải các thư viện lớn hoặc thực hiện các phép tính phức tạp khi khởi động.
- **Giao tiếp cầu nối**: Gửi/nhận dữ liệu qua cầu nối JS-native có chi phí cao.
- **Quản lý tài nguyên kém**: Giữ tham chiếu đến các đối tượng lớn hoặc không giải phóng tài nguyên.

#### Hướng dẫn tối ưu hóa mô-đun native
1. **Sử dụng Turbo Modules**:
   - Turbo Modules cho phép gọi trực tiếp mã native qua JSI, giảm chi phí cầu nối.
   - Chuyển đổi mô-đun native cũ sang Turbo Modules:
     ```javascript
     // Trong tệp JS
     import { TurboModuleRegistry } from 'react-native';
     const MyModule = TurboModuleRegistry.getEnforcing('MyModule');

     // Trong mã native (Kotlin)
     class MyModule : TurboModule {
       override fun getName(): String = "MyModule"
       override fun doSomething() {
         // Logic native
       }
     }
     ```

2. **Trì hoãn khởi tạo**:
   - Tránh khởi tạo các mô-đun native trong giai đoạn khởi động ứng dụng.
   - Sử dụng lazy loading:
     ```javascript
     const LazyModule = () => importNativeModule('LazyModule');
     ```

3. **Tối ưu hóa mã native**:
   - **Android (Kotlin/Java)**:
     - Sử dụng các hàm bất đồng bộ để tránh chặn luồng chính:
       ```kotlin
       @ReactMethod(isBlockingSynchronousMethod = false)
       fun doAsyncTask(promise: Promise) {
         GlobalScope.launch(Dispatchers.IO) {
           // Công việc nặng
           promise.resolve(result)
         }
       }
       ```
     - Loại bỏ mã không sử dụng bằng ProGuard hoặc R8.
   - **iOS (Swift/Objective-C)**:
     - Sử dụng Grand Central Dispatch (GCD) để chạy các tác vụ nặng trên luồng nền:
       ```swift
       @objc func doHeavyTask(_ resolve: @escaping RCTPromiseResolveBlock, reject: @escaping RCTPromiseRejectBlock) {
         DispatchQueue.global().async {
           // Công việc nặng
           resolve(result)
         }
       }
       ```
     - Giảm sử dụng các API đồng bộ như `dispatch_sync`.

4. **Giảm dữ liệu truyền qua cầu nối**:
   - Chỉ gửi dữ liệu cần thiết giữa JS và native.
   - Sử dụng định dạng dữ liệu nhẹ (như JSON thay vì đối tượng phức tạp):
     ```javascript
     // Trước
     MyModule.sendLargeObject({ complex: largeObject });
     // Sau
     MyModule.sendMinimalData({ id: largeObject.id });
     ```

5. **Phân tích hiệu suất**:
   - Sử dụng **Android Studio Profiler** hoặc **Xcode Instruments** để đo thời gian thực thi của các hàm native.
   - Tìm các hàm tiêu tốn nhiều CPU hoặc bộ nhớ.

#### Thực tiễn tốt nhất
- Tận dụng **JSI** để gọi trực tiếp mã native, đặc biệt cho các tác vụ lặp lại.
- Kiểm tra hiệu suất mô-đun trên thiết bị cấp thấp để phát hiện các vấn đề thực tế.
- Tài liệu hóa các mô-đun native để dễ dàng bảo trì và tối ưu hóa trong tương lai.

---

### HƯỚNG DẪN: CÁCH TÌM RÒ RỈ BỘ NHỚ

Rò rỉ bộ nhớ native xảy ra khi các đối tượng native (như view, mô-đun, hoặc tài nguyên) không được giải phóng, dẫn đến tiêu tốn bộ nhớ và có thể gây crash ứng dụng. Trong React Native, rò rỉ bộ nhớ native thường liên quan đến cầu nối, mô-đun tùy chỉnh, hoặc các thư viện bên thứ ba.

#### Dấu hiệu của rò rỉ bộ nhớ native
- Ứng dụng chậm dần hoặc crash sau thời gian dài sử dụng.
- Bộ nhớ heap native tăng liên tục trong Android Studio hoặc Xcode Instruments.
- Các lỗi "Out of Memory" (OOM) trên thiết bị cấp thấp.

#### Công cụ tìm rò rỉ bộ nhớ
- **Android Studio Memory Profiler**: Phát hiện các đối tượng Java/Kotlin không được thu gom.
- **Xcode Instruments (Leaks và Allocations)**: Tìm rò rỉ trong Swift/Objective-C hoặc C++.
- **Flipper Memory Plugin**: Theo dõi bộ nhớ native và JS tổng quan.

#### Hướng dẫn tìm và khắc phục rò rỉ
1. **Sử dụng Android Studio Memory Profiler**:
   - Mở **Memory Profiler** và chạy ứng dụng.
   - Thực hiện các hành động như điều hướng qua lại giữa các màn hình hoặc gọi mô-đun native.
   - Chụp heap snapshot và tìm các đối tượng tích lũy bất thường, chẳng hạn như `ReactContext`, `NativeModule`, hoặc `View`.
   - Kiểm tra các tham chiếu giữ lại đối tượng (retaining references).

2. **Sử dụng Xcode Instruments**:
   - Mở **Leaks** trong Instruments và chạy ứng dụng.
   - Tìm các đối tượng Swift/Objective-C hoặc C++ không được giải phóng, như `RCTView`, `RCTBridge`, hoặc view controllers.
   - Sử dụng **Allocations** để theo dõi phân bổ bộ nhớ và phát hiện các đối tượng tăng liên tục.

3. **Khắc phục rò rỉ**:
   - **Giải phóng tài nguyên trong mô-đun native**:
     - Trong Android:
       ```kotlin
       override fun onCatalystInstanceDestroy() {
         myResource?.release()
         myResource = null
       }
       ```
     - Trong iOS:
       ```swift
       deinit {
         myResource = nil
       }
       ```
   - **Kiểm tra cầu nối**:
     - Đảm bảo các lời gọi qua cầu nối được hoàn tất và không giữ tham chiếu:
       ```javascript
       MyModule.doTask().then(() => {
         // Xử lý kết quả
       }).catch(() => {
         // Xử lý lỗi
       });
       ```
   - **Kiểm tra thư viện bên thứ ba**:
     - Một số thư viện (như `react-native-maps`) có thể gây rò rỉ nếu không được cấu hình đúng.
     - Cập nhật thư viện lên phiên bản mới nhất hoặc kiểm tra mã nguồn.


4. **Phân tích với Flipper**:
   - Sử dụng **Memory Plugin** để so sánh heap snapshots trước và sau các hành động.
   - Tìm các đối tượng native liên quan đến React Native (như `RCTRootView`) không được giải phóng.

#### Thực tiễn tốt nhất
- Luôn giải phóng tài nguyên trong các phương thức dọn dẹp (`onCatalystInstanceDestroy`, `deinit`).
- Sử dụng **Turbo Modules** để quản lý tài nguyên native hiệu quả hơn.
- Theo dõi bộ nhớ định kỳ trong quá trình phát triển để phát hiện rò rỉ sớm.

---

## PHẦN 3: GÓI ỨNG DỤNG

### GIỚI THIỆU

Phần này tập trung vào việc tối ưu hóa kích thước và hiệu suất của gói ứng dụng (APK trên Android hoặc IPA trên iOS) và gói JavaScript (JS bundle). Một gói ứng dụng được tối ưu hóa giúp:
- **Giảm thời gian tải**: Gói nhỏ hơn tải nhanh hơn, cải thiện TTI.
- **Tiết kiệm băng thông**: Đặc biệt quan trọng cho người dùng trên mạng chậm.
- **Cải thiện khả năng mở rộng**: Dễ dàng cập nhật và bảo trì ứng dụng.

Các kỹ thuật chính bao gồm phân tích kích thước gói, loại bỏ mã không sử dụng, và tải mã từ xa khi cần. Chúng tôi sẽ sử dụng các công cụ như **Metro Bundle Visualizer**, **Android Studio APK Analyzer**, và **Xcode Archive** để hỗ trợ quá trình này.

---

### HƯỚNG DẪN: CÁCH PHÂN TÍCH KÍCH THƯỚC GÓI JS

Kích thước gói JavaScript (JS bundle) là một yếu tố quan trọng ảnh hưởng đến thời gian tải và hiệu suất tổng thể của ứng dụng React Native. Phân tích kích thước gói JS giúp bạn xác định các phần mã hoặc thư viện chiếm nhiều dung lượng và tối ưu hóa chúng.

#### Công cụ phân tích
- **Metro Bundle Visualizer**: Hiển thị cấu trúc gói JS dưới dạng biểu đồ, giúp xác định các thư viện hoặc module lớn.
- **Webpack Bundle Analyzer**: Một công cụ thay thế nếu bạn sử dụng Webpack thay vì Metro.
- **Flipper (Bundle Plugin)**: Theo dõi kích thước gói JS và các thay đổi theo thời gian.

#### Hướng dẫn sử dụng Metro Bundle Visualizer
1. **Cài đặt công cụ**:
   - Cài đặt `metro-visualizer`:
     ```bash
     npm install --save-dev metro-visualizer
     ```

2. **Tạo báo cáo**:
   - Chạy lệnh để tạo biểu đồ gói JS:
     ```bash
     npx metro-visualizer
     ```
   - Công cụ sẽ tạo một tệp HTML hiển thị cấu trúc gói JS, với các module và thư viện được phân loại theo kích thước.

3. **Phân tích kết quả**:
   - Tìm các thư viện lớn (như `lodash`, `moment`) hoặc các module tùy chỉnh chiếm nhiều dung lượng.
   - Kiểm tra các module trùng lặp (duplicate modules), thường do cấu hình Metro không chính xác.
   - Xác định mã không sử dụng (dead code) có thể loại bỏ.

4. **Tối ưu hóa gói JS**:
   - **Tree Shaking**: Đảm bảo Metro loại bỏ mã không sử dụng:
     ```javascript
     // metro.config.js
     module.exports = {
       transformer: {
         minifierConfig: {
           keep_classnames: false,
           mangle: false,
         },
       },
     };
     ```
   - **Code Splitting**: Tách gói JS thành các phần nhỏ hơn:
     ```javascript
     const LazyComponent = React.lazy(() => import('./LazyComponent'));
     ```
   - **Sử dụng Hermes**: Bật Hermes để giảm kích thước gói JS và cải thiện hiệu suất thực thi:
     ```gradle
     // android/app/build.gradle
     project.ext.react = [
       enableHermes: true
     ]
     ```

#### Thực tiễn tốt nhất
- Theo dõi kích thước gói JS sau mỗi lần thêm thư viện hoặc cập nhật mã.
- Sử dụng các thư viện nhẹ hơn (ví dụ: thay `moment` bằng `date-fns`).
- Kiểm tra kích thước gói trên thiết bị thực tế để đảm bảo hiệu suất.

---

### HƯỚNG DẪN: CÁCH PHÂN TÍCH KÍCH THƯỚC GÓI ỨNG DỤNG

Kích thước gói ứng dụng (APK trên Android hoặc IPA trên iOS) ảnh hưởng trực tiếp đến thời gian tải, cài đặt, và cập nhật ứng dụng. Phân tích kích thước gói giúp bạn xác định các thành phần chiếm nhiều dung lượng và tối ưu hóa chúng.

#### Công cụ phân tích
- **Android Studio APK Analyzer**: Phân tích cấu trúc APK, bao gồm tài nguyên, thư viện native, và gói JS.
- **Xcode Archive**: Kiểm tra kích thước IPA và các thành phần như tài nguyên, framework.
- **Bundletool**: Phân tích kích thước APK theo cấu hình thiết bị (ví dụ: DPI, ABI).

#### Hướng dẫn sử dụng Android Studio APK Analyzer
1. **Tạo APK**:
   - Chạy lệnh để tạo APK release:
     ```bash
     cd android && ./gradlew assembleRelease
     ```

2. **Mở APK Analyzer**:
   - Trong Android Studio, chọn **File > Profile or Debug APK** và chọn file APK.
   - Phân tích các thành phần:
     - **res/**: Tài nguyên (hình ảnh, XML).
     - **lib/**: Thư viện native (SO files).
     - **assets/**: Gói JS và tài nguyên khác.

3. **Tối ưu hóa**:
   - **Tài nguyên**:
     - Nén hình ảnh bằng công cụ như `ImageOptim` hoặc `TinyPNG`.
     - Loại bỏ tài nguyên không sử dụng bằng `androidResources` trong Gradle:
       ```gradle
       android {
         buildTypes {
           release {
             shrinkResources true
           }
         }
       }
       ```
   - **Thư viện native**:
     - Chỉ bao gồm các ABI cần thiết (ví dụ: `armeabi-v7a`, `arm64-v8a`):
       ```gradle
       android {
         splits {
           abi {
             enable true
             reset()
             include 'armeabi-v7a', 'arm64-v8a'
           }
         }
       }
       ```
   - **Gói JS**:
     - Tối ưu hóa gói JS như đã đề cập ở chương trước (tree shaking, code splitting).

4. **Kiểm tra kích thước**:
   - So sánh kích thước APK trước và sau khi tối ưu hóa.
   - Kiểm tra trên các thiết bị với cấu hình khác nhau bằng **Bundletool**:
     ```bash
     bundletool build-apks --bundle=app.aab --output=app.apks
     ```

#### Hướng dẫn sử dụng Xcode Archive
1. **Tạo IPA**:
   - Trong Xcode, chọn **Product > Archive** để tạo file archive.
   - Xuất IPA từ Organizer.

2. **Phân tích IPA**:
   - Mở file IPA (đổi đuôi thành .zip và giải nén).
   - Kiểm tra các thư mục:
     - **Frameworks**: Các thư viện native (Swift, Objective-C).
     - **Assets**: Tài nguyên (hình ảnh, font).
     - **Main Bundle**: Gói JS và mã thực thi.

3. **Tối ưu hóa**:
   - **Tài nguyên**: Nén hình ảnh và loại bỏ tài nguyên không sử dụng bằng `Asset Catalog`.
   - **Thư viện**: Loại bỏ các framework không cần thiết trong **Build Phases**.
   - **Gói JS**: Tương tự Android, sử dụng Hermes và code splitting.

#### Thực tiễn tốt nhất
- Sử dụng **App Bundles** (AAB) trên Android để giảm kích thước APK theo thiết bị.
- Kiểm tra kích thước IPA trên iOS bằng cách xuất archive với các tùy chọn tối ưu hóa.
- Theo dõi kích thước gói sau mỗi lần thêm thư viện hoặc tài nguyên mới.

---

### HƯỚNG DẪN: XÁC ĐỊNH KÍCH THƯỚC THỰC SỰ CỦA THƯ VIỆN BÊN THỨ BA

Các thư viện bên thứ ba (như `react-native-maps`, `react-native-firebase`) có thể làm tăng đáng kể kích thước gói ứng dụng. Phân tích kích thước thực sự của chúng giúp bạn đưa ra quyết định có nên sử dụng hay thay thế.

#### Công cụ phân tích
- **Webpack Bundle Analyzer**: Phân tích kích thước thư viện trong gói JS.
- **Metro Bundle Visualizer**: Kiểm tra kích thước thư viện trong React Native.
- **Android Studio APK Analyzer**: Phân tích thư viện native trong APK.

#### Hướng dẫn phân tích
1. **Phân tích gói JS**:
   - Sử dụng **Metro Bundle Visualizer** để kiểm tra kích thước của thư viện:
     ```bash
     npx metro-visualizer
     ```
   - Tìm các thư viện lớn (ví dụ: `moment`, `lodash`) và xác định kích thước sau khi tree shaking.

2. **Phân tích thư viện native**:
   - Trong **Android Studio APK Analyzer**, kiểm tra thư mục `lib/` để tìm các file `.so` liên quan đến thư viện.
   - Trong Xcode, kiểm tra thư mục **Frameworks** trong IPA.

3. **Đánh giá kích thước thực**:
   - So sánh kích thước gói trước và sau khi thêm thư viện:
     ```bash
     # Tạo gói không có thư viện
     npx react-native bundle --platform android --dev false --entry-file index.js --bundle-output main.jsbundle
     # Thêm thư viện và tạo lại gói
     ```
   - Kiểm tra tài liệu của thư viện để biết các mô-đun tùy chọn có thể loại bỏ.

4. **Tối ưu hóa**:
   - **Loại bỏ mô-đun không cần thiết**:
     - Ví dụ, với `react-native-firebase`, chỉ cài đặt các mô-đun cần thiết (như `analytics`, `auth`):
       ```bash
       npm install @react-native-firebase/analytics @react-native-firebase/auth
       ```
   - **Thay thế thư viện nặng**:
     - Thay `moment` bằng `date-fns` hoặc `day.js` để giảm kích thước gói JS:
       ```javascript
       import { format } from 'date-fns';
       const formattedDate = format(new Date(), 'yyyy-MM-dd');
       ```
   - **Sử dụng tree shaking**:
     - Đảm bảo thư viện hỗ trợ tree shaking và sử dụng các import cụ thể:
       ```javascript
       import { get } from 'lodash/get';
       ```

#### Thực tiễn tốt nhất
- Luôn kiểm tra kích thước thư viện trước khi thêm vào dự án.
- Ưu tiên các thư viện native thay vì web để giảm kích thước gói JS.
- Cập nhật thư viện thường xuyên để tận dụng các cải tiến về kích thước và hiệu suất.

---

### HƯỚNG DẪN: TRÁNH XUẤT BARREL

Xuất barrel (barrel exports) là kỹ thuật xuất nhiều module từ một tệp duy nhất (thường là `index.js`). Trong React Native, barrel exports có thể làm tăng kích thước gói JS do cản trở tree shaking.

#### Ví dụ barrel exports
```javascript
// Trước (barrel export)
export * from './moduleA';
export * from './moduleB';
export * from './moduleC';

// Sau (import cụ thể)
import ModuleA from './moduleA';
import ModuleB from './moduleB';
export { ModuleA, ModuleB };
```

#### Tại sao nên tránh?
- **Cản trở tree shaking**: Các công cụ như Metro hoặc Webpack không thể loại bỏ mã không sử dụng từ barrel exports.
- **Tăng kích thước gói**: Bao gồm cả các module không cần thiết.

#### Hướng dẫn tránh barrel exports
1. **Kiểm tra mã**:
   - Tìm các tệp `index.js` sử dụng `export * from`.
   - Kiểm tra các import trong ứng dụng:
     ```javascript
     // Tránh
     import { ModuleA, ModuleB } from './modules';
     // Nên dùng
     import ModuleA from './modules/moduleA';
     import ModuleB from './modules/moduleB';
     ```

2. **Tái cấu trúc mã**:
   - Thay thế barrel exports bằng các export cụ thể:
     ```javascript
     export { default as ModuleA } from './moduleA';
     export { default as ModuleB } from './moduleB';
     ```
   - Cập nhật các import trong ứng dụng để sử dụng đường dẫn cụ thể.

3. **Phân tích hiệu quả**:
   - Sử dụng **Metro Bundle Visualizer** để kiểm tra kích thước gói trước và sau khi loại bỏ barrel exports.
   - Kiểm tra kích thước APK/IPA để xác nhận cải thiện.

#### Thực tiễn tốt nhất
- Tránh sử dụng `export *` trong các tệp `index.js`.
- Sử dụng các công cụ như ESLint để phát hiện barrel exports:
  ```json
  {
    "rules": {
      "no-barrel-files": "error"
    }
  }
  ```
- Tài liệu hóa cấu trúc module để khuyến khích các import cụ thể.

---

### HƯỚNG DẪN: THỬ NGHIỆM VỚI TREE SHAKING

Tree shaking là kỹ thuật loại bỏ mã không sử dụng (dead code) trong quá trình xây dựng gói, giúp giảm kích thước gói JS. Trong React Native, tree shaking đặc biệt quan trọng khi sử dụng các thư viện lớn như `lodash` hoặc `moment`.

#### Cách tree shaking hoạt động
- Các công cụ như Metro, Webpack, hoặc Rollup phân tích mã để xác định các phần không được sử dụng.
- Mã không được import hoặc gọi sẽ bị loại bỏ khỏi gói cuối cùng.

#### Hướng dẫn áp dụng tree shaking
1. **Cấu hình Metro**:
   - Đảm bảo Metro được cấu hình để hỗ trợ tree shaking:
     ```javascript
     // metro.config.js
     module.exports = {
       transformer: {
         minifierConfig: {
           keep_classnames: false,
           mangle: false,
         },
       },
     };
     ```

2. **Sử dụng các import cụ thể**:
   - Tránh import toàn bộ thư viện:
     ```javascript
     // Tránh
     import _ from 'lodash';
     // Nên dùng
     import get from 'lodash/get';
     ```

3. **Kiểm tra hiệu quả**:
   - Sử dụng **Metro Bundle Visualizer** để kiểm tra kích thước gói trước và sau khi áp dụng tree shaking.
   - So sánh kích thước gói JS:
     ```bash
     npx react-native bundle --platform android --dev false --entry-file index.js --bundle-output main.jsbundle
     ```

4. **Khắc phục các vấn đề**:
   - Một số thư viện không hỗ trợ tree shaking (như `moment`).
   - Thay thế bằng các thư viện thân thiện với tree shaking (như `date-fns`):
     ```javascript
     import { format } from 'date-fns';
     ```

#### Thực tiễn tốt nhất
- Kiểm tra tài liệu của thư viện để đảm bảo hỗ trợ tree shaking.
- Sử dụng các công cụ như `esbuild` để phân tích mã không sử dụng:
  ```bash
  npx esbuild --bundle index.js --outfile=out.js --tree-shaking=true
  ```
- Kết hợp tree shaking với code splitting để tối ưu hóa thêm.

---

### HƯỚNG DẪN: TẢI MÃ TỪ XA KHI CẦN

Tải mã từ xa (code pushing) là kỹ thuật tải các phần mã JS từ máy chủ thay vì bao gồm trong gói ứng dụng ban đầu. Điều này giúp giảm kích thước gói và cho phép cập nhật ứng dụng mà không cần phát hành phiên bản mới.

#### Lợi ích
- **Gói nhỏ hơn**: Chỉ tải mã cần thiết khi người dùng truy cập tính năng.
- **Cập nhật nhanh**: Sửa lỗi hoặc thêm tính năng mà không cần cập nhật qua store.
- **Linh hoạt**: Tải các tính năng theo ngữ cảnh (ví dụ: chỉ tải mã quảng cáo trong chiến dịch).

#### Hướng dẫn triển khai code pushing
1. **Sử dụng thư viện**:
   - **CodePush** (Microsoft) là lựa chọn phổ biến cho React Native:
     ```bash
     npm install react-native-code-push
     ```

2. **Cấu hình CodePush**:
   - Liên kết ứng dụng với CodePush:
     ```bash
     code-push app add MyApp android react-native
     code-push app add MyApp ios react-native
     ```
   - Cập nhật mã trong `App.js`:
     ```javascript
     import codePush from 'react-native-code-push';
     const App = () => {
       // Logic ứng dụng
     };
     export default codePush({ checkFrequency: codePush.CheckFrequency.ON_APP_START })(App);
     ```

3. **Tách mã**:
   - Tạo các bundle riêng cho từng tính năng:
     ```bash
     npx react-native bundle --platform android --entry-file feature1.js --bundle-output feature1.jsbundle
     ```
   - Tải bundle từ xa khi cần:
     ```javascript
     import { fetch } from 'react-native';
     const loadFeature = async () => {
       const bundle = await fetch('https://my-server.com/feature1.jsbundle');
       // Tải bundle vào ứng dụng
     };
     ```

4. **Phân tích hiệu suất**:
   - Đo TTI và FPS để đảm bảo tải mã từ xa không làm chậm ứng dụng.
   - Sử dụng Flipper để theo dõi thời gian tải bundle.

#### Thực tiễn tốt nhất
- Lưu trữ bundle trên CDN (như AWS CloudFront) để tải nhanh hơn.
- Triển khai cơ chế fallback nếu tải bundle thất bại:
  ```javascript
  const loadFeature = async () => {
    try {
      const bundle = await fetch('https://my-server.com/feature1.jsbundle');
      return bundle;
    } catch (error) {
      return fallbackFeature;
    }
  };
  ```
- Kiểm tra code pushing trên mạng chậm (3G, 4G) để đảm bảo trải nghiệm người dùng.

---

### HƯỚNG DẪN: THU NHỎ MÃ VỚI R8 ANDROID

R8 là công cụ tối ưu hóa mã trên Android, thay thế ProGuard, giúp thu nhỏ mã, loại bỏ mã không sử dụng, và tối ưu hóa hiệu suất. Trong React Native, R8 đặc biệt hữu ích để giảm kích thước APK.

#### Cách R8 hoạt động
- **Thu nhỏ mã**: Rút ngắn tên lớp, phương thức, và biến.
- **Loại bỏ mã không sử dụng**: Tương tự tree shaking, nhưng áp dụng cho mã native.
- **Tối ưu hóa**: Hợp nhất các lớp và phương thức để cải thiện hiệu suất.

#### Hướng dẫn sử dụng R8
1. **Kích hoạt R8**:
   - Trong `android/app/build.gradle`:
     ```gradle
     android {
       buildTypes {
         release {
           minifyEnabled true
           proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
         }
       }
     }
     ```

2. **Cấu hình quy tắc ProGuard**:
   - Tạo tệp `android/app/proguard-rules.pro` để tránh xóa mã cần thiết:
     ```proguard
     -keep class com.facebook.** { *; }
     -keep class com.myapp.** { *; }
     ```

3. **Phân tích kết quả**:
   - Xây dựng APK release và sử dụng **APK Analyzer** để kiểm tra kích thước trước và sau khi áp dụng R8.
   - Kiểm tra hiệu suất ứng dụng để đảm bảo R8 không làm hỏng chức năng.

4. **Khắc phục lỗi**:
   - Nếu ứng dụng gặp lỗi sau khi thu nhỏ, thêm quy tắc giữ lại lớp hoặc phương thức:
     ```proguard
     -keep class com.myapp.MyModule { *; }
     ```

#### Thực tiễn tốt nhất
- Luôn kiểm tra ứng dụng release trên thiết bị thực tế sau khi áp dụng R8.
- Sử dụng các quy tắc ProGuard từ tài liệu của thư viện bên thứ ba.
- Kết hợp R8 với tree shaking để tối ưu hóa cả mã JS và native.

---

### HƯỚNG DẪN: SỬ DỤNG THƯ MỤC TÀI NGUYÊN NATIVE

Thư mục tài nguyên native (như hình ảnh, font, âm thanh) có thể làm tăng kích thước gói ứng dụng nếu không được quản lý đúng cách. Tối ưu hóa tài nguyên native giúp giảm kích thước APK/IPA và cải thiện TTI.

#### Hướng dẫn tối ưu hóa tài nguyên
1. **Nén tài nguyên**:
   - **Hình ảnh**:
     - Sử dụng công cụ như `ImageOptim` hoặc `TinyPNG` để nén hình ảnh.
     - Chuyển sang định dạng hiện đại như WebP:
       ```xml
       <!-- Trong android/app/src/main/res/drawable -->
       <image src="image.webp" />
       ```
   - **Font**: Chỉ bao gồm các ký tự cần thiết bằng công cụ như `FontSquirrel`.

2. **Loại bỏ tài nguyên không sử dụng**:
   - Trong Android, bật `shrinkResources`:
     ```gradle
     android {
       buildTypes {
         release {
           shrinkResources true
         }
       }
     }
     ```
   - Trong iOS, sử dụng **Asset Catalog** để quản lý tài nguyên và loại bỏ các file không dùng.

3. **Sử dụng tài nguyên theo cấu hình**:
   - **Android**: Cung cấp hình ảnh cho các DPI khác nhau (ldpi, mdpi, hdpi, xhdpi):
     ```plaintext
     android/app/src/main/res/drawable-mdpi/image.png
     android/app/src/main/res/drawable-xhdpi/image.png
     ```
   - **iOS**: Sử dụng `@2x`, `@3x` trong Asset Catalog.

4. **Phân tích kích thước**:
   - Sử dụng **APK Analyzer** hoặc Xcode để kiểm tra kích thước thư mục tài nguyên.
   - So sánh kích thước trước và sau khi tối ưu hóa.

#### Thực tiễn tốt nhất
- Chỉ bao gồm tài nguyên cần thiết cho từng nền tảng.
- Sử dụng các định dạng hiệu quả (WebP cho hình ảnh, TTF tối ưu cho font).
- Kiểm tra tài nguyên trên thiết bị thực tế để đảm bảo chất lượng.

---

### HƯỚNG DẪN: TẮT NÉN GÓI JS

Nén gói JS (JS bundle compression) có thể làm tăng thời gian tải trên một số thiết bị, đặc biệt khi thiết bị phải giải nén gói trong quá trình khởi động. Tắt nén trong một số trường hợp có thể cải thiện TTI.

#### Khi nào nên tắt nén?
- Thiết bị cấp thấp với CPU yếu, nơi giải nén làm chậm khởi động.
- Ứng dụng có gói JS nhỏ, nơi nén không mang lại lợi ích đáng kể.

#### Hướng dẫn tắt nén
1. **Android**:
   - Trong `android/app/build.gradle`:
     ```gradle
     project.ext.react = [
       bundleInRelease: true,
       enableJsBundleCompression: false
     ]
     ```

2. **iOS**:
   - Trong `ios/Podfile`:
     ```ruby
     pod 'React', :path => '../node_modules/react-native', :subspecs => [
       'Core',
       'CxxBridge',
       # Tắt nén
       'RCTBundleCompressionDisabled'
     ]
     ```

3. **Phân tích hiệu quả**:
   - Đo TTI trước và sau khi tắt nén bằng Flipper hoặc React Native Performance.
   - Kiểm tra kích thước gói JS để đảm bảo không tăng quá nhiều.

#### Thực tiễn tốt nhất
- Chỉ tắt nén trên các thiết bị đã xác định có vấn đề về hiệu suất giải nén.
- Kết hợp với các kỹ thuật khác (như code splitting, Hermes) để giảm kích thước gói.
- Kiểm tra hiệu suất trên nhiều thiết bị để đảm bảo cải thiện.

---

## LỜI CẢM ƠN

### VỀ CÁC TÁC GIẢ

Hướng dẫn này được viết bởi đội ngũ tại **Callstack**, một công ty tư vấn và phát triển chuyên về React Native. Các tác giả chính bao gồm:

- **Mike Grabowski**, Nhà sáng lập & CTO của Callstack, với hơn 10 năm kinh nghiệm trong phát triển React Native và đóng góp vào cộng đồng mã nguồn mở.
- **Anna Láng**, Kỹ sư trưởng tại Callstack, chuyên về tối ưu hóa hiệu suất và Kiến Trúc Mới của React Native.
- **Piotr Szlachciak**, Nhà phát triển senior, có chuyên môn sâu về Turbo Modules và Fabric.

Chúng tôi cảm ơn tất cả các thành viên cộng đồng React Native đã cung cấp phản hồi và đóng góp ý tưởng cho hướng dẫn này.

### CÁC THƯ VIỆN VÀ CÔNG CỤ ĐƯỢC ĐỀ CẬP TRONG HƯỚNG DẪN NÀY

Dưới đây là danh sách các công cụ và thư viện được đề cập trong hướng dẫn, cùng với liên kết để bạn tham khảo:

- **React Native DevTools**: Công cụ gỡ lỗi tích hợp cho React Native. [Link](https://reactnative.dev/docs/debugging)
- **Flipper**: Nền tảng gỡ lỗi đa năng cho iOS và Android. [Link](https://fbflipper.com/)
- **Metro Bundle Visualizer**: Phân tích kích thước gói JS. [Link](https://github.com/metro-visualizer)
- **React Native Performance**: Thư viện đo lường hiệu suất. [Link](https://github.com/oblador/react-native-performance)
- **Hermes**: Động cơ JS tối ưu hóa cho React Native. [Link](https://hermesengine.dev/)
- **CodePush**: Tải mã từ xa cho React Native. [Link](https://microsoft.github.io/code-push/)
- **Reanimated**: Thư viện hoạt ảnh hiệu suất cao. [Link](https://docs.swmansion.com/react-native-reanimated/)
- **Jotai**: Quản lý trạng thái nguyên tử. [Link](https://jotai.org/)
- **Turbo Modules**: Mô-đun native thế hệ mới. [Link](https://reactnative.dev/docs/turbo-modules)
- **Fabric**: Trình render mới của React Native. [Link](https://reactnative.dev/docs/fabric)

Chúng tôi khuyến khích bạn khám phá các công cụ này để nâng cao kỹ năng phát triển và tối ưu hóa ứng dụng React Native.

---