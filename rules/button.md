# Button tag

> Dùng để trigger các hành động xảy ra trong cùng một page.

## `type`

- Tuỳ chọn
- Mặc định là `type="button"`

## `aria-label`

- Bắt buộc
- Nên nêu rõ hành động gì sẽ xảy ra khi click vào button này

---

## Button nằm ngoài `form`

❌ Bad: bị trùng lặp

```html

<button aria-label="Open menu">Open menu</button>
```

❌ Bad: `type="button"` là mặc định nên không cần thiết phải khai báo lại

```html

<button type="button">Open menu</button>
```

✅ Good: descriptive text là "Open menu"

```html

<button>Open menu</button>
```

✅ Good: descriptive text là `aria-label="Open menu"`

```html

<button aria-label="Open menu"><i class="icon-hamburger"></i></button>
```

## Button nằm trong `form`

ℹ️ Info: button với `type="submit"` sẽ trigger form submit khi click vào.

```html

<button type="submit">Send message</button>
```

❌ Bad: do có `type="submit"` nên các element dưới đây cũng có chức năng submit form, dù đúng chức năng và a11y nhưng lại
sai về semantic.

```html
<a href="#" type="submit">Send message</a>

<div type="submit">Send message</div>
```

---

1. W3schools. Accessibility Buttons & Links. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_buttons_links.php