# CrowdStrike-Windows-BlueScreen-rememdiation
本周五，即7月19日，发生了一起CrowdStrike Agent问题，导致Windows出现蓝屏。为确保云环境的高效和优质的运维体验，以下是针对主要云服务提供商的一站式修复建议。

On Friday of this week, that is, July 19th, a CrowdStrike Agent issue occurred, causing Windows to have a blue screen. To ensure an efficient and excellent operation and maintenance experience of the cloud environment, here is a one-stop remediation suggestion for major cloud providers.

The following are suggestions we found on our official website from CrowdStrike. They may be officially revised by CrowdStrike. Please refer to the official website link for details.
https://supportportal.crowdstrike.com/s/article/Tech-Alert-Windows-crashes-related-to-Falcon-Sensor-2024-07-19

==================================================================

The official workaround is now confirmed as follows:

Boot Windows into Safe Mode or the Windows Recovery Environment.

Navigate to the C:\Windows\System32\drivers\CrowdStrike directory.

Locate the file matching “C-00000291*.sys” and delete it.

Boot the host normally.

==================================================================

For more information, please refer to the following link:



## #Powershell-AWS

### Step 0: Set Credential and region
你可以使用相关的循环进行批量遍历，这里只进行一个account Credential 和一个region的设置。 
You can use relevant loops for batch traversal. Here, we only set the credentials and region for one account.

### Step 1: 定义新实例的ID
Define the new instance ID.

### Step 2: 停止实例并解绑"安装了CrowdStrike Agent windows instance"的系统卷
停止实例并解绑“安装了CrowdStrike Agent的Windows实例”的系统卷。  
Stop the instance and detach the system volume of the "CrowdStrike Agent installed Windows instance".

### Step 3: 挂载卷到新实例
Attach the volume to the new instance.

### Step 4: 在新实例上删除指定路径下的文件
在新实例上删除指定路径下的文件。  
Delete files in the specified path on the new instance.

### Step 5: 卸载卷并重新挂载到原始实例
Detach the volume and reattach it to the original instance.

### Step 6: 启动原始实例
Start the original instance.
