# Networking Configuration between two VM's 

## Goal:
Allow VMs to access the internet and communicate with each other.

## Create a Network & Apply it to the Network Adapters to our VM's
1. Open **VirtualBox**.
2. Go to **Network**- **NAT Network**- **Create**.
3. Right click on **NAT Network**, GO to **Properties**.
4. GO to **Name**- Assign Name.
5. Go to **IPv4**- Put range according to you.
6.  Keep **DHCP**- Enable- **Apply**.

## Set Up NAT Network 
### Step-by-Step: Create NAT Network
1. Open **VirtualBox**.
2. **Shutdown both VMs** if they’re running.
3. Go to **Settings** for each VM.
4. Navigate to **Network** > **Adapter 1**
5. Check "Enable Network Adapter"
6. Set **Attached to** → `NAT Network`
7. Name the network– must be the same for both VMs.
8. - Uncheck "Supports DHCP" (if you want to set static IPs manually)
   - Click OK
9. Start both VMs

## Test Networking Between VMs
### Step 1: Get IPs
- On Ubuntu: Run `ip a` or `ip addr`
- On Windows: Run `ipconfig`

You should see private IPs like `10.0.3.x` or Manually created.

### Step 2: Ping Test
- From Ubuntu: Ping <Windows_VM_IP>
- From Windows: Ping <Ubantu_VM_IP>
✅ If you see replies, your VMs are successfully talking to each other.

## Tips
1. Check if only one Adaptor were **Enable** for both VM's.
