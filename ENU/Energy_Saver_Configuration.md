---
title: Energy Saver Configuration
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM enables Energy Saver configuration for the payload you use to configure energy-saver settings on Windows and macOS devices.

**Applicable to**:

- Windows 10 through the most recently released version as supported by Ivanti Neurons for MDM.
- macOS 10.7 through the most recently released version as supported by Ivanti Neurons for MDM.

**Procedure**

1. Go to **Configurations** > **+Add**.
2. Search and select the **Energy Saver** configuration.
3. In the Choose OS section, select **Windows** or **macOS** and click **Next**.
4. Click **+ Add Description** to enter a brief description of the configuration.
5. For Windows, configure the following **Energy Saver** settings:\* [**Device on Battery**](./Energy_Saver_Configuration.md)
   - [**Device is Plugged in**](./Energy_Saver_Configuration.md)
6. Configure the following **Energy Saver** settings:\* [**Desktop AC power energy-saver settings**](./Energy_Saver_Configuration.md)
   - [**Schedule for the computer to start up or shut down settings**](./Energy_Saver_Configuration.md)
   - [**Laptop AC power energy-saver settings**](./Energy_Saver_Configuration.md)
   - [**Laptop battery power energy-saver settings**](./Energy_Saver_Configuration.md)
7. Click **Next** to configure the distribution settings.
8. Select one of the distribution options to set up the **Energy Saver** configuration. For more information about configuring distribution options, see [**Working with Configurations**](./Working_with_Configurations.md).
9. Click **Done**.

## Windows Energy Saver configuration

When a new Energy Saver configuration applies to a device or when the existing Energy Saver configuration settings are modified, users must reboot their devices for the changes to take effect.

### Device on Battery

Use the following energy saver settings in the table when the device is using power from the battery:

| **Setting**                                   | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| --------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Battery Threshold to turn on Energy Saver** | When the device is using battery power, enter the battery charge level to turn on the Energy Saver, you can enter values from 0 to 100. Enter a percentage value that indicates the battery charge level. For example, when set to 80, Energy Saver turns on when the battery has 80% charge or less available charge.If you don't enter a value, Ivanti Neurons for MDM doesn't change or update this setting. By default, the Windows will set it to 70%. |
| **When Lid is closed**                        | - **Take No Action**: The device stays on and continues to use battery power.                                                                                                                                                                                                                                                                                                                                                                               |

- **Sleep**: The device goes into sleep mode and uses a small amount of battery charge. The computer is still on, and opened apps and files are stored in Random Access Memory (RAM).
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving. |
  \| **When Power button is selected**             | \* **Take No Action**: The device stays on and continues to use battery power.
- **Sleep**: The device goes into sleep mode and uses a small amount of battery charge. The computer is still on, and opened apps and files are stored in RAM.
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving.                        |
  \| **When Sleep button is selected**             | - **Take No Action**: The device stays on and continues to use battery power.
- **Sleep**: The device goes into sleep mode and uses a small amount of battery charge. The computer is still on, and opened apps and files are stored in RAM.
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving.                        |
  \| **Turn on hybrid sleep**                      | \* **True**: Devices can go into Hybrid Sleep mode. Opened apps and files are stored in RAM and on the hard disk. It uses a small amount of battery charge.
- **False**: Prevents devices from going into hybrid sleep mode.                                                                                                                                                                                                                                                                                 |

### Device is Plugged in

Use the following settings in the table when the device is using power from an external power source:

| **Setting**                                   | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Battery Threshold to turn on Energy Saver** | When the device is plugged in, enter the battery charge level to turn on Energy Saver, you can enter values from 0 to 100. Enter a percentage value that indicates the battery charge level. For example, when set to 80, Energy Saver turns on when the battery has 80% charge or less available charge.If you don't enter a value, Ivanti Neurons for MDM doesn't change or update this setting. By default, the Windows will set it to 70%. |
| **When Lid is closed**                        | - **Take No Action**: The device stays on and continues to use external power source.                                                                                                                                                                                                                                                                                                                                                          |

- **Sleep**: The device goes into sleep mode and uses a small amount of external power source. The computer is still on, and opened apps and files are stored in RAM.
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving. |
  \| **When Power button is selected**             | \* **Take No Action**: The device stays on and continues to use external power source.
- **Sleep**: The device goes into sleep mode and uses a small amount of external power source. The computer is still on, and opened apps and files are stored in RAM.
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving. |
  \| **When Sleep button is selected**             | - **Take No Action**: The device stays on and continues to use external power source.
