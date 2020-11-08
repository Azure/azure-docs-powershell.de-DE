---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 4ef8c131e0094928808e6479b2c5ffe40090c5d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166411"
---
# <span data-ttu-id="3d4eb-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4eb-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3d4eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4eb-103">Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="3d4eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d4eb-104">SYNTAX</span></span>

### <span data-ttu-id="3d4eb-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d4eb-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3d4eb-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d4eb-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3d4eb-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="3d4eb-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d4eb-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="3d4eb-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="3d4eb-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d4eb-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4eb-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="3d4eb-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d4eb-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d4eb-120">DESCRIPTION</span></span>
<span data-ttu-id="3d4eb-121">Das Cmdlet " **Satz-AzKeyVaultAccessPolicy** " gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="3d4eb-122">Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen im schlüsseltresor haben, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="3d4eb-123">Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, betrifft dieser Vorgang nur Benutzer in dieser Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="3d4eb-124">Die folgenden Verzeichnisse müssen alle das gleiche Azure-Verzeichnis aufweisen:</span><span class="sxs-lookup"><span data-stu-id="3d4eb-124">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="3d4eb-125">Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsselspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="3d4eb-126">Das Azure-Verzeichnis, in dem sich der Benutzer oder die Anwendungsgruppe befindet, dem Sie Berechtigungen erteilen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="3d4eb-127">Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert, sind:</span><span class="sxs-lookup"><span data-stu-id="3d4eb-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 
- <span data-ttu-id="3d4eb-128">Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="3d4eb-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="3d4eb-129">Jede Organisation verfügt über ein eigenes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-129">Each organization has its own directory.</span></span> 
- <span data-ttu-id="3d4eb-130">Ihr Azure-Konto verfügt über mehrere Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="3d4eb-131">Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht autorisieren, um Ihren schlüsseltresor zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="3d4eb-132">Die Anwendung muss sich im Standardverzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-132">The application must be in the default directory.</span></span>
<span data-ttu-id="3d4eb-133">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="3d4eb-134">Wenn Sie einen Dienstprinzipal verwenden, um Zugriffsrichtlinien Berechtigungen zu erteilen, müssen Sie den `-BypassObjectIdValidation` Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="3d4eb-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d4eb-135">EXAMPLES</span></span>

### <span data-ttu-id="3d4eb-136">Beispiel 1: Erteilen von Berechtigungen für einen Benutzer für einen schlüsseltresor und Ändern der Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="3d4eb-137">Der erste Befehl gewährt einem Benutzer in Azure Active Directory Berechtigungen, PattiFuller@contoso.com um Vorgänge für Schlüssel und Geheimnisse mit einem schlüsseltresor mit dem Namen Contoso03Vault durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="3d4eb-138">Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="3d4eb-139">Mit dem zweiten Befehl werden die Berechtigungen geändert, die PattiFuller@contoso.com im ersten Befehl gewährt wurden, sodass Sie nun zusätzlich zu den Einstellungen und Löschungen auch Geheimnisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="3d4eb-140">Die Berechtigungen für Schlüsselvorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="3d4eb-141">Der endgültige Befehl ändert weiterhin die vorhandenen Berechtigungen für PattiFuller@contoso.com , um alle Berechtigungen für wichtige Vorgänge zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="3d4eb-142">Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-142">The permissions to secret operations remain unchanged after this command.</span></span> 

