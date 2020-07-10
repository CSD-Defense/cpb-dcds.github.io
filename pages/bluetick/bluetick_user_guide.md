---
title: Bluetick User Guide
keywords: bluetick user guide
sidebar: bluetick_sidebar
permalink: bluetick_user_guide.html
folder: bluetick
---
## Scope

//TODO: add scope

## Build Natively

- Open terminal
- Navigate to &quot;bluetick/sensor/sensor/cmd&quot;
- Type: ( go build )

## Run Natively

- Open terminal
- Navigate to &quot;bluetick/sensor/sensor/cmd&quot;
- Type: ( sudo ./cmd ) To run the tool with no options. If you wish to run the tool with options, please be sure to review the &quot;Options&quot; section of this User Guide.

## View Output

Unless the &quot;outputfile&quot; option is set, the output file with be located in &quot;bluetick/sensor/sensor/cmd&quot; as &quot;sensor.json&quot;.

- **sessions** --Array of individual sessions
- **timestamp** -- EPOCH timestamp
- **src\_ip** -- Source IP address
- **dst\_ip** -- Destination IP address
- **src\_port** -- Source port
- **dst\_port** -- Destination port
- **tcp\_payload** -- TCP payload
- **tcp\_payload\_entropy** :
  - **shannon\_entropy** --
  - **chi\_square\_distance** --
  - **arithmetic\_mean** --
  - **serial\_correlation\_coefficient** --

## Build/Run in Docker

- Open terminal
- Navigate to bluetick/sensor/
- Type: ( docker-compose up )

## Options

- **assembly\_debug\_log** – If true, the github.com/google/gopacket/tcpassembly library will log verbose debugging information (at least one line per packet)
- **assembly\_memuse\_log** – If true, the github.com/google/gopacket/tcpassebly library will log information regarding its memory use every once in a while.
- **base** (_string_) -- Base layer when decoding packets. (default &quot;ethernet&quot;)
- **bpf** (_string_) -- Berkeley packet filter to apply to sniffer.
- **iface** (_string_) -- Network interface to capture on. (default &quot;eth0&quot;)
- **opts** (_string_) -- Decoding option. (default &quot;lazy&quot;)
- **outdir** (_string_) -- Directory to output results. Default is current directory.
- **outfile** (_string_) -- Name of output file. (default &quot;sensor.json&quot;)
- **pcaps** (_string_) -- Path to pcap file or directory containing pcaps.
- **promisc** – Toggle promiscuous mode for live interface capture. (default true)
- **snaplen** (_int_) -- The snaplen for live interface capture. (default 1024)
