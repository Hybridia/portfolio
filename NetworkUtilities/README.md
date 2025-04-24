# Network Utilities

A collection of tools for network diagnostics, monitoring, and management.

## Tools Included

### 3shapeconnection.exe
- **Purpose**: Specialized connection tool for 3Shape dental equipment networks
- **Key Features**:
  - Custom protocol support for dental equipment
  - Connection quality monitoring
  - Automatic reconnection capabilities
  - Diagnostic logging

### speedtest6.exe
- **Purpose**: Network speed testing with detailed metrics
- **Key Features**:
  - Download and upload speed measurement
  - Latency and packet loss testing
  - ISP connection quality assessment
  - Historical comparison of network performance

### portscanner.exe
- **Purpose**: Network port scanning and security assessment
- **Key Features**:
  - TCP/UDP port scanning
  - Service identification
  - Common vulnerability checking
  - Network topology mapping

### connection_log.txt
- **Purpose**: System for logging network connection events
- **Key Features**:
  - Connection establish/drop tracking
  - Timestamp and duration logging
  - Error code interpretation
  - Network event correlation

### interfacechanger.exe
- **Purpose**: Network interface configuration management
- **Key Features**:
  - Quick switching between network profiles
  - IP configuration management
  - DNS settings adjustment
  - VPN connection handling

### serveraccess.exe
- **Purpose**: Remote server access management and monitoring
- **Key Features**:
  - Connection security verification
  - Access log monitoring
  - Permission management
  - Session tracking

### remote.exe
- **Purpose**: Remote system management and control
- **Key Features**:
  - Remote command execution
  - System information retrieval
  - Remote process monitoring
  - Script execution capabilities

### checkhostnames.exe
- **Purpose**: DNS resolution and hostname verification
- **Key Features**:
  - Batch hostname resolution
  - DNS propagation checking
  - Hostname-to-IP mapping
  - FQDN validation

### checkactiveconnections2.exe
- **Purpose**: Active network connection monitoring
- **Key Features**:
  - Real-time connection tracking
  - Connection statistics
  - Suspicious connection alerting
  - Bandwidth usage per connection

### intercept.exe & InterCepter.exe
- **Purpose**: Network traffic inspection and analysis
- **Key Features**:
  - Packet capture and analysis
  - Protocol inspection
  - Traffic pattern detection
  - Security anomaly identification

## Usage

Most tools can be run directly from the command line. For detailed usage instructions for each tool, please see the documentation in the `/docs` folder.

## System Requirements

- Windows 10/11 or Windows Server 2016+
- .NET Framework 4.7.2 or higher
- Administrator privileges required for most tools
- WinPcap or Npcap for packet capture functionality

## Development

These tools were developed using C# and .NET Framework, with additional networking libraries including SharpPcap for packet capture capabilities.