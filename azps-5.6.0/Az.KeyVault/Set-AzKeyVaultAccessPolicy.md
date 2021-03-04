---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919907"
---
# <span data-ttu-id="d4f7b-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4f7b-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="d4f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f7b-103">Erteilt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem Schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="d4f7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4f7b-104">SYNTAX</span></span>

### <span data-ttu-id="d4f7b-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4f7b-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d4f7b-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="d4f7b-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d4f7b-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="d4f7b-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d4f7b-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4f7b-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="d4f7b-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4f7b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4f7b-120">DESCRIPTION</span></span>
<span data-ttu-id="d4f7b-121">Das **Cmdlet Set-AzKeyVaultAccessPolicy** gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem Schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="d4f7b-122">Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen für den Schlüsseltresor besitzen, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="d4f7b-123">Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, betrifft dieser Vorgang nur Benutzer in dieser Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="d4f7b-124">Die folgenden Verzeichnisse müssen alle dasselbe Azure-Verzeichnis sein:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="d4f7b-125">Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsseltresor befindet.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="d4f7b-126">Das Azure-Verzeichnis, das den Benutzer oder die Anwendungsgruppe enthält, dem Sie Berechtigungen erteilen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="d4f7b-127">Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert, sind:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="d4f7b-128">Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d4f7b-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="d4f7b-129">Jede Organisation verfügt über ein eigenes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="d4f7b-130">Ihr Azure-Konto verfügt über mehrere Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="d4f7b-131">Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht autorisieren, Ihren Schlüsseltresor zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="d4f7b-132">Die Anwendung muss sich im Standardverzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-132">The application must be in the default directory.</span></span>
<span data-ttu-id="d4f7b-133">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet zwar optional ist, Sie dies aber tun sollten, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="d4f7b-134">Wenn Sie einen Dienstprinzipal verwenden, um Zugriffsrichtlinienberechtigungen zu erteilen, müssen Sie den -Parameter `-BypassObjectIdValidation` verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="d4f7b-135">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4f7b-135">EXAMPLES</span></span>

### <span data-ttu-id="d4f7b-136">Beispiel 1: Erteilen von Berechtigungen für einen Benutzer für einen Schlüsseltresor und Ändern der Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="d4f7b-137">Der erste Befehl erteilt einem Benutzer in Azure Active Directory Berechtigungen zum Ausführen von Vorgängen an Schlüsseln und Geheimnissen mit einem Schlüsseltresor namens PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="d4f7b-138">Der *Parameter PassThru* führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="d4f7b-139">Mit dem zweiten Befehl werden die Berechtigungen geändert, die im ersten Befehl erteilt wurden, um nun das Abrufen von Geheim geheimen Daten sowie das Festlegen und Löschen der Berechtigungen PattiFuller@contoso.com zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="d4f7b-140">Die Berechtigungen für Schlüsselvorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="d4f7b-141">Mit dem endgültigen Befehl werden die vorhandenen Berechtigungen zum Entfernen aller Berechtigungen PattiFuller@contoso.com für Schlüsselvorgänge weiter geändert.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="d4f7b-142">Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="d4f7b-143">Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienstprinzipal zum Lesen und Schreiben von Geheimnissen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d4f7b-144">Dieser Befehl erteilt Berechtigungen für eine Anwendung für einen Schlüsseltresor namens Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="d4f7b-145">Der *Parameter ServicePrincipalName* gibt die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="d4f7b-146">Die Anwendung muss in Ihrem Azure Active Directory registriert sein.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="d4f7b-147">Der Wert des *Parameters ServicePrincipalName* muss entweder der Dienstprinzipalname der Anwendung oder die GUID der Anwendungs-ID sein.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="d4f7b-148">In diesem Beispiel wird der Name des Dienstprinzipals angegeben, und der Befehl erteilt der Anwendung Berechtigungen zum Lesen `http://payroll.contoso.com` und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="d4f7b-149">Beispiel 3: Erteilen von Berechtigungen für eine Anwendung mit ihrer Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="d4f7b-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d4f7b-150">Dieser Befehl erteilt der Anwendung Berechtigungen zum Lesen und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="d4f7b-151">In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienstprinzipals der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="d4f7b-152">Beispiel 4: Erteilen von Berechtigungen für einen Prinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="d4f7b-153">Dieser Befehl gewährt "Get", "List" und "Set"-Berechtigungen für den angegebenen Benutzerprinzipalnamen für den Zugriff auf Geheiminformationen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="d4f7b-154">Beispiel 5: Aktivieren des Abrufens von Geheiminformationen aus einem Schlüsseltresor durch den Microsoft.Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="d4f7b-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="d4f7b-155">Mit diesem Befehl werden die Berechtigungen für Geheiminformationen erteilt, die vom Microsoft.Compute-Ressourcenanbieter aus dem Contoso03Vault-Schlüsseltresor abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="d4f7b-156">Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="d4f7b-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="d4f7b-157">Der erste Befehl verwendet das Get-AzADGroup-Cmdlet, um alle Active Directory-Gruppen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="d4f7b-158">In der Ausgabe werden drei gruppen zurückgegeben, **benannte Gruppen1**, **Gruppe2** und **Gruppe3 angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="d4f7b-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="d4f7b-159">Mehrere Gruppen können denselben Namen haben, aber immer eine eindeutige ObjectId haben.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="d4f7b-160">Wenn mehrere Gruppen mit demselben Namen zurückgegeben werden, verwenden Sie die ObjectId in der Ausgabe, um die zu verwendende Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="d4f7b-161">Anschließend verwenden Sie die Ausgabe dieses Befehls Set-AzKeyVaultAccessPolicy, um Berechtigungen für Group2 für Ihren Schlüsseltresor namens **myownvault zu erteilen.**</span><span class="sxs-lookup"><span data-stu-id="d4f7b-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="d4f7b-162">In diesem Beispiel werden die Gruppen mit dem Namen "gruppe2" inline in derselben Befehlszeile aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="d4f7b-163">Die zurückgegebene Liste enthält möglicherweise mehrere Gruppen mit dem Namen "Gruppe2".</span><span class="sxs-lookup"><span data-stu-id="d4f7b-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="d4f7b-164">In diesem Beispiel wird das erste Beispiel, das durch Index 0 in der zurückgegebenen \[ \] Liste angegeben ist, verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="d4f7b-165">Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandantenschlüssel (BYOK)</span><span class="sxs-lookup"><span data-stu-id="d4f7b-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="d4f7b-166">Mit diesem Befehl wird Azure Information Protection autorisiert, einen vom Kunden verwalteten Schlüssel (das Szenario "Bring your own key" oder "BYOK") als Azure Information Protection-Mandantenschlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="d4f7b-167">Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen Schlüsseltresornamen an, müssen aber den *Parameter ServicePrincipalName* mit der GUID **00000012-0000-0000-c000-0000-0000000000** angeben und die Berechtigungen im Beispiel angeben.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="d4f7b-168">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4f7b-168">PARAMETERS</span></span>

