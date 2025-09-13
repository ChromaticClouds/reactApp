## 🎨 CSS 전역 변수 관리 (:root)

공통적으로 사용되는 색상, 폰트 크기, 간격 등을
`:root` 선택자 안에서 CSS 변수(`--변수명`)로 정의합니다.

### 📌 사용 규칙
- **반드시 `:root` 안에 정의**하고, 스타일 필드에서는 `var(--변수명)`으로 불러와 사용합니다.
- 색상, 폰트, 간격 등 **재사용되는 값만 등록**합니다.
- 이름은 **의미 기반 네이밍**을 원칙으로 합니다.
  - ❌ `--blue`, `--big-font`  
  - ✅ `--primary-color`, `--font-size-lg`

### 📌 예시 코드

```css
:root {
  /* Colors */
  --primary-color: #1e88e5;
  --secondary-color: #ff9800;
  --surface-color: #f5f5f5;
  --text-color: #333;

  /* Font Sizes */
  --font-size-sm: 12px;
  --font-size-md: 16px;
  --font-size-lg: 20px;

  /* Spacing */
  --spacing-sm: 4px;
  --spacing-md: 8px;
  --spacing-lg: 16px;
}
```

### 📌 사용 방법

```css
.button {
  background-color: var(--primary-color);
  font-size: var(--font-size-md);
  margin: var(--spacing-md);
}
```
