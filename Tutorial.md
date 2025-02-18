## Launcher Tutorial
Exode Launcher is based on an open-source launcher called Helios Launcher.

#### 1. Change the Logo: 
[![](https://i.postimg.cc/8P6WfR5X/image.png)](https://i.postimg.cc/8P6WfR5X/image.png)

You can find the logo in: `app/assets/images/SealCircle.png`, along with all other launcher icons. Get your image, rename it to `SealCircle`, and ensure it is in `.png` format.

------------

#### 2. Change the App Name: 
[![](https://i.postimg.cc/Y0Vsn6Ky/image.png)](https://i.postimg.cc/Y0Vsn6Ky/image.png)

If you are using Visual Studio Code or any other text editor, select "Search" (or its equivalent in the software you are using) and search for the current launcher name. Enable "Match Case," go through each result, and replace it with your desired name.

------------

#### 3. Change the Data Directory:
[![](https://i.postimg.cc/Fsry8dsT/image.png)](https://i.postimg.cc/Fsry8dsT/image.png)

You can find the data directory line in `app\assets\js\configmanager.js` at line 10, as shown below:
[![](https://i.postimg.cc/s2Y13mT7/image.png)](https://i.postimg.cc/s2Y13mT7/image.png)

If the changes do not take effect, delete `.helioslauncher`, `Helios Launcher`, `.exodelauncher`, and `Exode Launcher`. That should resolve the issue!

------------

#### 4. Change the Launcher Background: 
[![](https://i.postimg.cc/wB18Vjmv/image.png)](https://i.postimg.cc/wB18Vjmv/image.png)

To change the launcher's background, go to `app\assets\images\backgrounds\0.jpg` and replace it with your desired background image. Ensure that the format is `.jpg` and that the file name is `0`.

------------


#### 5. Change Editor Text/Language: 
[![](https://i.postimg.cc/9XbQYGF4/image.png)](https://i.postimg.cc/9XbQYGF4/image.png)

To change the launcher's text, go to `app\assets\lang\en_US.toml` and edit each variable/text with your desired text. There is also `app\assets\lang\_custom.toml` that contains all your social media links and welcome messages.

------------

#### 6. Change The Server Address
Need help with Nebula?
Here is TL;DR guide
1. [Download](https://github.com/dscalzi/Nebula) Nebula using Github's zip method, or using Git
2. Install dependancies using `npm i`
3. Create .env file with the following values, then edit it to suit your needs
`JAVA_EXECUTABLE=C:\Program Files\AdoptOpenJDK\jdk-16.0.1.9-hotspot\bin\java.exe`

	`ROOT=D:\TestRoot2`

	`BASE_URL=http://localhost:8080/`

	`HELIOS_DATA_FOLDER=C:\Users\user\AppData\Roaming\Helios Launcher`
	
	JAVA_EXECUTABLE is the path to your java.exe file. ROOT is a path to an empty folder where you will get your nebula files. BASE_URL is the first part of the url where you will be able to download the files. HELIOS_DATA FOLDER is the path to the directory that contains distribution.json, settings etc.

4. Create your distribution root with `npm start -- init root`
5. Create your server using `npm start -- generate server [server name] [Minecraft Version eg 1.12.2] --forge [forge version eg 14.23.5.2859]`. Please note Forge is required.
6. Put your mods, and libraries in folder ROOT\servers\yourserver-mcversion
7. Generate distro `npm start -- generate distro`
8. Upload generated files in your web server
9. On your launcher, in `app/assets/js/distromanager.js` on line 7, edit the url to match your own distribution.json url


> **Using a text/code editor with a "Search All Files" feature will significantly help in searching and editing the required values.**