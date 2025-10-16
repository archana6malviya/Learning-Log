#  Networking: NAT Network

## What I Did
- Connected both Windows 10 and Ubuntu VMs to the same **NAT Network** in VirtualBox.
- This allowed both VMs to **access the internet** and **communicate with each other**.
- Both VM's are physically separated from our host but logically connected to each other.
- Created a Network & then Apply it to the Network Adapters.

## What I Learned
- **NAT Network** is different from basic **NAT**:
  - Still uses host's internet connection.
  - VMs are placed in the same **private virtual network**.
  - They get IPs like `10.0.2.x` or `10.0.3.x` and **can ping each other**.
- This is useful when you want:
  - Internet access
  - VM-to-VM communication
  - No direct host access to VMs (safe for testing malware, etc.)

## Result:
Ubuntu can ping Windows VM ✅
Windows can ping Ubuntu VM ✅
Both have internet access ✅

