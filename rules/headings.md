# Headings

Có 6 heading tags bao gồm từ `<h1>` tới `<h6>`. Trong mỗi page cần đảm bảo các điều kiện tiên quyết dưới đây:

1. Tồn tại duy nhất một `<h1>` và phải nhìn thấy được.
2. Các headings phải phân cấp theo thứ tự.

---

❌ Bad:

- `<h3>Sticky article 1</h3>` và `<h4>Article 2</h4>` đều cùng là các article thuộc section "Breaking news" nên phải có
  heading cùng cấp.
- Thiếu `<h3>` khi giật cấp từ `<h2>Hot Topics</h2>` xuống `<h4>Article 4</h4>`.

```html
<h1>The New York Times</h1>

<h2>Breaking news</h2>

<h3>Sticky article 1</h3>
<h4>Article 2</h4>
<h4>Article 3</h4>

<h2>Hot Topics</h2>

<h4>Article 4</h4>
<h4>Article 5</h4>
<h4>Article 6</h4>
```

✅ Good: headings phân cấp theo thứ tự

```html
<h1>The New York Times</h1>

<h2>Breaking news</h2>

<h3>Article 1</h3>
<h3>Article 2</h3>
<h3>Article 3</h3>

<h2>Hot Topics</h2>

<h3>Article 4</h3>
<h3>Article 5</h3>
<h3>Article 6</h3>
```

---
Tham khảo:

1. W3schools. Accessibility Headings Introduction. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_headings_intro.php
2. Dennis Deacon (24/03/2020). Headings & Accessibility. Truy cập ngày 25/04/2022
   tại: https://www.tpgi.com/headings-accessibility