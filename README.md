# Đếm ngược sự kiện

Đếm ngược tới một ngày bất kỳ do bạn đặt: khai trương, ra mắt, kỷ niệm thành lập.

*[Read this in English](README.en.md)*

**Xem nó chạy thật:** https://nhatnguyet.org/widget/dem-nguoc

## Dán hai dòng này là xong

```html
<div data-widget="dem-nguoc"></div>
<script async src="https://nhatnguyet.org/embed/w.js"></script>
```

Không cần tài khoản, không cần khoá API, không mất phí.

## Nó giúp gì cho trang của bạn

Bản tổng quát của Đếm ngược Tết: thay vì cố định ở mùng Một, bạn đặt ngày nào cũng được qua data-ngay-den. Widget biết ba trạng thái, đang đếm, đúng ngày, và đã qua, nên nó không rơi vào cảnh đếm về 0 rồi đứng im ở đó.

## Vài điều nên biết trước

- Hai thuộc tính bắt buộc: ngày đích và tên sự kiện. Thiếu cái nào widget nói rõ thiếu cái đó, không hiện số bịa.
- Qua ngày sự kiện, widget đổi sang dòng đã diễn ra chứ không tự xoá mình khỏi trang.
- Số ngày tính theo lịch giờ Việt Nam, nên mọi người xem cùng ngày đều thấy cùng một con số.

## Các bước

1. Đặt data-ngay-den theo dạng năm-tháng-ngày, ví dụ 2027-03-15.
2. Đặt data-ten-su-kien là tên hiện cạnh số đếm, tối đa 60 ký tự.
3. Qua ngày rồi thì gỡ hoặc để lại tuỳ bạn, widget không tự biến mất.

## Dán vào đâu

**WordPress.** Thêm một khối *HTML tuỳ chỉnh* vào bài hoặc vào widget
*Text* ở cột bên, rồi dán cả hai dòng vào đó. Đừng dán vào trình soạn thảo
thường: nó sẽ hiện ra đúng chữ mã thay vì chạy mã.

**Wix, Squarespace, Haravan, Shopify.** Dùng khối *Nhúng mã HTML* (Embed
HTML / Custom HTML) rồi dán vào.

**Site tự viết.** Dán thẳng vào chỗ bạn muốn widget xuất hiện. Dòng
`<script>` có thể để chung một chỗ nếu bạn nhúng nhiều widget, nó chỉ cần
xuất hiện một lần trên trang.

**Ghi chú về chiều rộng.** Widget tự co theo bề ngang chỗ bạn đặt nó. Nếu chỗ ấy hẹp dưới 280px thì thêm `data-size="compact"`;
nếu là một dải ngang rộng thì `data-size="wide"`.

## Chỉnh cho hợp trang của bạn

| Thuộc tính | Giá trị | Ý nghĩa |
|---|---|---|
| `data-widget` | `dem-nguoc` | Bắt buộc |
| `data-theme` | light hoặc dark | Mặc định light |
| `data-accent` | #b3341f | Màu nhấn dạng hex 6 ký tự, để khớp bộ nhận diện của bạn |
| `data-lang` | vi hoặc en | Mặc định vi |
| `data-size` | compact, standard hoặc wide | Mức chi tiết theo bề ngang khung: compact bỏ bớt chi tiết phụ, wide trải ngang. Mặc định standard |
| `data-ngay-den` | 2027-03-15 | Ngày đích của widget đếm ngược sự kiện, dạng năm-tháng-ngày. Bắt buộc với widget đó |
| `data-ten-su-kien` | Khai trương chi nhánh 2 | Tên hiện cạnh số đếm ngược, tối đa 60 ký tự. Bắt buộc với widget đếm ngược sự kiện |

Đặt hết mọi thứ widget này nhận thì trông như sau:

```html
<div data-widget="dem-nguoc" data-theme="dark" data-accent="#1f6f5c" data-size="compact" data-ngay-den="2027-03-15" data-ten-su-kien="Khai truong chi nhanh 2"></div>
<script async src="https://nhatnguyet.org/embed/w.js"></script>
```

Muốn xem tận mắt trước khi dán lên trang thật thì mở
[`vi-du/index.html`](vi-du/index.html) bằng trình duyệt, không cần cài gì.

## Vài điều xin thưa trước

- Miễn phí cho website cá nhân và doanh nghiệp, không giới hạn lượt hiển thị.
- Giữ nguyên dòng ghi nguồn ở đáy widget. Đây là điều kiện đổi lại việc dùng
  miễn phí.
- Không nhúng trên trang cờ bạc, nội dung người lớn, lừa đảo hoặc vi phạm
  pháp luật Việt Nam.
- Nội dung là tri thức dân gian và quy ước văn hoá, để tham khảo, không phải
  lời khuyên về sức khoẻ, tài chính hay pháp lý.

Bản đầy đủ: [`DIEU-KHOAN.md`](DIEU-KHOAN.md) · [https://nhatnguyet.org/widget/dieu-khoan](https://nhatnguyet.org/widget/dieu-khoan)

## Nhật Nguyệt là ai

Nhật Nguyệt (https://nhatnguyet.org) là trang tra cứu lịch pháp và văn hoá tâm linh Việt
Nam: lịch âm tính theo múi giờ nước mình, can chi, tiết khí, giờ hoàng đạo,
tử vi, phong thuỷ, và một từ điển thuật ngữ.

Có một điều chúng tôi cố giữ cho bằng được, kể cả trong một khung widget
300px: nói rõ đâu là thứ tính ra được, đâu là quan niệm dân gian.

Ngày âm lịch, can chi, tiết khí là **tính ra được**: ai chạy cùng phép tính
cũng ra cùng kết quả, và chúng tôi công bố luôn bộ dữ liệu gốc theo giấy
phép CC BY 4.0 để bạn tự đối chiếu.

Giờ hoàng đạo, cung Bát Trạch, cung thước Lỗ Ban là **quy ước văn hoá**: có
bảng tra hẳn hoi, nhưng không phải phép đo. Widget cho bạn biết bảng nói gì,
còn tin tới đâu là việc của mỗi người.

Chỗ nào các phái không thống nhất, chúng tôi nói ra chỗ ấy, thay vì lặng lẽ
chọn một bên rồi trình bày như thể chỉ có một cách.

Dữ liệu mở: [GitHub](https://github.com/taman-spirit/du-lieu-am-lich) ·
[Hugging Face](https://huggingface.co/datasets/nhatnguyet)

## Thấy gì chưa ổn?

Mở một issue ngay trong kho này. Chúng tôi có đọc.

Toàn bộ thư viện widget: [https://nhatnguyet.org/widget](https://nhatnguyet.org/widget)