### <span data-ttu-id="3d4eb-143">Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienst Prinzipal zum Lesen und Schreiben von Geheimnissen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3d4eb-144">Dieser Befehl gewährt Berechtigungen für eine Anwendung für einen schlüsseltresor mit dem Namen Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> <span data-ttu-id="3d4eb-145">Der *servicePrincipalName* -Parameter gibt die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="3d4eb-146">Die Anwendung muss in Ihrem Azure Active Directory registriert sein.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="3d4eb-147">Der Wert des *servicePrincipalName* -Parameters muss entweder der Dienstprinzipalname der Anwendung oder die GUID der Anwendungs-ID sein.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="3d4eb-148">In diesem Beispiel wird der Dienstprinzipalname angegeben http://payroll.contoso.com , und der Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-148">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="3d4eb-149">Beispiel 3: Erteilen von Berechtigungen für eine Anwendung unter Verwendung der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="3d4eb-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3d4eb-150">Dieser Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="3d4eb-151">In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienst Prinzipals der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="3d4eb-152">Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="3d4eb-153">Dieser Befehl gewährt Get-, List-und festgelegte Berechtigungen für den angegebenen Benutzerprinzipalnamen für den Zugriff auf Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="3d4eb-154">Beispiel 5: Aktivieren von Geheimnissen aus einem schlüsseltresor durch den Microsoft. Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="3d4eb-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3d4eb-155">Dieser Befehl gewährt die Berechtigungen für Geheimnisse, die vom Contoso03Vault-schlüsseltresor vom Microsoft. Compute-Ressourcenanbieter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="3d4eb-156">Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="3d4eb-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="3d4eb-157">Der erste Befehl verwendet das Get-AzADGroup-Cmdlet, um alle Active Directory-Gruppen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="3d4eb-158">In der Ausgabe werden drei zurückgegebene Gruppen mit dem Namen " **group1** ", " **group2** " und " **Gruppe3** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-158">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="3d4eb-159">Mehrere Gruppen können denselben Namen haben, aber immer eine eindeutige ObjectID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="3d4eb-160">Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectID in der Ausgabe, um die gewünschte Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="3d4eb-161">Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzKeyVaultAccessPolicy, um group2-Berechtigungen für Ihren schlüsseltresor mit dem Namen **myownvault** zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="3d4eb-162">In diesem Beispiel werden die Gruppen mit dem Namen "group2" Inline in der gleichen Befehlszeile aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="3d4eb-163">In der zurückgegebenen Liste können mehrere Gruppen mit dem Namen "group2" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="3d4eb-164">In diesem Beispiel wird das erste Element mit dem Index \[ 0 \] in der zurückgegebenen Liste markiert.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="3d4eb-165">Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandanten Schlüssel (BYOK)</span><span class="sxs-lookup"><span data-stu-id="3d4eb-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="3d4eb-166">Mit diesem Befehl wird der Azure-Informationsschutz autorisiert, einen vom Kunden verwalteten Schlüssel (das Szenario "eigene Schlüssel" oder "BYOK") als Azure Information Protection-Mandanten Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="3d4eb-167">Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen schlüsseltresor Namen an, aber Sie müssen den *servicePrincipalName* -Parameter mit der GUID **00000012-0000-0000-C000-000000000000** angeben und die Berechtigungen im Beispiel angeben.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="3d4eb-168">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d4eb-168">PARAMETERS</span></span>