- **Sleep**: The device goes into sleep mode and uses a small amount of external power source. The computer is still on, and opened apps and files are stored in RAM.
- **Hibernate Sleep State**: The device goes into hibernate mode. Opened apps and files are stored on the hard disk, and the device turns off.
- **Shut down**: The device shuts down. Opened apps and files are closed without saving. |
  \| **Turn on hybrid sleep**                      | \* **True**: Devices can go into Hybrid Sleep mode. Opened apps and files are stored in RAM and on the hard disk. It uses a small amount of external power source.
- **False**: Prevents devices from going into hybrid sleep mode.                                                                                                                                                                                                                                                                  |

## macOS Energy Saver configuration

### Desktop AC power energy-saver settings

Use the following settings to configure the macOS desktop device’s AC power energy-saver settings:

| **Setting**                                      | **Description**                                                                                                                                            |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**                                         | Enter a name that identifies this configuration.                                                                                                           |
| **Description**                                  | Enter a description that clarifies the purpose of this configuration.                                                                                      |
| **Start up automatically after a power failure** | Enable the device to start up automatically after a power failure.                                                                                         |
| **Put a hard disk to sleep after**               | Enable the checkbox to put the hard disk to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the hard disk to sleep. |
| **Turn display off after**                       | Enable the checkbox to turn off the display at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never turn off the display.             |
| **Dynamic Power Step**                           | Select the checkbox to enable the dynamic power step.                                                                                                      |
| **Reduce Processor Speed**                       | Select the checkbox to reduce processor speed.                                                                                                             |
| **Put the computer to sleep after**              | Enable the checkbox to put the computer to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the computer to sleep.   |
| **Wake for network access**                      | Select the checkbox to wake the computer for network access.                                                                                               |
| **Wake for modem ring**                          | Select the checkbox to wake the computer for the modem ring.                                                                                               |

### Schedule for the computer to start up or shut down settings

Use the following settings to configure the macOS devices for scheduled start up or shut down of the devices.

### Turning off the device settings

Select the checkbox **Turn the device off** to shut down the devices at fixed intervals.

| **Setting**    | **Description**                                                |
| -------------- | -------------------------------------------------------------- |
| **Event Type** | Select one of the event types from the drop-down list:\* Sleep |

- Restart
- Shut Down |
  \| **When**       | Select one or more days of the week to schedule an event type.                      |
  \| **At**         | Select the time to schedule an event type.                                          |

### Starting or waking up the device settings

Select the checkbox **Start up or wake the device** to wake up the devices at fixed intervals.

| **Setting**    | **Description**                                                  |
| -------------- | ---------------------------------------------------------------- |
| **Event Type** | Select one of the event types from the drop-down list:\* Wake Up |

- Start Up / Wake |
  \| **When**       | Select one or more days of the week to schedule an event type.                    |
  \| **At**         | Select the time to schedule an event type.                                        |

### Laptop AC power energy-saver settings

Use the following settings to configure the macOS laptop device’s AC power energy-saver settings:

| **Setting**                                      | **Description**                                                                                                                                            |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Start up automatically after a power failure** | Enable the device to start up automatically after a power failure.                                                                                         |
| **Put a hard disk to sleep after**               | Enable the checkbox to put the hard disk to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the hard disk to sleep. |
| **Turn display off after**                       | Enable the checkbox to turn off the display at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never turn off the display.             |
| **Dynamic Power Step**                           | Select the checkbox to enable the dynamic power step.                                                                                                      |
| **Reduce Processor Speed**                       | Select the checkbox to reduce processor speed.                                                                                                             |
| **Put the laptop to sleep after**                | Enable the checkbox to put the laptop to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the laptop to sleep.       |
| **Wake for network access**                      | Select the checkbox to wake the laptop for network access.                                                                                                 |
| **Wake for modem ring**                          | Select the checkbox to wake the laptop for the modem ring.                                                                                                 |

### Laptop battery power energy-saver settings

Use the following settings to configure the macOS laptop battery power energy-saver settings:

| **Setting**                                      | **Description**                                                                                                                                                      |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Start up automatically after a power failure** | Enable the device to start up automatically after a power failure.                                                                                                   |
| **Put a hard disk to sleep after**               | Enable the checkbox to put the hard disk to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the hard disk to sleep.           |
| **Turn display off after**                       | Enable the checkbox to turn off the display at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never turn off the display.                       |
| **Dynamic Power Step**                           | Select the checkbox to enable the dynamic power step.                                                                                                                |
| **Reduce Processor Speed**                       | Select the checkbox to reduce processor speed.                                                                                                                       |
| **Put the computer to sleep after**              | Enable the checkbox to put the laptop battery to sleep at fixed intervals between 1 and 180 minutes.A value of 0 minutes will never put the laptop battery to sleep. |
| **Wake for network access**                      | Select the checkbox to wake up the laptop battery for network access.                                                                                                |
| **Wake for modem ring**                          | Select the checkbox to wake the laptop battery for the modem ring.                                                                                                   |
