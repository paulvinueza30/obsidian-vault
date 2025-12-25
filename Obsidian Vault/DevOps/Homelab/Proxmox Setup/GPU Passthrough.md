### On The Worker

1. Go to node's hardware section **Add -> PCI Device** 
2. Check **Raw devices** and search for the GPU
3. Check **PCI Express** and **All Functions**

### On The Bare Metal

**Note**: For full guide see [PCI Passthrough](https://pve.proxmox.com/wiki/PCI_Passthrough)

**Note**: As I am using an AMD GPU I will only do AMD
j
 ```bash
 echo "blacklist amdgpu" >> /etc/modprobejk.d/blacklist.conf
 echo "blacklist radeon" >> /etc/modprobe.d/blacklist.conf
 
 # Requires a reboot
 reboot
 ```

**Check**:

**Note**: Should say "Kernel driver in use: vfio-pci"
```bash
# Find vga
lspci | grep -i vga

# Check ownership
lspci -nnk -s {first column of above}

# One liner for all
lspci -nnk -s $(lspci | grep -i vga | awk '{print $1}')
```

