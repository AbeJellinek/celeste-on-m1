# Running Celeste on M1 Macs

It's really easy to get Celeste working on M1 Macs, but it requires updating a couple components of the game's engine that are outdated. Here's how.

1. Grab the updated libraries [here](https://github.com/AbeJellinek/celeste-on-m1/releases/download/v1.0/Celeste-M1-Libraries.zip).
2. Extract the ZIP file. The folder structure should look like this:
   ```
   Celeste-M1-Libraries
       FNA.dll
       FNA.dll.config
       osx
           libFAudio.0.dylib
           libFNA3D.0.dylib
           [...]
           libvulkan.1.dylib
   ```
3. Now go find Celeste on your disk. In Steam, you can locate it by right-clicking on it in the list and choosing *Properties* -> *Local Files* -> *Browse...*.
4. Right-click on Celeste and choose *Show Package Contents*, then go to `Contents/MacOS`. You should see a bunch of files in the `MacOS` folder, including some called `Celeste` and `Celeste.exe` and a folder called `osx`.
5. Copy `FNA.dll` and `FNA.dll.info` from the ZIP into the `MacOS` folder. When it asks if you want to replace the existing files, say yes.
6. Copy everything from the `osx` folder in the ZIP into the `MacOS/osx` folder. Again, replace.
7. You're done! Run the game.

##### Building (optional)

If you'd like to build the libraries yourself, you absolutely can. I grabbed the FNA code from [here](https://github.com/FNA-XNA/FNA) and built it with Visual Studio, and used [XnaToFna's prebuilt binaries](https://github.com/0x0ade/XnaToFna/releases) for the natives.

#### Licenses

[FAudio](https://github.com/FNA-XNA/FAudio/blob/master/LICENSE), [FNA3D](https://github.com/FNA-XNA/FNA3D/blob/master/LICENSE), [SDL](http://hg.libsdl.org/SDL/file/d3837b234ed8/COPYING.txt), and [Theorafile](https://github.com/FNA-XNA/Theorafile/blob/master/licenses/LICENSE) are licensed under the Zlib License. [FNA itself](https://github.com/FNA-XNA/FNA/blob/master/licenses/LICENSE) is licensed under the Microsoft Public License. [MoltenVK](https://github.com/KhronosGroup/MoltenVK/blob/master/LICENSE) and [Vulkan](https://github.com/KhronosGroup/Vulkan-Headers/blob/master/LICENSE.txt) are licensed under the Apache License. All libraries are copyright their respective authors and provided here only for convenience's sake. This repo contains no binaries or code from Celeste itself, only the free, open-source libraries it uses.