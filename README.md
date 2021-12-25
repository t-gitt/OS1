# OS1
[![Donate Paypal](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/paypalme/Taheralkamel)
[![Donate Bitcoin](https://img.shields.io/badge/btc-bc1qawj2lp8kxzf5n9hew7s72sq2l4e2q72643rgs0-%23F7931A)](https://taheralkamel.xyz/donate.html)

A Plymouth theme inspired by OS1 from the movie Her that supports encrypted boot setups

# Preview
https://user-images.githubusercontent.com/29256024/147393169-4e8f32bf-6007-4a2e-a952-ef43b8da4211.mp4

# Installation

### Fedora
```bash
git clone https://github.com/t-gitt/OS1.git
cd OS1/
sudo cp -r os1 /usr/share/plymouth/themes/
sudo plymouth-set-default-theme os1 -R
```
### Debian
```bash
git clone https://github.com/t-gitt/OS1.git
cd OS1/
sudo cp -r os1 /usr/share/plymouth/themes/
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/os1/os1.plymouth 100
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```

if you are using an unencrypted boot drive, replace this line ```:87```  in ```os_1.script```

```Plymouth.SetRefreshFunction (refresh_callback_with_password);```

with

``` Plymouth.SetRefreshFunction (refresh_callback); ```

#### Animation Credit
YouTube @That Martian

[![Her - Loading OS1](https://img.youtube.com/vi/WOeyLpgjQ5Y/0.jpg)](https://www.youtube.com/watch?v=WOeyLpgjQ5Y)
