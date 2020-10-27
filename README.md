Office 365 Tenant Details
=========================

            

This script is used to quickly retrieve all of the basic details about your Office 365 tenant and put them at your fingertips. If you are a tenant admin, or a Microsoft partner who administers tenants for your customers, this can save you a good bit of time
 sitting at the PowerShell command line.


It can also be useful if you want to write PowerShell code which alerts you on some of the values retrieved, such as 'DomainStatus=Unverified' which indicates that the DNS forward lookup zone for that MSOnline tenant domain hasn't been verified as being
 one you administer. Or quickly determine whether a user is licensed for a service or services by having them run this script and give you the results-as opposed to having to find them in the portal. If your concern is email administration this script
 quickly retrieves the users ProxyAddresses and AlternativeEmailAddresses for your to view what is set for that user.


**Frequently Asked Questions**


  *  This script will prompt for valid credentials for an identity in that tenant. The identity must not require password reset. Impersonation is not done by this script-you must have the password for that individual or have that individual run the script themselves
 and pass you the result. 
  *  This script does not require the person running it to be a tenant administrator identity for most information.

  *  If the user is not allowed to get information about roles (insufficient role access to run Get-MSRole) then the results will simply be false.

  *  The script requires that the Windows Azure Active Directory Module for Windows PowerShell be installed prior to running. More information on how to install that and the links to get it are available at
[this link](http://technet.microsoft.com/en-us/library/jj151815.aspx). 
  *  The script is essentially a formatted dump of the Get-MsolDomain, Get-MSolAccountSku and Get-MSRole.

  *  The licensing information for the user has license intepretation strings which can help remove some confusion about what the licensing actually provides services for.

  *  Data is returned in a 'master' PSObject which contains an assortment of single-value and multi-value noteproperties. Some of the noteproperties are other PSObjects so it would be very easy for this script to be separated into other smaller data retrieval
 scripts. 

**Sample Result** (from a non-tenant admin user in my own tenant)


 


![Image](https://github.com/azureautomation/office-365-tenant-details/raw/master/tenantinfo.jpg)

 

 


        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
