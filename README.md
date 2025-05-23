# 📘 Plantilla LaTeX para Monografías — UMSA

Este repositorio contiene una plantilla en LaTeX diseñada para la elaboración de monografías académicas o tesis en la Universidad Mayor de San Andrés (UMSA).

---

## 📁 Estructura del repositorio

```
umsa_latex_template/
├── main.tex            # Documento principal en LaTeX
├── bibliography.bib    # Archivo de referencias en formato BibTeX (APA)
├── images/             # Carpeta para logos o figuras
├── .gitignore
└── README.md
```

---

## 📚 Características

- Documento en un solo archivo (`main.tex`)
- Citas y referencias en formato APA con `biblatex` y `biber`
- Soporte para imágenes locales (como el logo de la UMSA)
- Listo para compilar con `pdflatex` y `biber`

---

## ⚙️ Requisitos

Asegúrate de tener instalados los siguientes componentes:

- [TeX Live](https://www.tug.org/texlive/) (2023 o posterior)
- `biber` (para procesar la bibliografía APA)

En sistemas Debian/Ubuntu puedes instalar con:

```bash
sudo apt install texlive-full biber
```

En macOS con Homebrew:

```bash
brew install --cask mactex-no-gui
```

---

## 🚀 Cómo compilar

Desde la raíz del proyecto, ejecuta los siguientes comandos:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Esto generará el archivo `main.pdf` con las citas y bibliografía correctamente formateadas.

---

## 📚 Ejemplo de entrada BibTeX (`bibliography.bib`)

```bibtex
@book{perez2021,
  author    = {Pérez, Juan},
  title     = {Educación digital en América Latina},
  year      = {2021},
  publisher = {Editorial UMSA},
  langid    = {spanish}
}
```

---

## ✍️ Citas en el texto

- Cita narrativa:

  ```latex
  \textcite{perez2021} analiza el impacto de la tecnología en la educación.
  ```

- Cita entre paréntesis:

  ```latex
  \parencite{perez2021}
  ```

---

## 🖼️ Inclusión de imágenes

Coloca tus imágenes en la carpeta `images/` y usa rutas relativas como esta:

```latex
\includegraphics[width=4cm]{images/logo_umsa.png}
```

---

## 🌐 Uso en Overleaf

Si no deseas instalar LaTeX localmente, puedes compilar esta plantilla en línea utilizando [Overleaf](https://www.overleaf.com), una plataforma gratuita para editar documentos LaTeX en la nube.

### Instrucciones:

1. Crea una cuenta gratuita en [overleaf.com](https://www.overleaf.com).
2. Haz clic en **"New Project" > "Upload Project"**.
3. Carga todo el contenido de la carpeta `umsa_latex_template/`, incluyendo el archivo `main.tex`, `bibliography.bib` y la carpeta `images/`.
4. Asegúrate de que el archivo principal sea `main.tex`.
5. En el menú superior, selecciona **"Compiler"** y elige `XeLaTeX` o `pdfLaTeX`.
6. Haz clic en **"Recompile"** para generar el PDF.

Puedes revisar el resultado final en el archivo `main.pdf` incluido en este repositorio como referencia.

---

## 📄 Licencia

Este proyecto está licenciado bajo la [Licencia MIT](LICENSE). Puedes usarlo, modificarlo y distribuirlo libremente para fines académicos.

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Puedes hacer un fork de este repositorio y enviar un pull request con tus mejoras o adaptaciones.
