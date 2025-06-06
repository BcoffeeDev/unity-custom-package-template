# Unity custom package template

A Unity custom package template following [Unity's official package layout](https://docs.unity3d.com/6000.1/Documentation/Manual/cus-layout.html), designed for easy reuse, modification, and sharing.

## 📦 Structure Overview

```
com.[company-name].[package-name]/
├── package.json
├── README.md
├── CHANGELOG.md
├── LICENSE.md
├── Third Party Notices.md
├── Editor/
├── Runtime/
├── Tests/
    ├── Runtime/
    ├── Editor/
├── Samples/
└── Documentation~/
```

For detailed structure and conventions, refer to Unity’s documentation:
- Layout: https://docs.unity3d.com/6000.1/Documentation/Manual/cus-layout.html
- `.asmdef`: https://docs.unity3d.com/6000.1/Documentation/Manual/cus-asmdef.html
- Documentation folder: https://docs.unity3d.com/6000.1/Documentation/Manual/cus-document.html
- Changelog format: https://keepachangelog.com/en/1.0.0/

## 🚀 Getting Started

1. Go to the repository's [Releases](https://github.com/your-repo/releases) and download the latest `.zip`.
2. Unzip and rename the folder from `com.[company-name].[package-name]` to your desired package name.
3. Add your preferred `LICENSE.md` to the root folder.
4. Fill in the `package.json` with your package's metadata.
5. Open (or create) a Unity project, navigate to the `Packages/` directory.
6. Move your renamed package folder into the `Packages/` folder.
7. Open Unity. The package should now appear under `Packages/` in the Project window.
8. Add assets (scripts, prefabs, art, etc.) to the appropriate subfolders (`Runtime/`, `Editor/`, etc.) based on Unity's [Package layout](https://docs.unity3d.com/6000.1/Documentation/Manual/cus-layout.html).
9. For any C# code, define assembly definitions (`.asmdef`) based on Unity's [Assembly definition and packages](https://docs.unity3d.com/6000.1/Documentation/Manual/cus-asmdef.html).
10. (Optional) Add or remove supporting files:
    - `README.md`: Package introduction
    - `CHANGELOG.md`: Change history
    - `Third Party Notices.md`: Required notices for dependencies
    - `Documentation~/`: Add documentation in Markdown format

> 📝 Note: If your package does not include scripts, documentation, or samples, you can remove the following folders as needed:
> `Runtime/`, `Editor/`, `Tests/Runtime/`, `Tests/Editor/`, `Samples/`, `Documentation`.

## 📤 Sharing Your Package

You can share this package in two primary ways:

### 1. As a Zip File
- Use your file browser to compress the package folder into a `.zip` file.
- Send it to collaborators or users.

### 2. Via GitHub (Recommended)
- Create a new repository.
- Upload all files and folders (including `.meta` files) from the package directory.
- Users can add your package to their Unity project in either of the following ways:
  - **Modify `manifest.json`**
    ```json
    "dependencies": {
      "com.[company-name].[package-name]": "https://github.com/your-username/your-repo.git"
    }
    ```
  - **Unity Package Manager**
    - Open Unity.
    - Go to **Window → Package Manager**.
    - Click the **+** button → **Add package from Git URL…**
    - Enter: `https://github.com/your-username/your-repo.git`

## 🤝 Contributions & Issues

If you encounter any issues or have ideas for improvements, feel free to:
- Open an issue in this repository.
- Submit a pull request with your suggested changes.

## 📄 License

This package is distributed under the terms of the license provided in `LICENSE.md`. Make sure to include one before sharing.
