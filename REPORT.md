# 📌 Rättningsrapport – fed24s-the-zoo-isabellavelasquez

## 🎯 Uppgiftens Krav:
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default tseslint.config({
  extends: [
    // Remove ...tseslint.configs.recommended and replace with this
    ...tseslint.configs.recommendedTypeChecked,
    // Alternatively, use this for stricter rules
    ...tseslint.configs.strictTypeChecked,
    // Optionally, add this for stylistic rules
    ...tseslint.configs.stylisticTypeChecked,
  ],
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config({
  plugins: {
    // Add the react-x and react-dom plugins
    'react-x': reactX,
    'react-dom': reactDom,
  },
  rules: {
    // other rules...
    // Enable its recommended typescript rules
    ...reactX.configs['recommended-typescript'].rules,
    ...reactDom.configs.recommended.rules,
  },
})
```


## 🔍 ESLint-varningar:
- C:\Work\AssignmentCorrector\backend\repos\fed24s-the-zoo-isabellavelasquez\src\helpers\animalsHelper.ts - no-unused-vars - 'FULL' is defined but never used.,no-unused-vars - 'ALMOST_HUNGRY' is defined but never used.,no-unused-vars - 'HUNGRY' is defined but never used.,no-unused-vars - 'STARVING' is defined but never used.
- C:\Work\AssignmentCorrector\backend\repos\fed24s-the-zoo-isabellavelasquez\src\reducers\animalReducer.ts - no-unused-vars - 'FED' is defined but never used.,no-unused-vars - 'FETCHED' is defined but never used.

## 🏆 **Betyg: G**
📌 **Motivering:** Koden täcker grundläggande krav för React + TypeScript + Vite. Den använder useContext och useReducer effektivt för globalt tillståndshantering och React Router för navigering. Dock finns det små förbättringsmöjligheter som kan höja kvaliteten.

💡 **Förbättringsförslag:**  
Det finns några kodkvalitetsaspekter som kan förbättras. En klar förbättring skulle vara att lägga till testning för komponenterna och använda PropTypes för att validera filtreringslogik. Felhantering i API-anropen kan stärkas genom att hantera exceptions vid asynkrona operationer. Dessutom skulle ESLint-konfigurationen kunna utökas med type-aware lint regler för att säkerställa en ännu striktare typkontroll.