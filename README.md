# Relapse ESP32 Autoloader

Relapse ESP32 Autoloader is a MicroPython-based Relapse Autoloader for ESP32 boards.

## Requirements

* ESP32 with a minimum of 8 MB flash
* Computer
* USB cable

## Setup

### Step 1: Format the ESP32 for MicroPython

1. Download and install [Thonny IDE](https://thonny.org/).

2. Download the latest `.bin` MicroPython firmware for your ESP32 model from the [official MicroPython downloads page](https://micropython.org/download/esp32/).

3. Connect your ESP32 board to your computer using a USB cable.

4. In Thonny, go to **Run > Select interpreter...** and select **MicroPython (ESP32)** along with the correct COM/serial port for your board.

5. Click **Install or update firmware** at the bottom right of the interpreter window. You can also access this through **Tools > Options > Interpreter**.

6. Select your target port and browse to the `.bin` firmware file you downloaded.

7. Enable **Erase flash before installing**, then click **Install**.

8. If prompted, hold down the **BOOT** button on the ESP32 until the installation begins, then release it.

### Step 2: Transfer Files to the ESP32

Before transferring the files, make sure the ESP32 is selected in the bottom-right corner of Thonny.

1. Open the file manager by clicking **View > Files**.

2. The file manager will display two sections:

   * **This computer** — your local files
   * **MicroPython device** — the files currently stored on the ESP32

3. Navigate to the Relapse project folder under **This computer**.

4. Drag the project files from **This computer** to **MicroPython device**.

5. Wait for the upload to complete. Thonny will display the upload progress.

### Step 3: Connect to the ESP32

Once the files have been transferred, disconnect the ESP32 from your computer.

1. Connect the ESP32 to one of the console's USB ports.

2. On the console, navigate to **Settings > Network**.

3. Look for the Wi-Fi network named **PSWIFI**.

4. Connect to **PSWIFI** using the password:

```text
jailbreak
```

### Step 4: Trigger the Exploit

1. Navigate to the manual page and trigger the exploit.

2. Wait for the process to continue. Do not restart or refresh the process if it appears to stop.

> **Note:** You may see the following message:
>
> `[iframe] no exploit log at about blank...`
>
> This is normal. The process will continue after a short wait.

3. The process may also appear to hang at:

```text
elfldr is listening on port 9021
```

This is also normal. This will take over a minute as the ESP32 devices are slow.