### <span data-ttu-id="d4f7b-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-169">-ApplicationId</span></span>
<span data-ttu-id="d4f7b-170">Für die zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-170">For future use.</span></span>

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

### <span data-ttu-id="d4f7b-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="d4f7b-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="d4f7b-172">Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="d4f7b-173">Verwenden Sie diesen Parameter nur, wenn Sie zugriff auf Ihren Schlüsseltresor auf eine Objekt-ID gewähren möchten, die sich auf eine delegierte Sicherheitsgruppe von einem anderen Azure-Mandanten bezieht.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="d4f7b-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f7b-174">-DefaultProfile</span></span>
<span data-ttu-id="d4f7b-175">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d4f7b-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4f7b-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d4f7b-176">-EmailAddress</span></span>
<span data-ttu-id="d4f7b-177">Gibt die E-Mail-Adresse des Benutzers an, dem Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d4f7b-178">Diese E-Mail-Adresse muss im Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist, und eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="d4f7b-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d4f7b-179">-EnabledForDeployment</span></span>
<span data-ttu-id="d4f7b-180">Ermöglicht dem Microsoft.Compute-Ressourcenanbieter das Abrufen von Geheimnissen aus diesem Schlüsseltresor, wenn bei der Ressourcenerstellung auf diesen Schlüsseltresor verwiesen wird, z. B. beim Erstellen eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="d4f7b-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d4f7b-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d4f7b-182">Ermöglicht es dem Azure-Datenträgerverschlüsselungsdienst, Geheimnisse zu erhalten und Schlüssel aus diesem Schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="d4f7b-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d4f7b-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d4f7b-184">Ermöglicht Azure Resource Manager das Erhalten von Geheimnissen aus diesem Schlüsseltresor, wenn in einer Vorlagenbereitstellung auf diesen Schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="d4f7b-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4f7b-185">-InputObject</span></span>
<span data-ttu-id="d4f7b-186">Schlüsseltresorobjekt</span><span class="sxs-lookup"><span data-stu-id="d4f7b-186">Key Vault Object</span></span>

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

