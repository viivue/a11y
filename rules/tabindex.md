# Tabindex

> Mọi clickable elements trong trang đều phải tiếp cận được thông qua bàn phím.

Một trong những yếu tố quan trọng trong Web A11y đó là hỗ trợ user sử dụng bàn phím để
nagivate. Xem video dưới đây để thấy cách [github.com](github.com) hỗ trợ Tabindex.

![Tabbing navigation on GitHub](_resources/Screen Recording 2022-05-13 at 15.45.07.mov)

Bấm `Tab` để tiến, `Shift + Tab` để lùi, `Enter` để click, `Space` để toggle.

Có 2 điểm cần lưu ý để một trang web có thể hỗ trợ Tabindex đầy đủ.

## Focus
Mặc định, các element có thể tương tác thì cũng sẽ có focus ([`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a), [`<button>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button), [`<details>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details), [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input), [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select), [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea), etc.). Khi một element có focus, nó sẽ có thể được navigate đến thông qua phím Tab.

### Non-interactive elements
Khi cần focus vào các element mà không có native focus, chúng ta có thể thêm attribute `tabindex="0"`.

```html
<div class="my-element" tabindex="0">
	Focusable element.
</div>
```

`tabindex` có thể nhận nhiều giá trị khác nhau, đọc thêm tại đường link dưới foot note.

## Indication (chỉ thị)
Sử dụng pseudo-selector `:focus-visible` để highlight element đang được focus.

```css
.my-element:focus-visible {
    outline:2px solid #5050ff;
}
```

Khác với `:focus`, `:focus-visible` chỉ hiển thị khi element được focus thông qua phím Tab, vì vậy chúng ta có thể styling cho trạng thái này mà không lo bị ảnh hưởng đến `:focus` có sẵn.

---

1. mdn web docs (27/04/2022). tabindex. Truy cập ngày 13/05/2022 tại https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex