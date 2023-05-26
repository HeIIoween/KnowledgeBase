---
title: Equipment and Equipment Dealer Offsets
---

## Information

* All offsets are for files from the official 1.1 patch.
* Numbers are in hexadecimal, or suffixed to indicate their type:

| Suffix | Type    | Size                 |
| ------ | ------- | -------------------- |
| f      | float   | 4 bytes              |
| d      | double  | 8 bytes              |
| i      | integer | 4 bytes              |
| b      | byte    | 1 byte (-128 to 127) |

A value like "0F 85 -> 90 E9" means replace the original bytes on the left with the new bytes on the right. (The bytes are given in file order, they don't represent a number like the offset.)

### Equipment Dealers

| Default Value                                                                                                                                                                      | File           | Offset            | By               | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ----------------- | ---------------- | ---------------------------------------------------------------------------------------------------------------- |
| 90 53 32 -> C0 DE 26                                                                                                                                                               | common.dll     | 139B74            | adoxa            | Use thruster hp_type for cloaking device.                                                                        |
| 90 53 32 -> 50 DB 26                                                                                                                                                               | common.dll     | 139B74            | adoxa            | Place cloaking devices on countermeasure hardpoints.                                                             |
| 90 53 32 -> 40 17 2D                                                                                                                                                               | common.dll     | 139B74            | adoxa, HeIIoween | Use cloaking device as internal equipment.                                                                       |
| 40172D -> C0DE26                                                                                                                                                                   | common.dll     | 139AF0            | Laz              | Use thruster hp_type for armour.                                                                                 |
| 00 BA 29<br/>-><br/>10 A7 27                                                                                                                                                       | common.dll     | 139AFC            | adoxa            | Consider armor types attached to hardpoint when mounted.                                                         |
| 0F 87 -> 90 E9                                                                                                                                                                     | freelancer.exe | 07C943            | adoxa            | Remove class info from equipment.                                                                                |
| 0F 84 -> 90 E9                                                                                                                                                                     | freelancer.exe | 0840B3            | M0tah            | Remove automatically generated portion of equipment infocards.                                                   |
| 0D -> 00                                                                                                                                                                           | freelancer.exe | 07EBF1            | adoxa            | Activate missile/torpedo/disruptor on purchase.                                                                  |
| 0D -> 00                                                                                                                                                                           | freelancer.exe | 07FAA4            | adoxa            | Activate missile/torpedo/disruptor on mount.                                                                     |
| 0.8f                                                                                                                                                                               | freelancer.exe | 1D6D38            | Dev              | Resale % for ships (client-side).                                                                                |
| 0.8f                                                                                                                                                                               | server.dll     | 08AE78            | FriendlyFire     | Resale % for ships (server-side, must match variable above or 1.1 server dll will kick client for cheating).     |
| 0.3f                                                                                                                                                                               | freelancer.exe | 1D0E2C            | fox              | Resale % for equipment (client-side).                                                                            |
| 0.3f                                                                                                                                                                               | server.dll     | 08AE7C            | fox              | Resale % for equipment (server-side, must match variable above or 1.1 server dll will kick client for cheating). |
| 0.33f                                                                                                                                                                              | common.dll     | 004A28<br/>0057FA | FriendlyFire     | Default repair price ratio (ships and collision groups) (both offsets must be changed).                          |
| 3B C7 74 2A 50 FF 15 FC 61 5C 00 83 C4 04 3B C7 89 44 24 10 74 18 D9 05 DC 75 5C 00<br/>-><br/>50 FF 15 FC 61 5C 00 90 89 44 E4 14 FF 15 58 61 5C 00 89 C1 FF 15 18 64 5C 00 D9 E8 | freelancer.exe | 0B3A0E            | adoxa            | Repair cost based on ship cost, not armor (Part 1).                                                              |
| 1C -> 58                                                                                                                                                                           | freelancer.exe | 0B3A30            | adoxa            | Repair cost based on ship cost, not armor (Part 2).                                                              |
| C4 -> C8                                                                                                                                                                           | freelancer.exe | 07C9A8            | M0tah            | Remove class number (just the number) on equipment entries.                                                      |
| 75 -> EB                                                                                                                                                                           | freelancer.exe | 080942            | M0tah            | Allow engines to be sold.                                                                                        |
| 0F 85 -> 90 E9                                                                                                                                                                     | freelancer.exe | 0808AD            | adoxa            | Allow engines to be transferred.                                                                                 |
| 0C -> 14                                                                                                                                                                           | freelancer.exe | 0808AC            | adoxa            | Prevent transfer of scanner (but allows engine).                                                                 |
| 0C -> 14                                                                                                                                                                           | freelancer.exe | 080941            | adoxa            | Prevent selling of scanner (but allows engine).                                                                  |
| 83 F8 -> EB 22                                                                                                                                                                     | freelancer.exe | 07B020            | adoxa            | Prevent transfer of all equipment.                                                                               |
| 84 -> 30                                                                                                                                                                           | freelancer.exe | 07CEC0            | adoxa            | Prevent mounting/unmounting of all equipment.                                                                    |
| 75 -> EB                                                                                                                                                                           | freelancer.exe | 0B88A4            | adoxa            | Disable "Select Ship" ship dealer button.                                                                        |
| 74 -> EB                                                                                                                                                                           | freelancer.exe | 1855C0            | adoxa            | Scale ship to fill the preview.                                                                                  |
| 14f                                                                                                                                                                                | freelancer.exe | 1855C8            | BC46             | Zoom level of the ship preview camera. Decrease this value to zoom in, increase it to zoom out.                  |
| 0f                                                                                                                                                                                 | freelancer.exe | 0B7B85            | adoxa            | Angular velocity of ship in preview around x-axis.                                                               |
| 0f                                                                                                                                                                                 | freelancer.exe | 0B7B90            | adoxa            | Angular velocity of ship in preview around y-axis.                                                               |
| 0f                                                                                                                                                                                 | freelancer.exe | 0B7B9B            | adoxa            | Angular velocity of ship in preview around z-axis.                                                               |
| 162.581f                                                                                                                                                                           | freelancer.exe | 0B8EFA            | adoxa            | Initial ship preview angle around x-axis (in degrees).                                                           |
| -71.6442f                                                                                                                                                                          | freelancer.exe | 0B8F02            | adoxa            | Initial ship preview angle around y-axis (in degrees).                                                           |
| 0f                                                                                                                                                                                 | freelancer.exe | 0B8F0A            | adoxa            | Initial ship preview angle around z-axis (in degrees).                                                           |
| 74 -> EB                                                                                                                                                                           | freelancer.exe | 080499            | adoxa            | Removes the level requirements for purchasing equipment in Single Player (Part 1).                               |
| 74 -> EB                                                                                                                                                                           | freelancer.exe | 082E95            | adoxa            | Removes the level requirements for purchasing equipment in Single Player (Part 2).                               |
| 74 -> EB                                                                                                                                                                           | freelancer.exe | 0B948D            | adoxa            | Removes the level requirements for purchasing ships in Single Player.                                            |
| 75 -> EB                                                                                                                                                                           | freelancer.exe | 08050B            | BC46             | Allows the purchase of equipment that cannot be mounted on the player's ship.                                    |
| 0F 85 8A 01 00 00 -> E9 8B 01 00 00 90                                                                                                                                             | freelancer.exe | 08053E            | BC46             | Allows the purchase of equipment for which no free hardpoint is available on the player's ship.                  |
| 00 00 -> E3 1F                                                                                                                                                                     | common.dll     | 053048            | adoxa            | include external equipment in cargo size (Part 1).                                                               |
| 00 00 -> E3 1F                                                                                                                                                                     | common.dll     | 05330E            | adoxa            | include external equipment in cargo size (Part 2).                                                               |
| 18 -> 00                                                                                                                                                                           | common.dll     | 0A9BA3            | adoxa            | include external equipment in cargo size (Part 3).                                                               |
| 18 -> 00                                                                                                                                                                           | common.dll     | 0AA904            | adoxa            | include external equipment in cargo size (Part 4).                                                               |
| 74 -> EB                                                                                                                                                                           | freelancer.exe | 0838AF            | adoxa            | Consider volume when buying external equipment                                                                   |