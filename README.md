
# Django Application Deployment on Rocky Linux 9

## Project Overview

Deployed a Django web application on Rocky Linux 9 using
Gunicorn as the WSGI application server and Nginx as a
reverse proxy.

Configured systemd to manage the Gunicorn application
service and enable automatic startup.

## Technology Stack

- Rocky Linux 9
- Python 3.9
- Django 4.2
- Gunicorn
- Nginx
- systemd
- SQLite
- firewalld
- SELinux

## Deployment Architecture

Client Browser
      |
      v
Nginx (Port 80)
      |
      v
Gunicorn (127.0.0.1:8000)
      |
      v
Django Application

## Implementation

1. Prepared Rocky Linux environment.
2. Installed Python and pip.
3. Created Django project and application.
4. Configured Python virtual environment.
5. Tested Django development server.
6. Installed and configured Gunicorn.
7. Created a dedicated Linux service account.
8. Configured systemd service.
9. Configured Nginx reverse proxy.
10. Configured firewall rules.
11. Configured SELinux for Nginx upstream connections.
12. Verified application accessibility through browser.

## Service Management

Start:
```bash
systemctl start django
```

Stop:
```bash
systemctl stop django
```

Restart:
```bash
systemctl restart django
```

Check status:
```bash
systemctl status django
```

View logs:
```bash
journalctl -u django -f
```

## Nginx Management

```bash
nginx -t
systemctl restart nginx
systemctl status nginx
```

## Repository Structure

- config/: Django project configuration
- dashboard/: Django application
- deployment/nginx/: Nginx configuration
- deployment/systemd/: systemd service definition
- screenshots/: Deployment evidence

## Deployment Result

The Django application was successfully hosted on
Rocky Linux 9 using Nginx and Gunicorn.

## Learning Outcomes

- Linux application hosting
- Python virtual environments
- Django application deployment
- WSGI application servers
- systemd service management
- Nginx reverse proxy configuration
- Linux permissions and service accounts
- Firewall and SELinux configuration
- Application troubleshooting

