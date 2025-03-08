# Tổng Quan về Thư Viện `java.util` trong Java

Thư viện `java.util` là một gói quan trọng trong Java, cung cấp rất nhiều công cụ và lớp hữu ích cho việc xử lý dữ liệu, làm việc với ngày tháng, thời gian, và các thao tác thông dụng khác. Dưới đây là cái nhìn tổng quan về các nhóm chức năng chính mà thư viện này hỗ trợ.

## 1. Collection Framework (Công Cụ Tập Hợp)

Java cung cấp một hệ thống mạnh mẽ để làm việc với các tập hợp (collections), bao gồm danh sách, tập hợp, bản đồ, và các công cụ giúp thao tác với chúng.

### Các lớp và giao diện chính:
- **List**: Là một tập hợp có thứ tự, cho phép lưu trữ các phần tử trùng lặp.
  - **ArrayList**: Một danh sách động, có thể thay đổi kích thước, dễ dàng truy cập phần tử theo chỉ số.
  - **LinkedList**: Một danh sách liên kết, nhanh hơn khi thêm hoặc xóa phần tử ở đầu hoặc cuối.
  
- **Set**: Là một tập hợp không có phần tử trùng lặp.
  - **HashSet**: Một tập hợp không bảo đảm thứ tự, hoạt động nhanh cho việc tìm kiếm.
  - **TreeSet**: Một tập hợp có sắp xếp theo thứ tự tự nhiên hoặc theo một bộ so sánh (comparator).

- **Queue**: Là một tập hợp cho phép thêm và lấy phần tử theo cách FIFO (First In First Out).
  - **PriorityQueue**: Một hàng đợi ưu tiên, nơi các phần tử được sắp xếp theo một thứ tự nhất định.

- **Map**: Là một cấu trúc lưu trữ cặp khóa-giá trị, mỗi khóa là duy nhất.
  - **HashMap**: Bản đồ sử dụng bảng băm để lưu trữ các cặp khóa-giá trị, không bảo đảm thứ tự.
  - **TreeMap**: Bản đồ có sắp xếp, đảm bảo các khóa được lưu trữ theo thứ tự tự nhiên hoặc theo một comparator.

## 2. Date and Time API (Lịch và Thời Gian)

Trước Java 8, việc làm việc với thời gian và ngày tháng là rất khó khăn vì lớp `Date` và `Calendar` có một số vấn đề và thiếu sót. Java 8 đã giới thiệu một API mới mạnh mẽ hơn và dễ sử dụng.

- **java.time** (Java 8 trở lên): Cung cấp các lớp như `LocalDate`, `LocalTime`, `LocalDateTime`, và `ZonedDateTime` để làm việc với ngày tháng và thời gian mà không gặp phải những vấn đề của các lớp cũ.
- **Instant**: Đại diện cho một mốc thời gian cụ thể (timestamp).
- **Duration và Period**: Dùng để tính toán khoảng thời gian giữa các mốc thời gian.

## 3. Utility Classes (Các Lớp Tiện Ích)

Thư viện `java.util` cung cấp nhiều lớp tiện ích để thực hiện các tác vụ thường gặp trong lập trình.

- **Collections**: Một lớp tiện ích với các phương thức tĩnh để thao tác với các collection như sắp xếp, đảo ngược, tìm kiếm, v.v.
  - Ví dụ: `Collections.sort(list)`, `Collections.shuffle(list)`, `Collections.reverse(list)`.

- **Arrays**: Cung cấp các phương thức để thao tác với mảng.
  - Ví dụ: `Arrays.sort(arr)`, `Arrays.copyOf(arr)`, `Arrays.toString(arr)`.

- **Random**: Lớp tạo số ngẫu nhiên, hữu ích cho các tác vụ như tạo số ngẫu nhiên hoặc chọn ngẫu nhiên phần tử từ danh sách.
- **UUID**: Dùng để tạo các mã nhận dạng duy nhất toàn cầu (UUID).
- **Optional**: Giúp xử lý các giá trị có thể null, tránh các lỗi `NullPointerException`.

## 4. Iterator và Spliterator

- **Iterator**: Giao diện giúp duyệt qua các phần tử trong một tập hợp. Bạn có thể sử dụng phương thức `next()`, `hasNext()` để duyệt qua tập hợp.
- **Spliterator**: Được giới thiệu trong Java 8, giao diện này cung cấp khả năng chia nhỏ các tập hợp lớn thành các phần nhỏ hơn, hữu ích cho việc xử lý song song.

## 5. Concurrency Utilities (Các Tiện Ích Đồng Thời)

Java cung cấp các công cụ đồng thời để xử lý các tác vụ đa luồng, như `java.util.concurrent`.

- **Executor**: Làm việc với các công việc chạy đồng thời, ví dụ như `ExecutorService`.
- **CountDownLatch**, **CyclicBarrier**: Hỗ trợ đồng bộ giữa các luồng.
- **Semaphore**: Giới hạn số lượng luồng truy cập vào một phần của ứng dụng.

## 6. Các Lớp Khác

- **Properties**: Lớp dùng để lưu trữ các thuộc tính, thường là các cặp khóa-giá trị, hữu ích cho việc cấu hình ứng dụng (tương tự như các tệp cấu hình `.properties`).
- **Stack**: Lớp mô phỏng một ngăn xếp (stack), cho phép thao tác với các phần tử theo kiểu LIFO (Last In, First Out).

---

## Tổng Kết về Thư Viện `java.util`

Thư viện `java.util` cung cấp các cấu trúc dữ liệu cơ bản và các công cụ hữu ích để làm việc với tập hợp, ngày giờ, các tác vụ đồng thời và các tiện ích khác. Nó là một phần quan trọng trong Java, đặc biệt là trong các ứng dụng có yêu cầu xử lý dữ liệu phức tạp hoặc yêu cầu tối ưu hóa hiệu suất.

- `java.util` hỗ trợ các thao tác đơn giản như sắp xếp mảng hay làm việc với thời gian, lẫn các tính năng phức tạp hơn như xử lý đồng thời và tạo số ngẫu nhiên.
