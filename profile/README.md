# Plugget
Plugget simplifies distributing your tools & plugins.  
- Supports: Maya, 3ds-Max, Blender, Krita, Unreal, ...
- Create private tool distribution lists for in-house pipelines, or search open source tools  
  
Stop struggling with Perforce to distribute your tools, or forcing your Art-team to use Git.  
Plugget handles the technical part⚡, and you create awesome tools for your team. 💪  

## Quickstart

Install your packages (plugins, addons, icons, ...) from a repo with a single Python command:
```python
import plugget
plugget.install("my_package")
```
_This code downloads the manifest from the public plugget repo,  
reads the manifest for the source URL & install instructions,  
and installs the plugin or addon to the correct folder._

## Repos

#### Core repos:
- [plugget](https://github.com/plugget/plugget)  The core Python module with all package download logic
- [plugget-pkgs](https://github.com/plugget/plugget-pkgs)  The standard manifest repo for plugget packages

#### UI wrappers for apps:
- [plugget-blender-addon](https://github.com/plugget/plugget-blender-addon)  An addon to use plugget in Blender with a standard Blender UI.
- [plugget-qt](https://github.com/plugget/plugget-qt)  A generic Qt UI window to install plugget packages, that can be used in any apps with Python.
  - [plugget-unreal](https://github.com/plugget/plugget-unreal)  An Unreal plugin that launches a Qt UI window
  - [plugget-qt-addon](https://github.com/plugget/plugget-qt-addon)  A Blender addon that launches a Qt UI window

<br>

### Why not use ... instead?
<details close><summary>🔍 Package managers compared</summary><blockquote>
  
Let's compare existing package managers, to help you understand if you need Plugget:  

Why not use PyPI?
- PyPI only installs packaged python modules. But many Blender scripts are not packaged, e.g. [this](https://github.com/absolute-quantum/cats-blender-plugin) addon.
- Addons aren't meant to be installed as Python packages. Pip installs to `site packages`, instead of `addons`.
- Plugget targets casual users who prefer a UI instead of a console. 
- Plugget also supports other languages than Python, e.g. Maxscript & Unreal plugins

What about WinGet, chocolatey, etc? These solutions install `apps`, Plugget installs  `plugins for apps`  
It might be possible to use Chocolatey's install scripts to install a plugin, however it seems complex, and Chocolatey wasn't designed for this.

</blockquote></details>
