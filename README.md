# Add storage to vm in Microsoft Azure
This tutorial is about how to manage your disks, add disks to your virtual machine on Microsoft Azure.

<a href="http://www.youtube.com/watch?feature=player_embedded&v=JyBUaBW_Zpo
" target="_blank"><img src="http://img.youtube.com/vi/JyBUaBW_Zpo/0.jpg" 
alt="Video Tutorial on how add extra disk to your VM on Microsoft Azure" width="240" height="180" border="10" /></a>

# 1) create the storage pool
- Launch Remote Desktop and connect to the VM on which you want to configure the storage space.
- If Server Manager does not appear by default, run it from the Start screen.
- Click the File And Storage Services tile near the middle of the window
- In the navigation pane, click Storage Pools
- In the Storage Pools area, click the Tasks drop-down list and select New Storage Pool
- In the New Storage Pool Wizard, click Next on the first page.
- Provide a name for the new storage pool, and click Next.
- Select all the disks you want to include in your storage pool, and click Next
- Click Create, and then click Close to create the storage pool

# 2) Create a Virtual Disk (from the storage pool)

- In Server Manager, in the Storage Pools dialog box, right-click your newly created storage pool and select New Virtual Disk
- Select your storage pool, and select OK
- Click Next on the first page of the wizard.
- Provide a name for the new virtual disk, and click Next.
- On the Specify enclosure resiliency page, click Next.
- Select the simple storage layout (because your VHDs are already triple replicated by Azure Storage, you do not need additional redundancy), and click Next
- For the provisioning type, leave the selection as Fixed. Click Next 
- For the size of the volume, select Maximum (Figure 1-22) so that the new virtual disk uses the complete capacity of the storage pool. Click Next
- On the Summary page, click Create.
- Click Close when the process completes

# 3) New Volume Wizard

- Click Next to skip past the first page of the wizard.
- On the Server And Disk Selection page, select the disk you just created . Click Next.
- Leave the volume size set to the maximum value and click Next
- Leave Assign A Drive Letter selected and select a drive letter to use for your new drive.
- Provide a name for the new volume, and click Next  
- Click Create.
- When the process completes, click Close.
- Open Windows Explorer to see your new drive listed

[Source](https://www.microsoftpressstore.com/store/exam-ref-70-532-developing-microsoft-azure-solutions-9781509304592)
