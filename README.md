# IoT Kiosk Fleet Manager

Production system for managing a fleet of Linux-based 
smart kiosk devices — remote deployment, monitoring, 
and hardware integration.

## Stack
- Flutter (Linux desktop) — kiosk UI
- Python — device management scripts
- systemd — service management and auto-restart
- Tailscale — secure mesh VPN for fleet access
- DigitalOcean Kubernetes — cloud backend
- PostgreSQL — device state and job tracking
- Redis — real-time device status
- RabbitMQ — async command routing to devices
- Docker — containerized backend services

## Hardware
- Raspberry Pi / ARM Linux devices
- IR sensors — occupancy detection
- Electronic lock controllers — access control
- Dual-SIM 4G routers — network failover
- Remote camera integration

## Features
- Remote Flutter binary deployment across fleet
- Systemd watchdog with automatic service recovery
- Custom GTK kiosk mode (no window chrome)
- IR sensor settle delay for accurate detection
- Manual override flows for hardware failures
- Tailscale-based secure SSH access to all devices
- Automated post-build deployment scripts

## Deploy Command
bash post_build.sh && sudo systemctl restart kiosk.service
