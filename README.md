# RAM Monitor Script

![Bash](https://img.shields.io/badge/Shell-Bash-green)
![License](https://img.shields.io/badge/License-MIT-blue)

A simple Bash script to monitor available RAM and alert when it falls below a specified threshold.

## Features

- Checks current available RAM in megabytes
- Compares against a configurable threshold (default: 500MB)
- Provides clear warning messages when RAM is low
- Lightweight with no dependencies (uses standard Linux commands)

## Prerequisites

- Linux/Unix system
- Bash shell
- Standard GNU core utilities (`free`, `grep`, `awk`)

## Installation

1. Clone this repository or download the script:
```bash
git clone https://github.com/yourusername/RAM_Monitor_Script.git
cd RAM_Monitor_Script
```

2. Make the script executable:
```bash
chmod +x ram_status.sh
```

## Usage

### Basic Usage
```bash
./ram_status.sh
```

This will check RAM against the default threshold of 500MB.

### Custom Threshold
You can specify a custom threshold (in MB) as an argument:
```bash
./ram_status.sh 1000  # Sets threshold to 1000MB
```

### Scheduled Monitoring (via Cron)
Add to your crontab to run regularly (e.g., every 30 minutes):
```bash
*/30 * * * * /path/to/ram_status.sh >> /var/log/ram_status.log
```

## Output Examples

**When RAM is sufficient:**
```
RAM Space is sufficient - 2048 M
```

**When RAM is low:**
```
WARNING, RAM is running low
```

## Customization

You can easily modify the script to:
- Change the default threshold (edit the `TH` variable)
- Add email/Slack notifications when RAM is low
- Include percentage-based checks
- Log output to a file with timestamps

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you find this script useful, consider starring the repository! For issues or questions, please open a GitHub issue.
