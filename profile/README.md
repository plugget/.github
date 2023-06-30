## Plugget
Plugget aims to make it really easy to distribute tools and plugins & supports various apps: Maya, 3ds-Max, Blender, Krita, Unreal, ...   
Install app packages (plugins, addons, icons, ...) from a repo with a single Python command  
```python
import plugget
plugget.install("my_package")
```


These repos implement different dcc's:

- [plugget](https://github.com/plugget/plugget)  The core Python module with all package download logic
- [plugget-pkgs](https://github.com/plugget/plugget-pkgs)  The standard manifest repo for plugget packages
- [plugget-blender-addon](https://github.com/plugget/plugget-blender-addon)  An addon to use plugget in Blender with a standard Blender UI.
- [plugget-qt](https://github.com/plugget/plugget-qt)  A generic Qt UI window to install plugget packages, that can be used in any apps with Python.
  - [plugget-unreal](https://github.com/plugget/plugget-unreal)  An Unreal plugin that launches a Qt UI window
  - [plugget-qt-addon](https://github.com/plugget/plugget-qt-addon)  A Blender addon that launches a Qt UI window


### package manager comparison
Let's compare existing package managers, to help you understand if you need Plugget:  

Why not use PyPI?
- PyPI only installs packaged python modules. But many Blender scripts are not packaged, e.g. [this](https://github.com/absolute-quantum/cats-blender-plugin) addon.
- Addons are not supposed to be installed as a Python module. A pip install would install them to site packages, isntead of in the addons folder.
- Using pip, is not something users are comfortable with. Only devs who know git will use this. Plugget targets casual users, e.g. artists, who prefer a UI instead of a console.
- Plugget also supports other languages than Python, e.g. Maxscript & Unreal plugins

What about WinGet, chocolatey, etc? These solutions install `apps`, Plugget installs  `plugins for apps`
I believe it might be possible to use e.g. Chocolatey and use install scripts to install a plugin, however it seems quite complex to me. And Chocolatey wasn't really designed for this.

### Bugs 

It's still in active development, so if you find any issues, open an issue on the GitHub repo and we'll get back to you.