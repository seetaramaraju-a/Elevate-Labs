# Task 4 - Firewall Configuration (Windows)

## Objective
Configure and test basic Windows Firewall rules to block and allow specific network traffic.

## Tools Used
- Windows Defender Firewall with Advanced Security
- Command Prompt (for testing)

## Steps Taken
1. **Checked existing firewall rules**  
   - Opened **Windows Defender Firewall with Advanced Security** from the Start menu.
   - Reviewed **Inbound Rules** and **Outbound Rules**.

2. **Blocked inbound traffic on Telnet (Port 23)**  
   - Clicked **Inbound Rules → New Rule → Port**.
   - Selected **TCP** and entered **23** as the port number.
   - Chose **Block the connection** for all profiles (Domain, Private, Public).
   - Named the rule **Block Telnet** and saved it.

3. **Tested the block rule**  
   - In Command Prompt:  
     ```cmd
     telnet localhost 23
     ```
   - Connection failed, confirming the block rule worked.

4. **Allowed SSH (Port 22)** *(for example purposes)*  
   - Created a new **Inbound Rule** for TCP port **22**.
   - Selected **Allow the connection** and applied it to all profiles.

5. **Removed the test block rule**  
   - Located **Block Telnet** in **Inbound Rules**.
   - Right-clicked and selected **Delete**.

## Test Results
- **Telnet** traffic (port 23) was successfully blocked.
- **SSH** traffic (port 22) was allowed without issues.
- Firewall rules were clearly visible in the inbound rules list.

## Screenshots
Screenshots of:
1. The Block Telnet rule creation.
2. The rules list showing applied firewall rules.

All screenshots are available in the [Screenshots](./Screenshots) folder.

## Key Learning
This task reinforced:
- How Windows Firewall filters inbound and outbound traffic.
- How to create, test, and remove custom firewall rules.
- Why blocking unused or insecure ports (like Telnet) improves security.
