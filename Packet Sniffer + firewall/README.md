🔥 Real-Time Packet Sniffer & Firewall Rule Manager
A Python GUI application that captures live network packets, classifies them (allowed/blocked), visualizes protocol distribution, and allows dynamic firewall rule management with JSON rule persistence.

📦 Features
✅ Live Packet Capture

Captures IP, TCP, UDP, and ICMP packets in real-time

Displays source/destination, ports, protocol, and status (Allowed/Blocked)

✅ Firewall Rules Engine

Block by IP, Port, or Protocol (TCP/UDP/ICMP)

Automatically filters packets based on configured rules

Persist rules in a JSON file (firewall_rules.json)

Manual save via GUI button

✅ Graphical Protocol Analysis

Visual pie chart of protocol distribution

Real-time updates with packet data

✅ Filtering and Export

Filter packets by protocol and/or port

Export filtered packet logs to a .txt file

✅ User-Friendly GUI

Built with PyQt5

Modular: Graph viewer, firewall rule manager, and main live monitor

🚀 Getting Started
🖥️ Requirements
Install the required Python libraries:

bash
Copy
Edit
pip install pyqt5 scapy matplotlib
💡 Run with administrator/root privileges to allow raw packet sniffing.

▶️ Run the Application
bash
Copy
Edit
python your_script_name.py
The main GUI window will open and immediately begin sniffing packets.

🧩 File Structure
File	Description
your_script.py	Main application script
firewall_rules.json	Auto-generated firewall rules (IP, Port, Proto)
README.md	Project documentation

🛡️ Firewall Rule Controls
Add Rule: Input IP/Port/Protocol → Click Add Rule

Delete Rule: Select a rule → Click Delete Selected Rule

Save Rules: Click Save Firewall Rules to write to firewall_rules.json

Blocked packets will show in red, and allowed packets in green.

📊 Graph Viewer
Click Open Graph Viewer from the main window

Shows a real-time pie chart of protocol usage

Click Refresh Graph to update the chart

💾 Saving Packets
Click Save Filtered Packets to export visible logs

Output file format: .txt

Only saves currently filtered/displayed packets

🧠 How It Works (Behind the Scenes)
Packet Sniffing: Uses scapy to capture packets and extract relevant data

Filtering: Matches packets against blocked IPs/ports/protocols

Multithreading: Packet sniffer runs on a daemon thread to keep UI responsive

Data Sharing: Uses queue.Queue to pass packets from sniffer thread to GUI

Visualization: Protocols are counted and visualized using matplotlib

🔐 Permissions
This tool requires root/administrator privileges to sniff packets:

On Linux/macOS:

bash
Copy
Edit
sudo python your_script.py


On Windows:
Run from an elevated Command Prompt or use Python IDE as Admin

⚠️ Disclaimer
This tool is for educational and research purposes only. Unauthorized packet sniffing may violate local laws or network policies. Always ensure you have permission to monitor the network.

🙌 Author & Credits
Developed by [Madhavan.S]

Libraries Used:

PyQt5

Scapy

Matplotlib
