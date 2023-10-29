---
tags:
  - technology
see also:
  - "[[IRK]]"
---
- Referred to as a Bluetooth MAC address is a 48-bit value that uniquely identifies a Bluetooth device
- There are two main types of Bluetooth addresses: public and random
  ![](https://mlv0gpv1snjt.i.optimole.com/cb:_0gS~51496/w:691/h:387/q:90/https://www.novelbits.io/wp-content/uploads/2020/04/Address-Types-1.png)

## Public Address

- A global fixed address must be registered with the IEEE
- Follows the same guidelines as MAC address and will have a 48-bit extended unique identifier

## Random Address

- More popular than public ones since they do not require registration
- It can be programmed into the device or generated at runtime
- There are two types: static and private

### Random Static Address

- An alternative to the public address can be assigned and fixed for the lifetime of the device or it can be changed at boot
- It **cannot be changed during runtime**

### Random Private Address

- There are two types: resolvable and non-resolvable
- Used to protect the privacy of a Bluetooth device by hiding its identity and preventing tracking

#### Resolvable Random Private Address

- Designed to prevent malicious third parties from tracking the device while still allowing one or more trusted parties to identify the device of interest
- It is resolvable using a key shared with a trusted device — this is the [[IRK]]
- Generated using an [[IRK]] and a random number
- This address changes periodically (recommended to change it every 15 minutes)

#### Non-Resolvable Random Private Address

- This type changes periodically
- Unlike resolvable address, it is not resolvable by any other device and its sole purpose is to prevent tracking by any other BLE
- It's not very common but is sometimes used in beacon applications

---
