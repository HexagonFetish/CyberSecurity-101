# What Are the Seven Layers of the OSI Model?

The OSI (Open Systems Interconnection) model was created back in the late 1970s by the ISO (International Organization for Standardization) and some other groups. It first dropped officially in 1984 as ISO 7498, and the latest version is ISO/IEC 7498-1:1994. The model breaks down networking into seven different layers, each with its own job. Here’s the breakdown:

## Physical Layer

This is the foundation. The physical layer deals with the actual hardware and the transmission of raw bits over a medium—things like fiber optics, copper wires, and even wireless signals flying through the air. It covers stuff like Bluetooth, NFC, and defines things like speed, voltage, and connection types. No data structuring here, just raw transmission.

## Data Link Layer

Once you’ve got a physical connection, the data link layer steps in to make sure that data frames can travel safely between two devices. It handles framing, error detection, and flow control. Think Ethernet standards. This layer is split into two parts: MAC (Media Access Control) for hardware addresses and LLC (Logical Link Control) for managing communications.

## Network Layer

The network layer figures out how to get data from one device to another across multiple networks. It’s all about routing, addressing, and forwarding. Protocols like IPv4 and IPv6 live here. If data needs to travel across countries or different networks, the network layer handles the roadmap.

## Transport Layer

This layer makes sure that data gets to the right place, in the right order, without messing anything up. It’s all about reliability, sequencing, and error recovery. TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) work here—TCP is reliable and ordered, UDP is faster but doesn’t guarantee delivery.

## Session Layer

The session layer sets up, manages, and tears down communication sessions between applications. It keeps data streams from getting mixed up and handles checkpoints and recovery if needed. Examples of session layer protocols include NFS (Network File System) and SMB (Server Message Block).

## Presentation Layer

This layer deals with the translation of data formats. It ensures that data sent from one system can be read and understood by another. It handles encryption, compression, and formatting. Think formats like HTML, JSON, and CSV.

## Application Layer

At the top of the stack, the application layer is what the user actually interacts with. It supports application services like web browsing (HTTP, HTTPS) and email (SMTP, POP3). It’s about protocols and services that users directly experience.

---

> **Note:** Not every system implements all seven layers exactly as they are described in the OSI model.