### <span data-ttu-id="d4f7b-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-187">-ObjectId</span></span>
<span data-ttu-id="d4f7b-188">Gibt die Objekt-ID des Benutzers oder Dienstprinzipals in Azure Active Directory an, für den Berechtigungen erteilt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="d4f7b-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4f7b-189">-PassThru</span></span>
<span data-ttu-id="d4f7b-190">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4f7b-191">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d4f7b-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="d4f7b-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="d4f7b-193">Gibt ein Array von Zertifikatberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d4f7b-194">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d4f7b-195">Alle</span><span class="sxs-lookup"><span data-stu-id="d4f7b-195">All</span></span>
- <span data-ttu-id="d4f7b-196">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d4f7b-196">Get</span></span>
- <span data-ttu-id="d4f7b-197">Liste</span><span class="sxs-lookup"><span data-stu-id="d4f7b-197">List</span></span>
- <span data-ttu-id="d4f7b-198">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-198">Delete</span></span>
- <span data-ttu-id="d4f7b-199">Erstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-199">Create</span></span>
- <span data-ttu-id="d4f7b-200">Importieren</span><span class="sxs-lookup"><span data-stu-id="d4f7b-200">Import</span></span>
- <span data-ttu-id="d4f7b-201">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d4f7b-201">Update</span></span>
- <span data-ttu-id="d4f7b-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="d4f7b-202">Managecontacts</span></span>
- <span data-ttu-id="d4f7b-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="d4f7b-203">Getissuers</span></span>
- <span data-ttu-id="d4f7b-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="d4f7b-204">Listissuers</span></span>
- <span data-ttu-id="d4f7b-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="d4f7b-205">Setissuers</span></span>
- <span data-ttu-id="d4f7b-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="d4f7b-206">Deleteissuers</span></span>
- <span data-ttu-id="d4f7b-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="d4f7b-207">Manageissuers</span></span>
- <span data-ttu-id="d4f7b-208">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-208">Recover</span></span>
- <span data-ttu-id="d4f7b-209">Sicherung</span><span class="sxs-lookup"><span data-stu-id="d4f7b-209">Backup</span></span>
- <span data-ttu-id="d4f7b-210">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-210">Restore</span></span>
- <span data-ttu-id="d4f7b-211">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f7b-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="d4f7b-212">-PermissionsToKeys</span></span>
<span data-ttu-id="d4f7b-213">Gibt ein Array mit Schlüsselvorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d4f7b-214">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d4f7b-215">Alle</span><span class="sxs-lookup"><span data-stu-id="d4f7b-215">All</span></span>
- <span data-ttu-id="d4f7b-216">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="d4f7b-216">Decrypt</span></span>
- <span data-ttu-id="d4f7b-217">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="d4f7b-217">Encrypt</span></span>
- <span data-ttu-id="d4f7b-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="d4f7b-218">UnwrapKey</span></span>
- <span data-ttu-id="d4f7b-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="d4f7b-219">WrapKey</span></span>
- <span data-ttu-id="d4f7b-220">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-220">Verify</span></span>
- <span data-ttu-id="d4f7b-221">Signieren</span><span class="sxs-lookup"><span data-stu-id="d4f7b-221">Sign</span></span>
- <span data-ttu-id="d4f7b-222">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d4f7b-222">Get</span></span>
- <span data-ttu-id="d4f7b-223">Liste</span><span class="sxs-lookup"><span data-stu-id="d4f7b-223">List</span></span>
- <span data-ttu-id="d4f7b-224">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d4f7b-224">Update</span></span>
- <span data-ttu-id="d4f7b-225">Erstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-225">Create</span></span>
- <span data-ttu-id="d4f7b-226">Importieren</span><span class="sxs-lookup"><span data-stu-id="d4f7b-226">Import</span></span>
- <span data-ttu-id="d4f7b-227">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-227">Delete</span></span>
- <span data-ttu-id="d4f7b-228">Sicherung</span><span class="sxs-lookup"><span data-stu-id="d4f7b-228">Backup</span></span>
- <span data-ttu-id="d4f7b-229">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-229">Restore</span></span>
- <span data-ttu-id="d4f7b-230">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-230">Recover</span></span>
- <span data-ttu-id="d4f7b-231">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f7b-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="d4f7b-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="d4f7b-233">Gibt ein Array mit geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d4f7b-234">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d4f7b-235">Alle</span><span class="sxs-lookup"><span data-stu-id="d4f7b-235">All</span></span>
- <span data-ttu-id="d4f7b-236">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d4f7b-236">Get</span></span>
- <span data-ttu-id="d4f7b-237">Liste</span><span class="sxs-lookup"><span data-stu-id="d4f7b-237">List</span></span>
- <span data-ttu-id="d4f7b-238">Festlegen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-238">Set</span></span>
- <span data-ttu-id="d4f7b-239">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-239">Delete</span></span>
- <span data-ttu-id="d4f7b-240">Sicherung</span><span class="sxs-lookup"><span data-stu-id="d4f7b-240">Backup</span></span>
- <span data-ttu-id="d4f7b-241">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-241">Restore</span></span>
- <span data-ttu-id="d4f7b-242">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-242">Recover</span></span>
- <span data-ttu-id="d4f7b-243">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f7b-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="d4f7b-244">-PermissionsToStorage</span></span>
<span data-ttu-id="d4f7b-245">Gibt berechtigungen für verwaltete Speicherkonto- und SaS-Definition-Operation an, die einem Benutzer oder Dienstprinzipal erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d4f7b-246">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="d4f7b-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d4f7b-247">alle</span><span class="sxs-lookup"><span data-stu-id="d4f7b-247">all</span></span>
- <span data-ttu-id="d4f7b-248">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d4f7b-248">get</span></span>
- <span data-ttu-id="d4f7b-249">Liste</span><span class="sxs-lookup"><span data-stu-id="d4f7b-249">list</span></span>
- <span data-ttu-id="d4f7b-250">löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-250">delete</span></span>
- <span data-ttu-id="d4f7b-251">Set</span><span class="sxs-lookup"><span data-stu-id="d4f7b-251">set</span></span>
- <span data-ttu-id="d4f7b-252">Update</span><span class="sxs-lookup"><span data-stu-id="d4f7b-252">update</span></span>
- <span data-ttu-id="d4f7b-253">Regeneratekey</span><span class="sxs-lookup"><span data-stu-id="d4f7b-253">regeneratekey</span></span>
- <span data-ttu-id="d4f7b-254">getsas</span><span class="sxs-lookup"><span data-stu-id="d4f7b-254">getsas</span></span>
- <span data-ttu-id="d4f7b-255">Listsas</span><span class="sxs-lookup"><span data-stu-id="d4f7b-255">listsas</span></span>
- <span data-ttu-id="d4f7b-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="d4f7b-256">deletesas</span></span>
- <span data-ttu-id="d4f7b-257">Setsas</span><span class="sxs-lookup"><span data-stu-id="d4f7b-257">setsas</span></span>
- <span data-ttu-id="d4f7b-258">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-258">recover</span></span>
- <span data-ttu-id="d4f7b-259">Sicherung</span><span class="sxs-lookup"><span data-stu-id="d4f7b-259">backup</span></span>
- <span data-ttu-id="d4f7b-260">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-260">restore</span></span>
- <span data-ttu-id="d4f7b-261">Löschen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f7b-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-262">-ResourceGroupName</span></span>
<span data-ttu-id="d4f7b-263">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4f7b-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4f7b-264">-ResourceId</span></span>
<span data-ttu-id="d4f7b-265">Ressourcen-ID des Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d4f7b-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="d4f7b-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-266">-ServicePrincipalName</span></span>
<span data-ttu-id="d4f7b-267">Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="d4f7b-268">Geben Sie die Anwendungs-ID an, die auch als Client-ID bezeichnet wird und für die Anwendung in AzureActive Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="d4f7b-269">Die Anwendung mit dem Dienstprinzipalnamen, den dieser Parameter angibt, muss im Azure-Verzeichnis registriert sein, das Ihr aktuelles Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="d4f7b-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-270">-UserPrincipalName</span></span>
<span data-ttu-id="d4f7b-271">Gibt den Benutzernamen des Benutzers an, dem Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d4f7b-272">Dieser Benutzername muss im Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="d4f7b-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d4f7b-273">-VaultName</span></span>
<span data-ttu-id="d4f7b-274">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="d4f7b-275">Dieses Cmdlet ändert die Zugriffsrichtlinie für den Schlüsseltresor, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="d4f7b-276">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4f7b-276">-Confirm</span></span>
<span data-ttu-id="d4f7b-277">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f7b-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f7b-278">-WhatIf</span></span>
<span data-ttu-id="d4f7b-279">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4f7b-280">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f7b-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f7b-281">CommonParameters</span></span>
<span data-ttu-id="d4f7b-282">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f7b-283">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4f7b-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f7b-284">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4f7b-284">INPUTS</span></span>

### <span data-ttu-id="d4f7b-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d4f7b-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="d4f7b-286">System.String</span><span class="sxs-lookup"><span data-stu-id="d4f7b-286">System.String</span></span>

## <span data-ttu-id="d4f7b-287">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4f7b-287">OUTPUTS</span></span>

### <span data-ttu-id="d4f7b-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4f7b-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d4f7b-289">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4f7b-289">NOTES</span></span>

## <span data-ttu-id="d4f7b-290">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4f7b-290">RELATED LINKS</span></span>

[<span data-ttu-id="d4f7b-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4f7b-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d4f7b-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4f7b-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

