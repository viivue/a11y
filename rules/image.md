# Img tag

## `src`

- Bắt buộc

## `alt`

- Bắt buộc

## `title`

- Tuỳ chọn (không khuyến khích)

---

❌ Bad: descriptive text là `src="image.png"`

```html
<img src="image.png">
```

❌ Bad: descriptive text là `src="/assets/img/company-logo.png"`

```html
<img src="/assets/img/company-logo.png">
```

❌ Bad: trùng lặp

```html
<img src="image.png" alt="Company logo" title="Company logo">
```

✅ Good: descriptive text là "Company logo"

```html
<img src="image.png" alt="Company logo">
```

---

1. W3schools. Accessibility Meaningful & Decorative Images. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_meaningful_images.php
2. W3schools. Accessibility Descriptive Texts for Images. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_image_text.php