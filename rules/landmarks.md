# Landmarks

Dưới đây là 6 landmark tag và role mặc định của nó (lưu ý rằng role mặc định không cần thiết phải khai báo lại):

- `<main role="main">`
- `<header role="banner">`
- `<footer role="contentinfo">`
- `<nav role="navigation">`
- `<aside role="complementary">`
- `<section role="region">`

---

ℹ️ Info: `<main>` chỉ nên xuất hiện một lần trong một page, các thẻ landmark còn lại có thể xuất hiện nhiều lần
với `role` và `aria-label` phù hợp.

ℹ️ Info: `<nav>`, `<aside>` và `<section>` nên nằm trong `<main>`

---

## `<main>`

- `role="main"`

## `<header>`

- `role="banner"` khi nằm trong `<body>`
- `role="generic"` khi nằm trong `<aside>`, `<main>`, `<nav>`, `<section>`,  `<article>`

## `<footer>`

- `role="contentinfo"`

---

## `<nav>`

- `role="navigation"`

✅ Good

```html
<main>
	<nav aria-label="Main menu"></nav>

	<nav aria-label="Product tabs content navigation"></nav>

	<nav aria-label="Footer menu"></nav>
</main>
```

---

## `<aside>`

- `role="complementary"`
- Chứa những element có liên quan đến `<main>` (không nhất thiết phải là sidebar).

✅ Good

```html

<main>
    <aside aria-label="Product filter sidebar"></aside>

    <aside aria-label="Share this product"></aside>
</main>
```

👀 Careful: đúng về a11y nhưng không hợp lý về semantic

```html

<main>
    <div role="complementary" aria-label="Product filter sidebar">
    </div>

    <div role="complementary" aria-label="Share this product">
    </div>
</main>
```

---

## `<section>`

- `role="region"`

✅ Good

```html
<main>
	<section aria-label="Featured product">
		<nav aria-label="Category navigation"></nav>
		<div role="contentinfo">
			<article></article>
			...
		</div>
		<nav aria-label="Bottom navigation">
			<a href="/shop">View more products</a>
		</nav>
	</section>
	
	<section aria-label="Newsletter"></section>
</main>
```

---

1. W3schools. Accessibility Landmarks. Truy cập ngày 25/04/2022
   tại: https://www.w3schools.com/accessibility/accessibility_landmarks.php
2. mdn web docs (12/04/2022). WAI-ARIA Roles. Truy cập ngày 25/04/2022
   tại: https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles
3. mdn web docs (18/02/2022). The Aside element. Truy cập ngày 25/04/2022
   tại: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside