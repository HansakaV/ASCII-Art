# 💻 Animated Terminal Profile Card Generator

Transform your profile picture into beautiful ASCII art and generate an animated terminal-style SVG profile card for your GitHub README. The generator automatically creates both **Dark** and **Light** theme versions, allowing GitHub to switch between them based on the viewer's preferred color scheme.

## ✨ Features

- 🎨 Converts your profile photo into high-quality ASCII art
- 🤖 Automatic background removal using AI (`rembg`)
- 🖼️ Edge detection for enhanced ASCII output
- 🌙 Generates both Dark & Light mode SVG cards
- ⚡ Smooth terminal-style animations
- 📱 Fully responsive SVG output
- 🚀 Perfect for GitHub Profile READMEs
- 🐍 Simple Python-based workflow

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

---

## 2. Add Your Profile Picture

Place a clear profile picture inside the project root directory.

> **Important**
>
> The image **must** be named:

```text
photo.jpg
```

Example project structure:

```text
project/
│
├── photo.jpg
├── photo_to_ascii.py
├── generate_profile.py
└── ...
```

---

## 3. Install Dependencies

Make sure Python 3.10+ is installed.

Then install the required packages:

```bash
pip install pillow numpy rembg onnxruntime
```

---

## 4. Generate ASCII Art

Run the ASCII conversion script:

```bash
python photo_to_ascii.py photo.jpg
```

The script will:

- Remove the background
- Detect edges
- Convert the image into ASCII art
- Generate:

```text
portrait.txt
```

> **Note:** The first run may take a little longer because AI models need to be downloaded.

---

## 5. Customize Your Profile Information

Open:

```text
generate_profile.py
```

Locate the `INFO` array and replace the placeholder values with your own information.

Example:

```python
INFO = [
    ("👨‍💻 Name", "John Doe"),
    ("💼 Role", "Full Stack Developer"),
    ("🌍 Location", "Sri Lanka"),
    ("⚙️ Skills", "Python, React, Next.js"),
    ("📧 Email", "john@example.com")
]
```

You can customize:

- Name
- Role
- Experience
- Skills
- Tech Stack
- Contact Information
- Social Links
- Any additional details

---

## 6. Generate the SVG Profile Cards

Run:

```bash
python generate_profile.py
```

This will generate two optimized animated SVG files:

```text
dark.svg
light.svg
```

---

# 📂 Generated Files

```text
project/
│
├── dark.svg
├── light.svg
├── portrait.txt
└── ...
```

---

# 🌗 Display on Your GitHub Profile

Upload or push the generated SVG files (`dark.svg` and `light.svg`) to your **GitHub Profile Repository** (the repository whose name exactly matches your GitHub username).

Then add the following snippet to your `README.md`:

```html
<div align="center">
  <picture>
    <source
      media="(prefers-color-scheme: dark)"
      srcset="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY/main/dark.svg">

    <source
      media="(prefers-color-scheme: light)"
      srcset="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY/main/light.svg">

    <img
      alt="Animated Terminal Profile"
      src="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY/main/dark.svg">
  </picture>
</div>
```

---

## 🔧 Replace These Values

Before using the HTML snippet, replace:

| Placeholder | Replace With |
|------------|--------------|
| `YOUR_GITHUB_USERNAME` | Your GitHub username |
| `YOUR_REPOSITORY` | Your repository name |

Example:

```text
https://raw.githubusercontent.com/johndoe/terminal-profile/main/dark.svg
```

---

# 📸 Workflow

```text
photo.jpg
      │
      ▼
photo_to_ascii.py
      │
      ▼
portrait.txt
      │
      ▼
generate_profile.py
      │
      ▼
dark.svg
light.svg
      │
      ▼
GitHub Profile README
```

---

# 📦 Requirements

- Python 3.10+
- Pillow
- NumPy
- rembg
- onnxruntime

Install them with:

```bash
pip install pillow numpy rembg onnxruntime
```

---

# 🤝 Contributing

Contributions are always welcome!

If you'd like to improve the project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub. It helps others discover the project and motivates future improvements.

---

Made with ❤️ for developers who love terminal aesthetics.
