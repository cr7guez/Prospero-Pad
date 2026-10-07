<p align="center"><img src="assets/logo0.png" width="180" alt="Prospero-Pad PS5"></p>

# Prospero-Pad PS5 — Free your PS5 from the DualSense

**A Bluetooth controller bridge for jailbroken PS5 consoles.**

Prospero-Pad PS5 allows you to use controllers from other platforms on your PS5 by connecting them directly through the console's own Bluetooth hardware and presenting them to the system as virtual DualSense controllers.

No USB dongle required.

---

## ⚠️ Known issue: DualSense pairing

While Prospero-Pad is scanning for controllers, it may detect the PS5's own **DualSense** and accidentally pair with it.

Until this is fixed:

**Keep your DualSense switched OFF while pairing another controller.**

If your DualSense becomes disconnected or stops working correctly:

1. Reset the DualSense using the small reset hole on the back, next to L2.
2. Hold it for approximately 5 seconds with a paperclip.
3. Connect the DualSense to the PS5 using a USB-C cable.

---

## ⚠️ Important: use a separate PS5 user

The external controller must be assigned to a **different PS5 user** than the one used by your DualSense.

Create a new local user on your PS5 and assign the external controller to that user when the console asks.

For example:

- Main user → DualSense
- `Xbox` user → Xbox controller
- `PS4` user → DualShock 4
- `Switch` user → Nintendo Switch Pro Controller

You can continue playing with your normal main user.

### Switching to the external controller

For PlayStation controllers such as the DualShock 4, simply press the **PS button**.

For controllers without a PS button, such as Xbox and Nintendo controllers, use the blue **"Press PS"** button in the Prospero-Pad web interface.

This makes the external controller the active controller for the console.

---

# Controller compatibility

| Controller                           | Status                | Notes                                                                                                                                                                |
| ------------------------------------ | --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Xbox Series Controller**           | ✅ **Full Support**   | Fully functional. After pairing, the Xbox button may continue flashing. Simply hold the controller's **pairing button for ~3 seconds** and it will connect normally. |
| **DualShock 4**                      | ✅ **Full Support**   | Buttons, sticks and triggers fully working. Tested on a real PS5.                                                                                                    |
| **Nintendo Switch Pro Controller**   | ✅ **Full Support**   | Fully supported.                                                                                                                                                     |
| **Wii U GamePad / Controller**       | 🧪 **Experimental**   | Currently being worked on. A small amount of input lag remains and two buttons still need correct mapping.                                                           |
| **Nintendo Switch 2 Pro Controller** | 🚧 **In Development** | Not supported yet. Support is being developed and will be available in a future version.                                                                             |

More controllers will be added and tested over time.

---

# How it works

Prospero-Pad PS5 runs as a resident payload on a jailbroken PS5.

It uses the PS5's own Bluetooth hardware to:

1. Discover and pair Bluetooth controllers.
2. Communicate with them using Bluetooth HID.
3. Translate their inputs.
4. Create a virtual DualSense controller for the PS5.
5. Pass controller input to the system, games and supported emulators.

It does **not** modify games, the PS5 firmware or the jailbreak itself.

Your PS5 must already be capable of running homebrew payloads.

---

# How to use

Using Prospero-Pad is intentionally simple.

### 1. Jailbreak your PS5

Launch your preferred PS5 exploit and wait until your console is ready to run payloads.

### 2. Load Prospero-Pad

Load the `Prospero-Pad-<version>.elf` payload using **whatever payload loader you normally use**.

You can use Payload Manager, an autoloader or any other compatible method.

### 3. Check the notification

Immediately after Prospero-Pad starts, your PS5 will display a notification containing the web interface address.

It will look similar to:

```text
Prospero-Pad PS5
Web interface:
http://192.168.1.100:8095
```

### 4. Open the address

From a phone, computer or the PS5 browser, open the address shown in the notification.

For example:

```text
http://192.168.1.100:8095
```

Your device must be connected to the **same local network** as the PS5.

You will see the Prospero-Pad interface.

### 5. Pair your controller

Press **Pair** in the web interface and put your controller into Bluetooth pairing mode.

| Controller              | Pairing mode                                              |
| ----------------------- | --------------------------------------------------------- |
| **Xbox Series**         | Turn it on and hold the pairing button on the top         |
| **DualShock 4**         | Hold **Share + PS** until the light bar flashes           |
| **Nintendo Switch Pro** | Press the small sync button next to the USB-C port        |
| **Wii U**               | Put the controller into its Bluetooth pairing mode        |
| **Other controllers**   | Follow the controller manufacturer's pairing instructions |

Once paired, the controller will appear in the Prospero-Pad interface.

After the first pairing, simply turning the controller on should allow it to reconnect automatically.

---

# Using the controller in games

Remember that the external controller must belong to a **different PS5 user** from your DualSense.

For example:

```text
User 1 → DualSense
User 2 → Xbox Controller
```

Start your game normally with your main user.

Then activate the external controller:

- **DualShock 4:** press the PS button.
- **Xbox / Switch / other controllers:** press **"Press PS"** in the Prospero-Pad web interface.

The external controller will then become the active controller.

---

# Multiple controllers

Prospero-Pad can handle **up to 4 controllers simultaneously**.

You can therefore use combinations such as:

```text
Xbox Series Controller
+
DualShock 4
+
Nintendo Switch Pro Controller
+
Wii U Controller
```

Each controller can have its own profile and PS5 user.

The web interface allows you to see paired and connected controllers and select which controller should become active.

---

# Web interface

The Prospero-Pad web interface runs on port:

```text
8095
```

It allows you to:

- Pair controllers
- View connected controllers
- View paired controllers
- Select the active controller
- Forget paired controllers
- View the Prospero-Pad log
- Stop Prospero-Pad

The interface is designed for use on your local network.

**No Internet connection is required.**

---

# Important: stopping Prospero-Pad

Before launching Prospero-Pad again, stop the current instance from the web interface using:

**"Stop Prospero-Pad PS5"**

This ensures that Bluetooth connections are closed cleanly before restarting the payload.

The **Exit** button only closes the web page. It does **not** stop Prospero-Pad.

---

# Troubleshooting

### My controller is paired but it doesn't work in games

Make sure the controller is assigned to a **different PS5 user** than your DualSense.

This is currently required for games and emulators to recognize the virtual controller correctly.

### My Xbox button keeps flashing after pairing

This can happen with the Xbox Series controller.

Simply hold the controller's **pairing button for approximately 3 seconds**.

It should connect normally and the controller will be ready to use.

### My DualSense stopped working

Prospero-Pad may have accidentally paired with the console's own DualSense while scanning.

Turn Prospero-Pad off, reset the DualSense using the small hole on its back for approximately 5 seconds, and connect it to the PS5 using USB-C.

When pairing another controller, **keep the DualSense switched off**.

### The web page does not open

Make sure:

- Prospero-Pad is running.
- Your phone/computer is on the same local network as the PS5.
- You are using the exact IP address shown in the PS5 notification.
- Port `8095` is included.

Example:

```text
http://192.168.1.100:8095
```

---

# Alpha / Experimental status

Prospero-Pad PS5 is still under active development.

The **DualShock 4, Xbox Series Controller and Nintendo Switch Pro Controller** have reached full support.

Other controllers are being progressively tested and improved.

The project is particularly focused on expanding compatibility with controllers from other platforms while keeping the experience as simple and stable as possible.

---

# License

GPL-3.0-or-later.

See [LICENSE](LICENSE).

---

# Contact

**X / Twitter:** https://x.com/cr7guezz
