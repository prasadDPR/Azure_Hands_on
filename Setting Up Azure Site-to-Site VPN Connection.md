# Setting Up Azure Site-to-Site VPN Connection

**Introduction:**
Azure Site-to-Site VPN allows you to securely connect your on-premises network to your Azure Virtual Network over the internet. This documentation provides step-by-step instructions for configuring a Site-to-Site VPN connection in Azure.

**Prerequisites:**
- An active Azure subscription.
- Administrative access to Azure Portal.
- A compatible VPN device on your on-premises network.
- Network configuration details for both Azure and on-premises networks.

**Step 1: Network Configuration**
1. Log in to the Azure Portal (https://portal.azure.com).
2. Navigate to the Azure Virtual Network service.
3. Create a new virtual network or select an existing one.
4. Define the address space and subnets for your virtual network.
5. Ensure that the virtual network does not overlap with your on-premises network.
![alt text](file:///c%3A/Users/Dell/Desktop/Published%20images/S2S%20Vnet%20image.png)

**Step 2: VPN Gateway Deployment**
1. Within your virtual network, select "VPN Gateway" from the left menu.
2. Click on "Create VPN Gateway".
3. Choose the appropriate VPN Gateway SKU and other settings.
4. Review and confirm your configuration, then click "Create".
5. Wait for the VPN Gateway deployment to complete (this may take several minutes).

**Step 3: Local Network Gateway Configuration**
1. Navigate to the "Local Network Gateways" section within the VPN Gateway settings.
2. Click "Add" to create a new local network gateway.
3. Enter the public IP address of your on-premises VPN device.
4. Define the address space of your on-premises network.
5. Specify any additional settings required for your VPN device.
6. Click "Create" to save the local network gateway configuration.

**Step 4: Connection Setup**
1. Return to the VPN Gateway settings and select "Connections".
2. Click "Add" to create a new VPN connection.
3. Choose the VPN Gateway and local network gateway created earlier.
4. Configure the connection type (IKEv1/IKEv2) and authentication method.
5. Enter the pre-shared key for securing the connection.
6. Review the settings and click "OK" to create the VPN connection.
7. Once created, click on the connection to view its status.

**Step 5: Monitoring and Troubleshooting**
1. Monitor the status of the VPN connection in the Azure Portal.
2. Use Azure Network Watcher to diagnose connectivity issues if necessary.
3. Check the logs on your on-premises VPN device for any error messages.
4. Ensure that your on-premises firewall allows traffic to and from Azure VPN Gateway.

**Step 6: Security Considerations**
1. Ensure that encryption and authentication settings are configured securely.
2. Implement network security groups (NSGs) to control traffic flow.
3. Regularly review and update access controls and VPN configurations.

**Azure Site-to-Site VPN Documentation:**
- For detailed documentation on Azure Site-to-Site VPN, refer to the Azure documentation: [Azure Site-to-Site VPN](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal)
