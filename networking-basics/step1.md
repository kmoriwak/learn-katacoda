# What is NetworkManager?

NetworkManager is a great tool for creating and modifying network connections.
The `nmcli` command is how you will be running NetworkManager in this lab. Any changes
made with `nmcli` are persistent configuration file changes. This lab will give you an
overview of some of the most common operations you would run using this tool.

# Listing network devices

Before you can set up a connection, you have to know what hardware
is available for you to use. To show what network devices this system has with
`nmcli`, run

`nmcli device`{{execute T2}}

>_NOTE:_ You may need to wait a few seconds and retry the command above if the terminal for __host01__ is still loading.

This will show a list of network interfaces available on the system as well as
how they are configured, similar to the following:

<pre class=file>
DEVICE  TYPE      STATE                                  CONNECTION         
ens3    ethernet  connected                              System ens3        
ens5    ethernet  connecting (getting IP configuration)  Wired connection 1
lo      loopback  unmanaged                              --      
</pre>

This output shows that there are three devices: __ens3__ and __ens5__ (ethernet devices)
as well as __lo__ (the loopback device).

Next, you will make your own connection on this host.
