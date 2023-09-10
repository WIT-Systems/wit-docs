
# Setting up a Proxy Host with NGINX Proxy Manager

In this guide, we will walk through the process of setting up a proxy host using NGINX Proxy Manager's web portal. This involves creating a DNS record to point to the proxy server and configuring the proxy using the NGINX Proxy Manager interface.

## Step 1: Create a DNS Record

1. Log in to your domain registrar or DNS hosting provider's control panel.

2. Navigate to the DNS management section.

3. Create a new DNS record (A or CNAME) that points to the IP address of your proxy server. This DNS record will be used to access the proxy host. For example, you can create a record like `helloworld.example.com` and set it to the IP address of the WIT proxy server.

   ```WIT-proxy IP
   178.194.170.189
   ```

4. Save the DNS record.

5. It may take some time for DNS changes to propagate across the internet. Be patient and wait for the DNS record to fully propagate.

## Step 2: Access the NGINX Proxy Manager Web Portal

1. Open a web browser.

2. Navigate to the [NGINX Proxy Manager web portal](https://nginx.wicki.sbs)

3. Log in to the NGINX Proxy Manager web portal using your credentials. If you do not have any or forgot your password, please go to our [Helpdesk](https://support.wicki.sbs/en/customer/create-ticket/)

## Step 3: Configure the Proxy Host

1. In the NGINX Proxy Manager dashboard, click on "Proxy Hosts" in the left sidebar.

2. Click the "Add Proxy Host" button.

3. Fill out the following details:
   - **Domain Names:** Enter the domain name you created in Step 1 (e.g., `helloworld.example.com`).
   - **Scheme:** Choose the appropriate scheme (HTTP, HTTPS, or HTTP/HTTPS).
   - **Forward Hostname/IP:** Enter the hostname or IP address of the destination server you want to proxy to.
   - **Forward Port:** Specify the port on the destination server where you want to forward the traffic.

4. Click the "Create" button to save the proxy host configuration.

5. Review the SSL settings if you want to enable HTTPS. You may need to provide SSL certificates for your domain. (If you are using cloudflare, you will automattically get https without reviewing these settings)

6. Once the configuration is saved, NGINX Proxy Manager will automatically generate the NGINX configuration and start proxying traffic to the specified destination server.

7. Test the proxy host by accessing it through your browser or a tool like `curl` to ensure that traffic is being properly redirected to the destination server or just open the created proxy.

Congratulations! You have successfully set up a proxy host with NGINX Proxy Manager's web portal, created a DNS record to point to the proxy server, and configured the proxy to forward traffic to the desired destination server.
