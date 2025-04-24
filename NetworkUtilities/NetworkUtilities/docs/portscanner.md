# PortScanner Tool Documentation

## Overview

PortScanner is a network utility designed to scan and analyze open ports on local and remote systems. It helps identify available services, potential security vulnerabilities, and network configuration issues by systematically probing TCP/UDP ports and analyzing responses.

## System Requirements

- **OS**: Windows 10/11 or Windows Server 2016+
- **Runtime**: .NET Framework 4.7.2 or higher
- **Privileges**: Administrator rights recommended
- **Network**: Active network connection with target visibility

## Installation

1. No installation required - the tool is portable
2. Download the executable to a location of your choice
3. Right-click and select "Run as Administrator" for full functionality

## Usage

### Basic Usage

```
portscanner.exe [options] [targets]
```

### Parameters

| Parameter | Description | Required | Default Value |
|-----------|-------------|----------|---------------|
| `--target` | Target IP or hostname | Yes | None |
| `--range` | Port range to scan (start-end) | No | 1-1024 |
| `--timeout` | Connection timeout in ms | No | 500 |
| `--threads` | Number of concurrent threads | No | 50 |
| `--output` | Output file path | No | None |
| `--service` | Enable service identification | No | True |
| `--udp` | Include UDP ports in scan | No | False |

### Examples

Scan common ports on a single host:
```
portscanner.exe --target 192.168.1.1
```

Scan a specific port range:
```
portscanner.exe --target example.com --range 1-65535
```

Scan multiple hosts:
```
portscanner.exe --target 192.168.1.1,192.168.1.2,192.168.1.3 --range 20-30,80,443
```

Export results to CSV:
```
portscanner.exe --target 10.0.0.1 --output scan_results.csv
```

## Output Explanation

The tool displays the following information for each scanned port:

- **IP Address**: Target IP address
- **Port Number**: The port that was scanned
- **Status**: Open, Closed, or Filtered
- **Service**: Identified service name (if available)
- **Response Time**: Connection response time in ms
- **Banner**: Service banner information (if available)

## Common Use Cases

1. **Network Inventory**: Identify all running services on a network
2. **Security Assessment**: Find potentially vulnerable open ports
3. **Troubleshooting**: Verify if specific services are accessible
4. **Network Mapping**: Discover available hosts and services
5. **Compliance Checking**: Ensure only approved ports are open

## Troubleshooting

- **Slow Scans**: Reduce thread count or increase timeout
- **False Negatives**: Some firewalls may block scans without rejection
- **Incomplete Results**: Network congestion may affect scan accuracy
- **Service Identification Errors**: Some services may provide misleading banners

## Version History

- v1.0.0 - Initial release with basic TCP scanning
- v1.1.0 - Added UDP scanning capability
- v1.2.0 - Added service identification
- v2.0.0 - Complete rewrite with multi-threading
- v2.1.0 - Added banner grabbing functionality
- v2.2.0 - Improved accuracy and performance

## Known Issues

- Some antivirus software may flag as a potential threat
- UDP scanning is less reliable than TCP
- Very aggressive scans may be blocked by IDS/IPS systems
- Some cloud providers may block scanning activity