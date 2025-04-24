# System Monitor Tools

A collection of utilities for monitoring system resources and performance.

## Tools Included

### processdisk.exe
- **Purpose**: Monitors disk usage by individual processes
- **Key Features**:
  - Real-time disk read/write tracking
  - Process-specific I/O measurement
  - Performance impact analysis
  - CSV export capability

### processdisk2.exe & processdisk3.exe
- **Purpose**: Enhanced versions with additional capabilities
- **Key Features**:
  - Historical data comparison
  - Alert thresholds for excessive disk usage
  - Network drive monitoring

### ram_usage3.exe
- **Purpose**: Detailed memory allocation and usage monitoring
- **Key Features**:
  - Per-process memory consumption
  - Memory leak detection
  - Historical trend analysis
  - System memory health assessment

### readmyram.exe & readmyramWithCPU.exe
- **Purpose**: Combined resource monitoring for memory and CPU
- **Key Features**:
  - Simultaneous CPU and RAM monitoring
  - Process prioritization recommendations
  - Resource bottleneck identification
  - Performance optimization suggestions

### diskreadandwriteread.exe
- **Purpose**: Disk I/O performance testing and benchmarking
- **Key Features**:
  - Sequential and random read/write testing
  - SSD vs HDD performance comparison
  - Disk health assessment
  - Performance bottleneck identification

## Usage

Most tools can be run directly from the command line. For detailed usage instructions for each tool, please see the documentation in the `/docs` folder.

## System Requirements

- Windows 10/11 or Windows Server 2016+
- .NET Framework 4.7.2 or higher
- Administrator privileges for some functionality

## Development

These tools were developed using C# and the .NET Framework, leveraging Windows Management Instrumentation (WMI) for system metrics collection.