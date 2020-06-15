# Pre-requisites to deploy Windows Virtual Desktop

To deploy a Windows Virtual Desktop environment, we need a pre-created windows domain (e.g: contoso.com). This can be created one of the following:

1. Azure Active Directory Domain Services(AADDS)
2. Windows Active Directory

In this lab, we have used AADDS and it is pre-provisioned. The Domain name will be the suffix of your lab user account (Eg: If your lab user account is *odl_user_189588@**azurehol1057.onmicrosoft.com***, the domain will be **azurehol1057.onmicrosoft.com**.) Your lab user account is given ‘AAD DC Administrator’ privilege, hence can be used to domain join machines later. 
