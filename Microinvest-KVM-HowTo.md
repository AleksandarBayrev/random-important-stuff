# OS
```xml
<os>
  <type arch='x86_64' machine='pc-q35-4.2'>hvm</type>
  <smbios mode='sysinfo'/>
</os>
```
# SYSINFO

```xml
<sysinfo type='smbios'>
  <bios>
    <entry name='vendor'>American Megatrends Inc.</entry>
    <entry name='version'>3405</entry> </bios>
  <system>
    <entry name='manufacturer'>ASUSTeK COMPUTER INC.</entry>
    <entry name='product'>PRIME B550-PLUS</entry>
    <entry name='version'>Rev 1.xx</entry>
  </system>
  <baseBoard>
    <entry name='manufacturer'>ASUSTeK COMPUTER INC.</entry>
    <entry name='product'>PRIME B550-PLUS</entry>
    <entry name='version'>Rev 1.xx</entry>
  </baseBoard>
</sysinfo>
```

# Features

```xml
<features>
  <acpi/>
  <apic/>
  <hyperv>
    <relaxed state='on'/>
    <vapic state='on'/>
    <spinlocks state='on' retries='8191'/>
    <vendor_id state='on' value='ASUS_B550'/>
  </hyperv>
  <kvm>
    <hidden state='on'/>
  </kvm>
</features>
```

# CPU

```xml
<cpu mode='host-passthrough' check='none'>
  <topology sockets='1' dies='1' cores='4' threads='2'/>
  <feature policy='disable' name='hypervisor'/>
</cpu>
```

# Network
## Choose a Real ASUS MAC Prefix

#### For an ASUS B550-PLUS, the onboard LAN is usually a Realtek or Intel chip. To look authentic, your MAC address should start with one of these ASUS-registered prefixes:

* BC:EE:7B (Common for modern ASUS boards)
* 04:42:1A (Newer ASUS allocation)
* 24:4B:FE (Used for recent PRIME series)

#### Example Authenticated MAC: 24:4B:FE:0A:B1:C2 (The last 3 segments can be random hex).

## The Libvirt XML Modification

#### Open your VM config: virsh edit <vm_name>

#### Find the <interface> section and modify the <mac> and <model> tags.

```xml
<devices>
  <interface type='network'>
    <mac address='24:4B:FE:A1:B2:C3'/> <!-- this is the important part-->
    
    <source network='default'/> <!-- not mandatory, probably already present -->
    
    <model type='e1000e'/> <!-- this as well-->
    
    <address type='pci' domain='0x0000' bus='0x01' slot='0x00' function='0x0'/> <!-- not mandatory -->
  </interface>
</devices>
```