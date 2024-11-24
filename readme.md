# Daemonize

`Daemonize` is a script that converts an application or script into a daemon. It can be moved to `/usr/bin` for easy access.

## Installation

To install `Daemonize`, download the script from the releases page and move it to `/usr/bin`:

```sh
curl https://github.com/CrakA2/Daemonize/releases/download/beta/daemonize -O daemonize
sudo mv daemonize /usr/bin/
```

Usage
Direct CLI Flags
You can run the script directly with command-line flags to provide the necessary information:

Options:

-b binary: Path to the executable binary.
-p absolute_path: Absolute path to the executable.
-h, --help: Show the help message and exit.
Guided Mode
If you run the script without any flags, it will guide you through the process interactively:

Executable Path: You will be prompted to enter the path to the executable.
Initialization Command: You will be prompted to enter the initialization command (e.g., python3, node, go run, or leave it empty).
Service Description: You will be prompted to enter a description for the service.
Service User: You will be prompted to enter the user under which the service should run (default is root).
Start and Enable Service: You will be asked if you want to start the service immediately and if you want to enable it to start on boot.
Managing the Service
Once the service is created, you can manage it using the following commands:

Start the service: sudo systemctl start <service_name>
Stop the service: sudo systemctl stop <service_name>
Enable the service to start on boot: sudo systemctl enable <service_name>
Check the status of the service: sudo systemctl status <service_name>
View service logs: sudo journalctl -u <service_name>
Removing the Service
To remove the service, use the following commands:

Stop the service: sudo systemctl stop <service_name>
Disable the service: sudo systemctl disable <service_name>
Remove the service file: sudo rm /etc/systemd/system/<service_name>
Reload systemd: sudo systemctl daemon-reload
## License

This project is licensed under the GNU General Public License (GPL).

## Disclaimer

This software is provided "as is", without any warranty whatsoever. Use at your own risk.

## Contributing

Feel free to open an issue if you encounter any problems or have suggestions for improvements.
