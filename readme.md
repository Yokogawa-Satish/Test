<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-193476523-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-193476523-1');
</script>


# Install sample AI application on e-RT3 Plus device

Follow these steps to install the `sample-ai-application` on the e-RT3 Plus device:

1. Upload `installer.sh` and `sample-ai-application` on the e-RT3 Plus device.

   1.1. Log on to the e-RT3 Plus device with [WinSCP application](https://winscp.net/eng/download.php).

   1.2 In WinSCP, navigate to the folder (such as `/home/ert3/`) where you want to save the installer and executable files.

   1.3 Drag-and-drop or copy-and-paste the application folder (`sample-ai-application`) from your local computer to the location specified in the previous step.

2. Navigate to the application folder (such as `/home/ert3/sample-ai-application`) in the terminal.

   2.1 Open the [putty application](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html).

   2.2 Configure the settings as follows:

   - `Host Name (or IP address)`: **IP address of the e-RT3 Plus device**
   - `Port`: **22**
   - `Connection Type`: **SSH**

   2.3 Click `Open`.

   2.4 Type your username and then the password to log in.

   2.5 After logging in successfully, navigate to the same uploaded folder (such as `/home/ert3/sample-ai-application`) by using the `cd` command.

   ```bash
   cd /home/ert3/sample-ai-application
   ```

3. Execute the `installer.sh` file.

   3.1 Verify that `installer.sh` and `sample-ai-application` are uploaded to the specified location by using the `ls` command.

   3.2 Grant the executable permission to the `installer.sh` file by using `chmod` command.

   ```bash
   sudo chmod +x installer.sh
   ```

   > **Note:** [Click here](https://github.com/Yokogawa-Technologies-Solutions-India/e-RT3-docs/blob/master/Articles/Azure/Send-telemetry-data-from-e-RT3-to-azure-IoT-hub.md#enabling-sudo-user) to read about enabling **_sudo privileges_**.

   3.3 Install the application by using the following command:

   ```bash
   sudo ./installer.sh
   ```

4. Use the sample AI application

   4.1 Open your web browser. For example, [Google Chrome](https://www.google.com/chrome/index.html)

   4.2 In the address bar, specify the URL with `9092` as the port number in the following format:

   ```text
   http://<IP_ADDRESS_OF_ERT3_DEVICE>:9092/
   ```

   > **_Note:_** Replace IP_ADDRESS_OF_ERT3_DEVICE with the IP address of your e-RT3 Plus device.
   > 
