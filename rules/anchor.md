# `<a>` tag

> Chỉ dùng anchor tag **khi cần điều hướng sang một page khác**. Đối với các tác vụ thực hiện hành động trong cùng một page, hãy sử dụng [[button]].

## `href`

- Bắt buộc
- Không được set `href="#"` hoặc `href=""` hoặc `href="javascript:void(0)"`

## `title`

- Tuỳ chọn (không khuyến khích)
- Chỉ sử dụng khi cần thông báo một nội dung khác với descriptive text thông qua tooltip. Ví dụ thông báo cho user biết
  link này sẽ open in new tab.

## `aria-label`

- Tuỳ chọn
- Không nên dùng chung với `title`

---

## Anchor tag có `<img>` bên trong

❌ Bad: Bị trùng lặp giữa `aria-label` của `<a>` và `alt` của `<img>`

```html
<a href="/home" aria-label="Company logo"><img src="image.png" alt="Company logo"></a>
```

👀 Careful: descriptive text là `alt="Company logo"`, `title` nên có giá trị khác với descriptive text

```html
<a href="/home" title="Go to home page"><img src="image.png" alt="Company logo"></a>
```

✅ Good: descriptive text là `alt="Company logo"`

```html
<a href="/home"><img src="image.png" alt="Company logo"></a>
```

✅ Good: descriptive text là "This is our Company logo"

```html
<a href="/home">This is our <img src="image.png" alt="Company logo"></a>
```

---

## Anchor tag có text bên trong

✅ Good: descriptive text là "Go back to shop page"

```html
<a href="/shop">Go back to shop page</a>
```

❌ Bad: descriptive text và `title` bị trùng lặp

```html
<a href="/shop" title="Go back to shop page">Go back to shop page</a>
```

---

## Anchor tag có SVG bên trong

✅ Good: descriptive text là `aria-label="Go back to shop page"`

```html
<a href="/shop" aria-label="Go back to shop page">
    <svg>...</svg>
</a>
```

---

1. W3schools. Accessibility Buttons & Links. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_buttons_links.php
2. Adrian Roselli (25/06/2021). Link Targets and 3.2.5. Truy cập ngày 25/04/2022
   tại: https://adrianroselli.com/2020/02/link-targets-and-3-2-5.html