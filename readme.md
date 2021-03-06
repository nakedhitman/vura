## VURA: The VAMI Update Repository Appliance ##

About:
-----

The VAMI Update Repository Appliance is a tool to help you create a portable update repository for VMware VAMI-enabled VMware virtual appliances. This allows you to transport the necessary bits for performing upgrades to locations without internet access. It can also help to generate update ISO images for appliances that do not have them available for download.

Requirements:
----

[vApp Version]
 - ESXi 4.0U2+
 - 1 vCPU
 - 512 MB RAM
 - 16 GB Disk Space (thick provisioned)
 - Internet access for initial repository creation
 
[Source Version]
 - Python 2.7
 - Internet access for initial repository creation
 - User permission to bind port 80 (or use authbind - recommended)
 - (Optional) genisoimage - If you wish to be able to generate ISO images

Instructions
----

Download Here:
https://github.com/nakedhitman/vura/releases

[vApp Version (Recommended)] 

1. Deploy and boot VURA appliance in location with internet access
2. Obtain the Update URL from the administration page of your VAMI appliance (usually https://[your appliance IP]:5480)
3. Point your browser to the ip address of the VURA appliance
4. Paste the URL in the URL field of the UI
5. Give the repository a name without spaces or special characters
6. Press the Create button
7. Migrate the VURA appliance to your desired environment
8. You may now either download the ISO image and attach it to your VM to upgrade it, or paste the Update URL into the administration page of your appliance

[Source Version]

0. Ensure you have adequate disk space to host 2x the size of the update repository you will be downloading. You can assume it will be similar in size to the original OVA image you used to deploy it.
1. Download source tree to a machine that has Python 2.7
2. Execute vura.py as a user that can bind port 80 (or use authbind - recommended)
3. Follow appliance instructions starting at Step 2

Technologies Used:
----

 - Python 2.7
 - CherryPy
 - jQuery
 - DataTables
 - genisoimage
