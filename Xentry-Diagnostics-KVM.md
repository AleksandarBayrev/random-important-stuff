# First - select BIOS without SecureBoot (IMPORTANT!!!)
# To use Xentry in VM edit your XML machine
```xml
<features>
  <acpi/>
  <apic/>
  <hyperv mode="custom">
    <relaxed state="on"/>
    <vapic state="on"/>
    <spinlocks state="on" retries="8191"/>
    <vendor_id state="on" value="AuthenticAMD"/>
  </hyperv>
  <kvm>
    <hidden state="on"/>
  </kvm>
  <vmport state="off"/>
  <smm state="on"/>
  <ioapic driver="kvm"/>
</features>
<cpu mode="host-passthrough" check="none" migratable="on">
  <topology sockets="1" dies="1" cores="3" threads="2"/>
  <feature policy="disable" name="hypervisor"/>
  <feature policy="require" name="vmx"/>
</cpu>
```