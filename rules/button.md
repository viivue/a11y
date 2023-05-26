# Button tag

> Dùng để trigger các hành động xảy ra trong cùng một page.

## `type`

- Tuỳ chọn
- Mặc định là `type="button"`

## `aria-label`

- Bắt buộc
- Nên nêu rõ hành động gì sẽ xảy ra khi click vào button này

## Accessible name
Ngoài `aria-label`, mỗi thẻ button cần có text bên trong để đảm bảo accessibility. Trong một số trường hợp, do design nên button không có text hiển thị bên ngoài (hamburger button,...) thì đoạn text này có thể đặt trong một thẻ `span` với một số thuộc tính CSS kết hợp để duy trì accessibility nhưng vô hình về mặt hiển thị. Kỹ thuật này còn được biết đến với tên `Visually Hidden`.

Xem thêm về [Visually Hidden](https://www.joshwcomeau.com/snippets/react-components/visually-hidden/).

CSS cho Visually Hidden sẽ được support bởi [atomic-css](https://github.com/viivue/atomic-css), theo dõi PR tại [đây](https://github.com/viivue/atomic-css/issues/24).

```html

<button aria-label="Open menu">
   <i class="icon-hamburger"></i>
   
   <!-- this text is hidden to normal devices but visible for screen readers -->
   <span class="visually-hidden">Open menu</span>
</button>
```

<details><summary>Lighthouse báo lỗi khi thiếu accessible name.</summary>

   ![missing accessible name](https://github.com/viivue/a11y/assets/14942380/6ee60f0f-43eb-4c6e-ad96-3aa65460ce38)
   
</details> 

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
