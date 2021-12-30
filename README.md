# Defmt RTT plugin from GDB

This small plugin runs [defmt-print](https://crates.io/crates/defmt-print) on the RTT stream produced by JLinkGDBServer,
so that you can see the defmt logs in the GDB session.

# Usage

Make sure you have installed:

* defmt-print
* nc (netcat)

Start the JLinkGDBServer (or other server that streams RTT over TCP), then
source the plugin script and run the defmt command:

```
(gdb) source defmt-rtt-gdb.py
(gdb) defmt-rtt
```

