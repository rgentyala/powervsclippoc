This directory contains the sample Terraform code to create a Power virtual server instance image. 

To create your own Power virtual server instance image, you should fork this repository and then modify the local variable `public_image_name` in the file `main.tf` to reference your own publicly availble image.

## Before you begin

  Verify that your custom image is publicly available in all supported regions.

  Make sure that you have the following IBM Cloud Identity and Access Management (IAM) permissions:

   * Manager service access role for IBM Cloud Schematics
   * TODO: Need IAM Permissions for Power here...
  
  TODO: Anything else needed here?

## Required resources

  * Create a Power Systems Virtual Server Instance. For more information, see [Getting started with IBM Power Systems Virtual Servers](https://cloud.ibm.com/docs/power-iaas?topic=power-iaas-getting-started).  
  * Create a [SSH key](https://www.ibm.com/docs/en/power-systems-vs?topic=aix-creating-virtual-machine-vm-ssh-keys-root-login).   
  * Create a [Network](https://www.ibm.com/docs/en/power-systems-vs?topic=networking-configuring-adding-private-network-subnet).
  
## Installing the software

To install the software, configure the following required variables:
  * Select a Power Systems Virtual Server Instance
  * Enter a name for the new image instance that is being created
  * Enter an SSH Key Name for the selected server instance
  * Enter a Network Name or ID for the selected server instance.  

If necessary, modify the optional configuration items related to [memory](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/pi_instance#pi_memory), [processors](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/pi_instance#pi_processors), [processor type](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/pi_instance#pi_proc_type), and [system type](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/pi_instance#pi_sys_type).

## Upgrading to a new version

Run the image instance to install fixes or updates. Update and fix commands must be run from the OS itself.

## Uninstalling the software

Complete the following steps to uninstall a Helm Chart from your account. 

1. Go to the **Menu** > **Schematics**.
2. Select your workspace name. 
3. Click **Actions** > **Destroy resources**. All resources in your workspace are deleted.
4. Click **Update**.
5. To delete your workspace, click **Actions** > **Delete workspace**. 
