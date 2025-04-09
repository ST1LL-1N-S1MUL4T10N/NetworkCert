### Command Line Tools – CompTIA Network+ N10-009 – 5.5

In the world of network troubleshooting, command line tools are essential for diagnosing and fixing issues. Let's dive into some of the most common and useful command line utilities, including `ping`, `traceroute`, `nslookup`, `dig`, `tcpdump`, `netstat`, and more.

#### Ping Command:
- **Purpose:** The `ping` command checks if a device is reachable over the network. If the device is not reachable, it provides information about why it isn’t.
- **Protocol:** Uses **ICMP (Internet Control Message Protocol)** to send a request to a target and wait for a reply.
- **Usage Example:**
  - On any operating system (macOS, Linux, or Windows), you can run `ping 1.1.1.1` (Cloudflare’s DNS) to see if it responds.
  - If successful, you'll receive the round trip time of the ICMP request, along with the TTL (Time to Live) information. If unsuccessful, you'll see a timeout error.
- **Stopping Ping:** On Linux/macOS/Windows, use **Ctrl+C** to stop the continuous ping and display statistics.
  
#### Traceroute Command:
- **Purpose:** The `traceroute` command traces the path packets take from your device to the destination device (such as a server). It shows each hop along the route.
- **Difference Between OS:** 
  - On Linux/macOS, use `traceroute` 
  - On Windows, use `tracert`.
- **How It Works:** 
  - It manipulates the TTL (Time to Live) field in the packet header to gather the route information. It starts with TTL=1, sending packets to the first router. The router decrements TTL, and if it reaches 0, it sends a response back indicating the hop.
  - Traceroute continues incrementing TTL and collects responses from each hop.
- **ICMP Filtering:** Some firewalls may block ICMP messages, resulting in asterisks in the output where data should be.
  
#### Nslookup and Dig:
- **Purpose:** These tools help you query DNS servers to resolve domain names to IP addresses.
- **Nslookup:** 
  - Available on Windows, Linux, and macOS.
  - **Deprecated:** It's being replaced by `dig` in modern systems.
  - Example: `nslookup www.professormesser.com` provides IP addresses associated with the domain.
- **Dig:**
  - Available natively on Linux and macOS, and can be installed on Windows.
  - Provides detailed DNS information and better format than `nslookup`.
  - Example: `dig www.professormesser.com` will show the DNS query results with A records (IPv4 addresses).

#### Tcpdump:
- **Purpose:** `tcpdump` captures packets on the network, allowing you to see the raw data flowing through the network.
- **Usage:** It can show every packet on the network or filtered traffic based on criteria (such as IP address, port, or protocol).
- **Packet Capture:** Saves captured data in **pcap** (Packet Capture) format, which can be loaded into Wireshark for detailed analysis.

#### Netstat:
- **Purpose:** Displays network statistics and shows information about active connections.
- **Common Commands:**
  - `netstat -a`: Lists all active connections and listening ports.
  - `netstat -b`: In Windows, shows the executable involved in the connection.
  - `netstat -n`: Shows IP addresses instead of domain names.
- **Example:** Running `netstat` will display local and remote IPs, ports, and connection states.

#### IP Configuration Commands:
- **Purpose:** To view and troubleshoot local device IP configurations.
- **Windows:** Use `ipconfig` to view IP addresses, subnet masks, and gateways. Use `ipconfig /all` for more details, like DHCP settings and DNS servers.
- **Linux/macOS:** Use `ifconfig` (older) or `ip a` (newer) to view the IP address and network interface details.

#### ARP (Address Resolution Protocol):
- **Purpose:** Resolves IP addresses to MAC addresses on the local network.
- **Command:** `arp -a` displays the ARP table, showing IP-to-MAC address mappings.
- **Useful For:** Troubleshooting network connectivity, such as checking if a device is properly mapping its IP to its MAC address.
