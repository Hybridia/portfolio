# ProcessDisk Tool Documentation

## Overview

ProcessDisk is a system utility designed to monitor and analyze disk I/O operations on a per-process basis. It provides detailed insights into how individual processes interact with the disk subsystem, helping identify performance bottlenecks and problematic applications.

## System Requirements

- **OS**: Windows 10/11 or Windows Server 2016+
- **Runtime**: .NET Framework 4.7.2 or higher
- **Privileges**: Administrator rights required
- **Disk Space**: 10MB minimum

## Installation

1. No installation required - the tool is portable
2. Download the executable to a location of your choice
3. Right-click and select "Run as Administrator" for full functionality

## Usage

### Basic Usage

```
processdisk.exe [options]
```

### Parameters

| Parameter | Description | Required | Default Value |
|-----------|-------------|----------|---------------|
| `--interval` | Sampling interval in seconds | No | 5 |
| `--top` | Number of processes to display | No | 10 |
| `--output` | CSV output file path | No | None |
| `--filter` | Process name filter | No | None |
| `--threshold` | Minimum I/O to display (KB) | No | 0 |

### Examples

Monitor top 10 processes with 2-second update interval:
```
processdisk.exe --interval 2 --top 10
```

Monitor only browser processes:
```
processdisk.exe --filter chrome,firefox,edge
```

Export results to CSV:
```
processdisk.exe --output disk_activity.csv --interval 30
```

## Output Explanation

The tool displays the following metrics for each process:

- **Process Name**: Name of the executable
- **PID**: Process ID
- **Read Rate**: Current disk read rate in KB/s
- **Write Rate**: Current disk write rate in KB/s
- **Total I/O**: Combined read/write operations in KB/s
- **Read Ops**: Number of read operations per second
- **Write Ops**: Number of write operations per second
- **Avg. Latency**: Average I/O operation latency in ms

## Common Use Cases

1. **Performance Troubleshooting**: Identify processes causing disk bottlenecks
2. **Application Assessment**: Evaluate the disk efficiency of applications
3. **System Monitoring**: Regular monitoring of disk activity patterns
4. **Capacity Planning**: Determine disk I/O requirements for applications

## Troubleshooting

- **Access Denied Errors**: Ensure you're running with Administrator privileges
- **Missing Data**: Some system processes may not report complete I/O statistics
- **High CPU Usage**: Reduce sampling frequency with `--interval` option
- **Empty Output**: Check if processes are filtered by threshold or name filters

## Version History

- v1.0.0 - Initial release with basic monitoring
- v1.1.0 - Added CSV export capability
- v1.2.0 - Added process filtering
- v1.3.0 - Improved performance and reduced overhead
- v2.0.0 - Complete rewrite with enhanced metrics

## Known Issues

- May report incomplete data for some system processes
- High sampling rates (<1s) may impact system performance
- Some virtualized environments may show inaccurate statistics