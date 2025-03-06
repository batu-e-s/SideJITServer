# HOW TO INSTALL FOR WINDOWS - NOOB GUIDE

If you are new to technology and need a simple guide, this is for you! Let's get started.

## Step 1: Installing Python

Download [this](https://www.python.org/downloads/release/python-3119/) file and run the setup. Make sure to check the option **"Add Python to PATH"**—this is very important!

## Step 2: Downloading iTunes

Download iTunes from [here](https://www.apple.com/itunes/download/win64). After installing, open **Apple Software Update** and check for updates to ensure you have the latest version.

## Step 3: Configuring Your Device

1. Connect your iPhone to your PC using a USB cable.
2. Open **iTunes**.
3. Click on your phone's icon when it appears in iTunes.
4. Scroll down and check the box **"Access This iPhone Over Wi-Fi"**.
5. Click **Apply**.
6. Disconnect your iPhone and check if it remains connected in iTunes.

## Step 4: Downloading SideJITServer

Now this step is a bit tricky. follow these carefully. Do not just blindly copy and paste.
1. Go to the project’s main page and click the green **"Code"** button, then select **Download ZIP**.
2. Extract the ZIP file to a folder.
3. Open the extracted folder and check its path. It should look like:
   ```
   C:/Users/YOUR_USERNAME/SideJITServer
   ```
4. Make sure you didn’t accidentally create a duplicate folder. If the extracted folder contains another folder with the same name inside, move its contents to the main folder.
5. Rename the folder to **jit** and move it to **C:/** for easier access.

### Setting Up the Server

1. Open **Start Menu**, type **CMD**, right-click **Command Prompt**, and select **Run as Administrator**.
2. In the command prompt, navigate to your folder using:
   ```
   cd C:/jit
   ```
3. Create a virtual environment:
   ```
   python3 -m venv venv
   ```
4. Activate the virtual environment:
   ```
   .\venv\Scripts\activate.bat
   ```
   **Note:** Use the **inverted backslash (\)** character which is typed using **AltGr + ?** instead of **normal backslash(/)** which is typed using **Shift + 7** 
5. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
   If you get an error with **pip3**, try using **pip** instead.
6. Install **SideJITServer**:
   ```
   pip install SideJITServer
   ```
7. Downgrade **ipsw_parser**:
   ```
   pip install ipsw_parser==1.3.4
   ```

### Step 5: Pairing Your Device

1. Connect your iPhone to your PC via USB.
2. Run the following command:
   ```
   SideJITServer --pair
   ```
3. When prompted, press **Y** and then tap **Trust this computer** on your iPhone.
4. Once pairing is complete, you’ll see your server address (e.g., `http://192.168.1.248:8080`).
5. Ensure both your iPhone and PC are on the **same Wi-Fi network**.
6. Open Safari on your iPhone and enter the server address.
7. Copy your **UUID** (e.g., `74820636-000A9536052690E`).
8. Install [this shortcut](https://www.icloud.com/shortcuts/b0ffc9c3f0e74e7a8f8052c89fa322cf).
9. Open the shortcut and enter your **server address** and **UUID**.
   **Important:**
   - Make sure you enter the **"http\://"** part correctly.
   - Do not add a **"/"** at the end.
10. Run the shortcut and select an app to enable **JIT**.
11. Once done, close the server and unplug your iPhone.

## Step 6: Running SideJITServer in the Future

Whenever you want to run **SideJITServer**, follow these steps:

1. Open **Command Prompt as Administrator**.
2. Navigate to your folder:
   ```
   cd C:/jit
   ```
3. Activate the virtual environment:
   ```
   .\venv\Scripts\activate.bat
   ```
4. Start the server:
   ```
   SideJITServer
   ```
   *(No need to add ********`--pair`******** this time.)*
5. Run the shortcut on your iPhone and test if it works over Wi-Fi.

You're all set! 🎉

