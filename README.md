# 🛠️ Pi-Hole-Setup - Easy Network-Wide Ad Blocking

[![Download Pi-Hole-Setup](https://img.shields.io/badge/Download-Pi--Hole--Setup-brightgreen)](https://github.com/ahmedzaik/Pi-Hole-Setup/releases)

## 🚀 Getting Started

Pi-Hole-Setup offers an easy way to block ads across your entire network. This guide will help you download and set up the application, providing you with a seamless experience.

## 📦 What You Need

Before you begin, ensure you have:

- A computer with Docker installed. Check [Docker's installation guide](https://docs.docker.com/get-docker/).
- A stable internet connection.
- Basic knowledge of using a command line interface.
  
## 🔗 Key Features

- Deploy Pi-hole using Docker for simplicity.
- Configure DNS settings for Kali Linux.
- Set up router-level DNS for network-wide ad blocking.
- Use verification commands to confirm successful setup.

## 📥 Download & Install

To get started, visit this page to download: [Download Pi-Hole-Setup](https://github.com/ahmedzaik/Pi-Hole-Setup/releases).

1. Click on the link above to reach the Releases page.
2. Look for the latest version. You'll see options for different files.
3. Download the appropriate file for your operating system.

## 📋 Installation Steps

Once the download is complete, follow these steps:

1. **Open your terminal**: Depending on your operating system, this could be Command Prompt (Windows), Terminal (macOS, Linux), or any suitable command line interface.
   
2. **Navigate to your download directory**: Use the `cd` command to change your current directory to where you downloaded the file. For example:
   ```bash
   cd ~/Downloads
   ```

3. **Run the Docker command**: To start the Pi-hole setup, use the following command:
   ```bash
   docker-compose up -d
   ```
   
4. **Access the Pi-hole admin interface**: Open your web browser and go to `http://localhost/admin`. You can also use your server's IP address if running on a remote server.

5. **Complete the installation**: Follow the prompts in the user interface to finish setting up Pi-hole. This will include configuring your DNS settings and any additional preferences you may have.

## ⚙️ DNS Configuration for Kali Linux

For users running Kali Linux, follow these steps to configure your DNS settings:

1. Open a terminal.
   
2. Use the command to modify your network settings:
   ```bash
   nmcli dev set etho0 ipv4.dns "YOUR_PIHOLE_IP"
   ```
   Replace `YOUR_PIHOLE_IP` with the Pi-hole server's IP address.

3. Restart your network services:
   ```bash
   nmcli networking off && nmcli networking on
   ```

## 🔒 Router-Level DNS Enforcement

To enhance your Pi-hole setup, configure your router for DNS blocking. This ensures that all devices connecting to your network use Pi-hole as their DNS server.

1. **Log into your router**: Use your browser to enter the router's IP address.

2. **Find DNS settings**: This is usually in the WAN or DHCP settings area.

3. **Set the DNS server addresses**: Replace them with your Pi-hole server IP address.

4. **Save and reboot the router**: This finalizes the changes.

## ✅ Verification Commands

To confirm that Pi-hole is running correctly, you can run several commands in your terminal.

1. Check the status of Pi-hole:
   ```bash
   docker ps
   ```

2. Verify DNS resolution:
   ```bash
   nslookup pi.hole
   ```

3. Check for ads blocked since installation:
   ```bash
   pihole -c
   ```

## 📢 Need Help?

If you encounter issues or need further assistance, consider checking the official documentation on the GitHub repository or reaching out to the community for support.

## 🤝 Contributing

We welcome contributions to improve Pi-Hole-Setup. Please fork the repository, make your changes, and submit a pull request.

## 🔗 Learn More

For further information on Docker, Pi-hole, and network security, explore the following resources:

- [Docker Official Documentation](https://docs.docker.com/)
- [Pi-hole Official Documentation](https://docs.pi-hole.net/)
- [Kali Linux Documentation](https://www.kali.org/docs/)

By following these steps, you should successfully download, install, and configure Pi-Hole-Setup for your network. Enjoy ad-free browsing!