### <span data-ttu-id="3d4eb-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3d4eb-169">-ApplicationId</span></span>
<span data-ttu-id="3d4eb-170">Für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-170">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="3d4eb-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="3d4eb-172">Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="3d4eb-173">Verwenden Sie diesen Parameter nur, wenn Sie einer Objekt-ID, die sich auf eine delegierte Sicherheitsgruppe aus einem anderen Azure-Mandanten bezieht, Zugriff auf Ihren schlüsseltresor gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4eb-174">-DefaultProfile</span></span>
<span data-ttu-id="3d4eb-175">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d4eb-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-176">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="3d4eb-176">-EmailAddress</span></span>
<span data-ttu-id="3d4eb-177">Gibt die e-Mail-Adresse des Benutzers an, dem Sie Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="3d4eb-178">Diese e-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist, und eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3d4eb-179">-EnabledForDeployment</span></span>
<span data-ttu-id="3d4eb-180">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3d4eb-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3d4eb-182">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3d4eb-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3d4eb-184">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-185">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d4eb-185">-InputObject</span></span>
<span data-ttu-id="3d4eb-186">Vault-Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="3d4eb-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-187">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3d4eb-187">-ObjectId</span></span>
<span data-ttu-id="3d4eb-188">Gibt die Objekt-ID des Benutzers oder Dienst Prinzipals in Azure Active Directory an, für den Berechtigungen erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d4eb-189">-PassThru</span></span>
<span data-ttu-id="3d4eb-190">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3d4eb-191">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-191">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="3d4eb-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="3d4eb-193">Gibt ein Array von Zertifikat Berechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3d4eb-194">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="3d4eb-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3d4eb-195">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3d4eb-195">Get</span></span>
- <span data-ttu-id="3d4eb-196">Liste</span><span class="sxs-lookup"><span data-stu-id="3d4eb-196">List</span></span>
- <span data-ttu-id="3d4eb-197">Löschen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-197">Delete</span></span>
- <span data-ttu-id="3d4eb-198">Erstellen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-198">Create</span></span>
- <span data-ttu-id="3d4eb-199">Importieren</span><span class="sxs-lookup"><span data-stu-id="3d4eb-199">Import</span></span>
- <span data-ttu-id="3d4eb-200">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3d4eb-200">Update</span></span>
- <span data-ttu-id="3d4eb-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="3d4eb-201">Managecontacts</span></span>
- <span data-ttu-id="3d4eb-202">Getissuer</span><span class="sxs-lookup"><span data-stu-id="3d4eb-202">Getissuers</span></span>
- <span data-ttu-id="3d4eb-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="3d4eb-203">Listissuers</span></span>
- <span data-ttu-id="3d4eb-204">Setissuer</span><span class="sxs-lookup"><span data-stu-id="3d4eb-204">Setissuers</span></span>
- <span data-ttu-id="3d4eb-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="3d4eb-205">Deleteissuers</span></span>
- <span data-ttu-id="3d4eb-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="3d4eb-206">Manageissuers</span></span>
- <span data-ttu-id="3d4eb-207">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-207">Recover</span></span>
- <span data-ttu-id="3d4eb-208">Backup</span><span class="sxs-lookup"><span data-stu-id="3d4eb-208">Backup</span></span>
- <span data-ttu-id="3d4eb-209">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="3d4eb-209">Restore</span></span>
- <span data-ttu-id="3d4eb-210">Purge</span><span class="sxs-lookup"><span data-stu-id="3d4eb-210">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="3d4eb-211">-PermissionsToKeys</span></span>
<span data-ttu-id="3d4eb-212">Gibt ein Array von Schlüssel Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3d4eb-213">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="3d4eb-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3d4eb-214">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="3d4eb-214">Decrypt</span></span>
- <span data-ttu-id="3d4eb-215">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="3d4eb-215">Encrypt</span></span>
- <span data-ttu-id="3d4eb-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="3d4eb-216">UnwrapKey</span></span>
- <span data-ttu-id="3d4eb-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="3d4eb-217">WrapKey</span></span>
- <span data-ttu-id="3d4eb-218">Prüfen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-218">Verify</span></span>
- <span data-ttu-id="3d4eb-219">Melden sich</span><span class="sxs-lookup"><span data-stu-id="3d4eb-219">Sign</span></span>
- <span data-ttu-id="3d4eb-220">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3d4eb-220">Get</span></span>
- <span data-ttu-id="3d4eb-221">Liste</span><span class="sxs-lookup"><span data-stu-id="3d4eb-221">List</span></span>
- <span data-ttu-id="3d4eb-222">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3d4eb-222">Update</span></span>
- <span data-ttu-id="3d4eb-223">Erstellen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-223">Create</span></span>
- <span data-ttu-id="3d4eb-224">Importieren</span><span class="sxs-lookup"><span data-stu-id="3d4eb-224">Import</span></span>
- <span data-ttu-id="3d4eb-225">Löschen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-225">Delete</span></span>
- <span data-ttu-id="3d4eb-226">Backup</span><span class="sxs-lookup"><span data-stu-id="3d4eb-226">Backup</span></span>
- <span data-ttu-id="3d4eb-227">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="3d4eb-227">Restore</span></span>
- <span data-ttu-id="3d4eb-228">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-228">Recover</span></span>
- <span data-ttu-id="3d4eb-229">Purge</span><span class="sxs-lookup"><span data-stu-id="3d4eb-229">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="3d4eb-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="3d4eb-231">Gibt ein Array von geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3d4eb-232">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="3d4eb-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3d4eb-233">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3d4eb-233">Get</span></span>
- <span data-ttu-id="3d4eb-234">Liste</span><span class="sxs-lookup"><span data-stu-id="3d4eb-234">List</span></span>
- <span data-ttu-id="3d4eb-235">Einrichten</span><span class="sxs-lookup"><span data-stu-id="3d4eb-235">Set</span></span>
- <span data-ttu-id="3d4eb-236">Löschen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-236">Delete</span></span>
- <span data-ttu-id="3d4eb-237">Backup</span><span class="sxs-lookup"><span data-stu-id="3d4eb-237">Backup</span></span>
- <span data-ttu-id="3d4eb-238">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="3d4eb-238">Restore</span></span>
- <span data-ttu-id="3d4eb-239">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-239">Recover</span></span>
- <span data-ttu-id="3d4eb-240">Purge</span><span class="sxs-lookup"><span data-stu-id="3d4eb-240">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="3d4eb-241">-PermissionsToStorage</span></span>
<span data-ttu-id="3d4eb-242">Gibt die Berechtigungen des verwalteten speicherkontos und des SAS-Definitionsvorgangs an, die einem Benutzer oder Dienstprinzipal gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-243">-ResourceGroupName</span></span>
<span data-ttu-id="3d4eb-244">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-244">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-245">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3d4eb-245">-ResourceId</span></span>
<span data-ttu-id="3d4eb-246">Schlüsseltresor-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3d4eb-246">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-247">-ServicePrincipalName</span></span>
<span data-ttu-id="3d4eb-248">Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="3d4eb-249">Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung im AzureActive-Verzeichnis registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="3d4eb-250">Die Anwendung mit dem Dienstprinzipalnamen, den dieser Parameter angibt, muss im Azure-Verzeichnis registriert sein, in dem sich das aktuelle Abonnement befindet.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d4eb-251">-UserPrincipalName</span></span>
<span data-ttu-id="3d4eb-252">Gibt den Benutzerprinzipalnamen des Benutzers an, dem Sie Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="3d4eb-253">Dieser Benutzerprinzipalname muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-254">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="3d4eb-254">-VaultName</span></span>
<span data-ttu-id="3d4eb-255">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="3d4eb-256">Mit diesem Cmdlet wird die Zugriffsrichtlinie für den schlüsseltresor geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-257">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-257">-Confirm</span></span>
<span data-ttu-id="3d4eb-258">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-258">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4eb-259">-WhatIf</span></span>
<span data-ttu-id="3d4eb-260">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d4eb-261">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-261">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4eb-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4eb-262">CommonParameters</span></span>
<span data-ttu-id="3d4eb-263">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4eb-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4eb-264">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d4eb-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4eb-265">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d4eb-265">INPUTS</span></span>

### <span data-ttu-id="3d4eb-266">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3d4eb-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="3d4eb-267">System. String</span><span class="sxs-lookup"><span data-stu-id="3d4eb-267">System.String</span></span>

## <span data-ttu-id="3d4eb-268">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d4eb-268">OUTPUTS</span></span>

### <span data-ttu-id="3d4eb-269">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3d4eb-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3d4eb-270">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d4eb-270">NOTES</span></span>

## <span data-ttu-id="3d4eb-271">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d4eb-271">RELATED LINKS</span></span>

[<span data-ttu-id="3d4eb-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3d4eb-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="3d4eb-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d4eb-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

