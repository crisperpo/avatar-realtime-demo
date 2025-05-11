# Avatar Realtime Demo

🚧 **Work in Progress**

This project is a demonstration of real-time avatar streaming, built with React, Vite, and TypeScript. It aims to showcase the integration of real-time technologies to create interactive avatar experiences.

## 🛠️ Technologies Used

- **Frontend**: React, Vite, TypeScript, Heygen
- **Backend**: Node.js (Express)
- **Styling**: SCSS
- **Linting**: ESLint

## 🚀 Getting Started

1. **Clone the repository**:

   ```bash
   git clone https://github.com/crisperpo/avatar-realtime-demo.git
   cd avatar-realtime-demo
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Set up environment variables**:

   Create a `.env` file in the root directory based on the `.env.example` file.

4. **Run the development server**:

   ```bash
   npm run dev
   ```

   The application will be available at [http://localhost:5173](http://localhost:5173).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```

## 📄 License

This project is licensed under the [MIT License](LICENSE).

Built by [@crisperpo](https://github.com/crisperpo) with 💡
