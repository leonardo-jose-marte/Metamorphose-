# Metamorphose 🦋

> *El puente definitivo entre la lógica algorítmica y la programación profesional en tiempo real.*

![Fase](https://img.shields.io/badge/Estado-Alfa-orange)
![Licencia](https://img.shields.io/badge/Licencia-MIT-blue)

---

> ⚠️ **Aviso de Estado:** El proyecto **Metamorphose** se encuentra actualmente en **fase de desarrollo activo (Fase Alfa)**. Las características, la estructura del AST y el soporte para los lenguajes están sujetos a cambios frecuentes y refactorización. ¡Las contribuciones y sugerencias son totalmente bienvenidas!

---

## 🎯 Propósito del Proyecto

**Metamorphose** es una aplicación de escritorio de alto rendimiento —inspirada en la agilidad visual de plataformas tipo *CodePen*— concebida para revolucionar la enseñanza y el aprendizaje de la programación.

Su objetivo principal es eliminar la fricción conceptual a la que se enfrentan los estudiantes al dar el salto desde el pseudocódigo básico (compatible con **PSeInt**) hacia lenguajes de programación reales de la industria. Escribes la lógica una sola vez en el panel izquierdo y observas en tiempo real la **metamorfosis sintáctica** estructurada en el lenguaje destino seleccionado.

---

## 🚀 Misión

Nuestra misión es democratizar y acelerar la comprensión lógica del desarrollo de software mediante un entorno interactivo, visual y agnóstico de lenguaje. Buscamos dotar a estudiantes, autodidactas y educadores de una herramienta de escritorio ligera y precisa que traduzca con rigor semántico el pseudocódigo pedagógico a **12 lenguajes de programación clave** (tanto de tipado dinámico como estático), permitiendo no solo ver el cambio de sintaxis, sino también ejecutar y validar los algoritmos de forma segura.

---

## 🔭 Visión

Convertirnos en el estándar de código abierto de referencia global para la introducción a la ciencia de la computación y la transpilación educativa multi-lenguaje. Aspiramos a construir un ecosistema modular extensible impulsado por una arquitectura de *plugins* basada en Árboles de Sintaxis Abstracta (AST), donde cualquier desarrollador pueda integrar nuevos paradigmas y lenguajes, uniendo la simplicidad pedagógica del pseudocódigo con la potencia de la ingeniería de software moderna.

---

## 🛠️ Ecosistema de Lenguajes Soportados

Metamorphose soporta la transpilación y análisis estructurado para un amplio abanico tecnológico dividido en dos grandes bloques:

* **Scripting y Tipado Dinámico:** Python, JavaScript, PHP, Ruby, Lua.
* **Sistemas, Web y Empresa (Tipado Estático):** TypeScript, C, C++, C#, Java, Go, Rust.

---

## ⚙️ Características Técnicas Principales

* **Interfaz de Doble Panel Sincronizado:** Edición fluida con resaltado de sintaxis profesional impulsado por *Monaco Editor*.
* **Motor AST Modular:** Análisis léxico y sintáctico avanzado con validación estricta de tipos de datos y tabla de símbolos.
* **Sandbox de Ejecución Segura:** Consola interactiva integrada con soporte para entradas (`Leer` / `input`) línea por línea y control de procesos mediante límites de tiempo (*timeouts*).
* **Arquitectura Eficiente:** Desarrollado sobre tecnologías nativas de bajo consumo de recursos (Tauri + Rust/Webview).

---

## 🏗️ Arquitectura General

```text
┌───────────────────────────┐      ┌────────────────────────────────┐
│   Panel Izquierdo (UI)    │      │      Panel Derecho (UI)        │
│   Editor PSeInt (.psc)    │      │   Vista Previa Sintaxis (12)   │
└─────────────┬─────────────┘      └───────────────▲────────────────┘
              │ (Debounced Event)                  │
              ▼                                    │
┌──────────────────────────────────────────────────┴────────────────┐
│                     CORE ENGINE (Transpilador)                    │
│   Parser PSeInt ──▶ AST Tipado ──▶ Tabla Símbolos ──▶ Plugins     │
└─────────────┬─────────────────────────────────────────────────────┘
              │ (Ejecución Aislada)
              ▼
┌───────────────────────────────────────────────────────────────────┐
│                  SANDBOX RUNTIME & CONSOLA                        │
│        Procesos Locales / Contenedores + Timeout (5s)             │
└───────────────────────────────────────────────────────────────────┘
```

## 🗺️ Hoja de Ruta (Roadmap)

* [x] Fase 0: Prototipo funcional base (PSeInt → Python).
* [ ] Fase 1: Consolidación del Parser AST y UI base en Tauri + React + Monaco Editor[cite: 3].
* [ ] Fase 2: Soporte inicial para los Big Four (JavaScript, TypeScript, C++, C#)[cite: 3].
* [ ] Fase 3: Motor Sandbox multi-lenguaje y consola interactiva (Stdin/Stdout)[cite: 3].
* [ ] Fase 4: Cobertura completa de los 12 lenguajes (Go, Rust, Java, PHP, Ruby, Lua, C)[cite: 3].
* [ ] Fase 5: Empaquetado nativo multiplataforma (.msi, .deb, .dmg) y CI/CD[cite: 3].

<!--## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si deseas añadir soporte para un nuevo lenguaje o mejorar el análisis del AST:

1. Haz un Fork del repositorio[cite: 3].
2. Crea una rama para tu funcionalidad (`git checkout -b feature/lang-nuevo`)[cite: 3].
3. Realiza tus cambios siguiendo las convenciones de Conventional Commits[cite: 3].
4. Abre un Pull Request detallando la matriz de equivalencia sintáctica[cite: 3].-->

## 📄 Licencia

Distribuido bajo la licencia MIT. Consulta el archivo LICENSE para más información.
