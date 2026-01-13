## 📖 Overview
This repository provides a **complete local installation setup for Odoo 17** on Ubuntu 24.04 LTS

It includes everything you need to run Odoo locally with a production-like environment:
- **Python virtual environment** setup for dependency management
- **PostgreSQL database configuration** for Odoo
- **Systemd service** to start Odoo automatically on boot
- **Nginx reverse proxy** for secure and efficient web access
- **Project structure and configuration files** for easy customization

This setup is ideal for:
- Developers who want to work on Odoo modules locally  
- Testing Odoo features before deploying to production  
- Learning Odoo 17 installation and configuration end-to-end

<img width="1792" height="576" alt="Gemini_Generated_Image_cs3xgrcs3xgrcs3x" src="https://github.com/user-attachments/assets/1a9f71b9-0e9a-494b-83e3-2bbc108150ed" />

### 🛠 Detailed Steps

1. Project Structure Initialization
Create the base directory and essential subfolders to keep the installation organized:
config/: For odoo.conf and Nginx configurations.
logs/: For Odoo and Nginx log files.
systemd/: To store the service unit file.

2. Prerequisites & Dependencies
Install the required system packages:
Python 3.12, pip, and virtualenv.
Development libraries for Odoo.
NodeJS & npm (for RTL support).
wkhtmltopdf (for PDF report generation).

3. PostgreSQL Database Setup
Install PostgreSQL server.
Create a dedicated database user matching your system user.
Configure Peer Authentication to allow seamless local connections.

4. Odoo 17 Source Code
Clone the official Odoo 17 branch directly from GitHub into your project folder.

5. Python Virtual Environment (venv)
Create a clean isolation layer using python3 -m venv venv.
Install all requirements listed in requirements.txt.
Note: Ensure setuptools is updated to avoid pkg_resources warnings.

6. Odoo Configuration
Create odoo.conf within the config/ directory. Key parameters:
db_user & db_password.
addons_path: Pointing to your Odoo and custom addons.
logfile: Path to your logs/ folder.

xmlrpc_port: Defaulting to 8069.

7. Systemd Service Integration
Create a systemd unit file to manage the Odoo process. This ensures:
Automatic start on system boot.
Automatic restart on failure.
Easy management via systemctl.

8. Nginx Reverse Proxy
Configure Nginx to handle incoming traffic on port 80/443:
Forward requests to Odoo (8069).
Handle Longpolling on port 8072 for real-time chat/updates.
Manage access and error logs within the project directory.

🏁 Verification
Once completed, the system should be accessible via:
Direct: http://your_ip:8069
Production: http://your_domain_or_ip (via Nginx)

## Key Capabilities

This Odoo 17 local installation setup provides the following capabilities:

- 🗂️ **Complete Odoo 17 Source Setup**: Includes all official Odoo 17 modules and core files.
- 🐍 **Python Virtual Environment**: Isolated environment for Python dependencies to avoid conflicts.
- 🐘 **PostgreSQL Database Integration**: Pre-configured for easy local development.
- ⚙️ **Systemd Service**: Automatic startup and background management of Odoo.
- 🌐 **Nginx Reverse Proxy**: Secure, production-like web access with optional SSL.
- 🧩 **Configurable Addons Path**: Easy to extend with custom modules.
- 📄 **Logs Management**: Centralized logs for Odoo and Nginx for debugging and monitoring.
- 📸 **Screenshots & Documentation**: Clear visual guidance for setup and usage.
- 🚀 **Ready for GitHub Deployment**: Clean project structure with `.gitignore` to avoid committing virtual environments or logs.



