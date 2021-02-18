---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410717"
---
# <span data-ttu-id="fd01f-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd01f-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="fd01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd01f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd01f-103">Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem Schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="fd01f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd01f-104">SYNTAX</span></span>

### <span data-ttu-id="fd01f-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd01f-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd01f-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd01f-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="fd01f-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd01f-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd01f-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="fd01f-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd01f-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd01f-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd01f-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd01f-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="fd01f-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd01f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd01f-120">DESCRIPTION</span></span>
<span data-ttu-id="fd01f-121">Das **Cmdlet "Set-AzKeyVaultAccessPolicy"** erteilt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem Schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="fd01f-122">Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen für den Schlüsseltresor besitzen, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="fd01f-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="fd01f-123">Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, wirkt sich dieser Vorgang nur auf Benutzer in dieser Sicherheitsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="fd01f-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="fd01f-124">Die folgenden Verzeichnisse müssen alle dasselbe Azure-Verzeichnis sein:</span><span class="sxs-lookup"><span data-stu-id="fd01f-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="fd01f-125">Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsseltresor befindet.</span><span class="sxs-lookup"><span data-stu-id="fd01f-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="fd01f-126">Das Azure-Verzeichnis, das den Benutzer oder die Anwendungsgruppe enthält, dem Sie Berechtigungen erteilen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="fd01f-127">Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert:</span><span class="sxs-lookup"><span data-stu-id="fd01f-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="fd01f-128">Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="fd01f-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="fd01f-129">Jede Organisation verfügt über ein eigenes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="fd01f-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="fd01f-130">Ihr Azure-Konto verfügt über mehrere Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="fd01f-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="fd01f-131">Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht zur Verwendung Ihres Schlüsseltresor autorisieren.</span><span class="sxs-lookup"><span data-stu-id="fd01f-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="fd01f-132">Die Anwendung muss sich im Standardverzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-132">The application must be in the default directory.</span></span>
<span data-ttu-id="fd01f-133">Beachten Sie: Obwohl die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, sollten Sie dies zur Leistungssteigerung tun.</span><span class="sxs-lookup"><span data-stu-id="fd01f-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="fd01f-134">Wenn Sie zum Erteilen von Zugriffsrichtlinienberechtigungen einen Dienstprinzipal verwenden, müssen Sie den Parameter `-BypassObjectIdValidation` verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="fd01f-135">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd01f-135">EXAMPLES</span></span>

### <span data-ttu-id="fd01f-136">Beispiel 1: Erteilen von Berechtigungen für einen Schlüsseltresor und Ändern der Berechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="fd01f-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="fd01f-137">Der erste Befehl erteilt einem Benutzer in Azure Active Directory Berechtigungen zum Ausführen von Vorgängen mit Schlüsseln und geheimen Daten mit einem Schlüsseltresor namens PattiFuller@contoso.com "Contoso03Vault".</span><span class="sxs-lookup"><span data-stu-id="fd01f-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="fd01f-138">Der *Parameter "PassThru"* führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd01f-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="fd01f-139">Der zweite Befehl ändert die Berechtigungen, die im ersten Befehl erteilt wurden, um jetzt zusätzlich zum Festlegen und Löschen des Befehls das Abrufen von geheimen Daten PattiFuller@contoso.com zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="fd01f-140">Die Berechtigungen für Wichtige Vorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd01f-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="fd01f-141">Der letzte Befehl ändert außerdem die vorhandenen Berechtigungen zum PattiFuller@contoso.com Entfernen aller Berechtigungen für Schlüsselvorgänge.</span><span class="sxs-lookup"><span data-stu-id="fd01f-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="fd01f-142">Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="fd01f-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="fd01f-143">Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienstprinzipal zum Lesen und Schreiben von geheimen Daten</span><span class="sxs-lookup"><span data-stu-id="fd01f-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fd01f-144">Dieser Befehl erteilt einer Anwendung Berechtigungen für einen Schlüsseltresor namens Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="fd01f-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="fd01f-145">Der *Parameter "ServicePrincipalName"* gibt die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="fd01f-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="fd01f-146">Die Anwendung muss in Azure Active Directory registriert sein.</span><span class="sxs-lookup"><span data-stu-id="fd01f-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="fd01f-147">Der Wert des Parameters *"ServicePrincipalName"* muss entweder der Dienstprinzipalname der Anwendung oder die Anwendungs-ID-GUID sein.</span><span class="sxs-lookup"><span data-stu-id="fd01f-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="fd01f-148">In diesem Beispiel wird der Dienstprinzipalname angegeben, und der Befehl erteilt der Anwendung Berechtigungen `http://payroll.contoso.com` zum Lesen und Schreiben von geheimen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd01f-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="fd01f-149">Beispiel 3: Erteilen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="fd01f-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fd01f-150">Dieser Befehl erteilt der Anwendung Berechtigungen zum Lesen und Schreiben von geheimen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd01f-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="fd01f-151">In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienstprinzipal der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd01f-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="fd01f-152">Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="fd01f-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="fd01f-153">Mit diesem Befehl werden "get", "list" und "set permissions" für den angegebenen Benutzerprinzipalnamen für den Zugriff auf geheime Daten erteilt.</span><span class="sxs-lookup"><span data-stu-id="fd01f-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="fd01f-154">Beispiel 5: Ermöglichen, dass geheime Daten vom Microsoft.Compute-Ressourcenanbieter aus einem Schlüsseltresor abgerufen werden</span><span class="sxs-lookup"><span data-stu-id="fd01f-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="fd01f-155">Dieser Befehl erteilt die Berechtigungen für geheime Daten, die vom Microsoft.Compute-Ressourcenanbieter aus dem Schlüsseltresor Contoso03Vault abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="fd01f-156">Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="fd01f-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="fd01f-157">Der erste Befehl verwendet das Get-AzADGroup Cmdlet, um alle Active Directory-Gruppen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd01f-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="fd01f-158">Aus der Ausgabe werden 3 Gruppen zurückgegeben, mit den Namen **"Gruppe1",** **"Gruppe2"** und **"Gruppe3".**</span><span class="sxs-lookup"><span data-stu-id="fd01f-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="fd01f-159">Mehrere Gruppen können denselben Namen, aber immer eine eindeutige ObjectId haben.</span><span class="sxs-lookup"><span data-stu-id="fd01f-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="fd01f-160">Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectId in der Ausgabe, um die Gruppe zu identifizieren, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fd01f-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="fd01f-161">Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzKeyVaultAccessPolicy, um Berechtigungen für Den Schlüsseltresor **"myownvault"** der Gruppe 2 zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="fd01f-162">In diesem Beispiel werden die Gruppen mit dem Namen "group2" inline in derselben Befehlszeile aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="fd01f-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="fd01f-163">Die zurückgegebene Liste enthält möglicherweise mehrere Gruppen mit dem Namen "Gruppe2".</span><span class="sxs-lookup"><span data-stu-id="fd01f-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="fd01f-164">In diesem Beispiel wird das erste Beispiel, das durch Index \[ 0 \] in der zurückgegebenen Liste angegeben ist, verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd01f-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="fd01f-165">Beispiel 7: Gewähren von Azure Information Protection Zugriff auf den vom Kunden verwalteten Mandantenschlüssel (BYOK)</span><span class="sxs-lookup"><span data-stu-id="fd01f-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="fd01f-166">Mit diesem Befehl wird Azure Information Protection autorisiert, einen vom Kunden verwalteten Schlüssel (das "Bring your own key" oder "BYOK"-Szenario) als Azure Information Protection-Mandantenschlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="fd01f-167">Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen Namen für den Schlüsseltresor an, müssen jedoch den Parameter *"ServicePrincipalName"* mit der GUID **00000012-0000-0000-c000-0000000000** angeben und die Berechtigungen im Beispiel angeben.</span><span class="sxs-lookup"><span data-stu-id="fd01f-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="fd01f-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd01f-168">PARAMETERS</span></span>

### <span data-ttu-id="fd01f-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fd01f-169">-ApplicationId</span></span>
<span data-ttu-id="fd01f-170">Für die zukünftige Verwendung.</span><span class="sxs-lookup"><span data-stu-id="fd01f-170">For future use.</span></span>

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

### <span data-ttu-id="fd01f-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="fd01f-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="fd01f-172">Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fd01f-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="fd01f-173">Verwenden Sie diesen Parameter nur, wenn Sie Zugriff auf Ihren Schlüsseltresor auf eine Objekt-ID gewähren möchten, die sich auf eine delegierte Sicherheitsgruppe von einem anderen Azure-Mandanten bezieht.</span><span class="sxs-lookup"><span data-stu-id="fd01f-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="fd01f-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd01f-174">-DefaultProfile</span></span>
<span data-ttu-id="fd01f-175">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fd01f-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd01f-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd01f-176">-EmailAddress</span></span>
<span data-ttu-id="fd01f-177">Gibt die E-Mail-Adresse des Benutzers an, dem Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fd01f-178">Diese E-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das mit dem aktuellen Abonnement verknüpft ist, und eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="fd01f-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="fd01f-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fd01f-179">-EnabledForDeployment</span></span>
<span data-ttu-id="fd01f-180">Ermöglicht es dem Microsoft.Compute-Ressourcenanbieter, geheime Daten aus diesem Schlüsseltresor abzurufen, wenn bei der Ressourcenerstellung auf diesen Schlüsseltresor verwiesen wird, z. B. beim Erstellen eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="fd01f-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="fd01f-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fd01f-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fd01f-182">Ermöglicht dem Azure-Datenträgerverschlüsselungsdienst das Erhalten von geheimen Schlüsseln und Entpackungsschlüsseln aus diesem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="fd01f-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="fd01f-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fd01f-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fd01f-184">Ermöglicht Azure Resource Manager, geheime Daten aus diesem Schlüsseltresor zu erhalten, wenn in einer Vorlagenbereitstellung auf diesen Schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fd01f-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="fd01f-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd01f-185">-InputObject</span></span>
<span data-ttu-id="fd01f-186">Key Vault Object</span><span class="sxs-lookup"><span data-stu-id="fd01f-186">Key Vault Object</span></span>

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

### <span data-ttu-id="fd01f-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fd01f-187">-ObjectId</span></span>
<span data-ttu-id="fd01f-188">Gibt die Objekt-ID des Benutzers oder Dienstprinzipal in Azure Active Directory an, für den Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="fd01f-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd01f-189">-PassThru</span></span>
<span data-ttu-id="fd01f-190">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fd01f-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd01f-191">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fd01f-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd01f-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="fd01f-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="fd01f-193">Gibt ein Array von Zertifikatberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd01f-194">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="fd01f-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd01f-195">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fd01f-195">Get</span></span>
- <span data-ttu-id="fd01f-196">Liste</span><span class="sxs-lookup"><span data-stu-id="fd01f-196">List</span></span>
- <span data-ttu-id="fd01f-197">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-197">Delete</span></span>
- <span data-ttu-id="fd01f-198">Erstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-198">Create</span></span>
- <span data-ttu-id="fd01f-199">Importieren</span><span class="sxs-lookup"><span data-stu-id="fd01f-199">Import</span></span>
- <span data-ttu-id="fd01f-200">Update</span><span class="sxs-lookup"><span data-stu-id="fd01f-200">Update</span></span>
- <span data-ttu-id="fd01f-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="fd01f-201">Managecontacts</span></span>
- <span data-ttu-id="fd01f-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="fd01f-202">Getissuers</span></span>
- <span data-ttu-id="fd01f-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="fd01f-203">Listissuers</span></span>
- <span data-ttu-id="fd01f-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="fd01f-204">Setissuers</span></span>
- <span data-ttu-id="fd01f-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="fd01f-205">Deleteissuers</span></span>
- <span data-ttu-id="fd01f-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="fd01f-206">Manageissuers</span></span>
- <span data-ttu-id="fd01f-207">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-207">Recover</span></span>
- <span data-ttu-id="fd01f-208">Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd01f-208">Backup</span></span>
- <span data-ttu-id="fd01f-209">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-209">Restore</span></span>
- <span data-ttu-id="fd01f-210">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-210">Purge</span></span>

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

### <span data-ttu-id="fd01f-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="fd01f-211">-PermissionsToKeys</span></span>
<span data-ttu-id="fd01f-212">Gibt ein Array mit Wichtigen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd01f-213">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="fd01f-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd01f-214">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="fd01f-214">Decrypt</span></span>
- <span data-ttu-id="fd01f-215">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="fd01f-215">Encrypt</span></span>
- <span data-ttu-id="fd01f-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="fd01f-216">UnwrapKey</span></span>
- <span data-ttu-id="fd01f-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="fd01f-217">WrapKey</span></span>
- <span data-ttu-id="fd01f-218">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="fd01f-218">Verify</span></span>
- <span data-ttu-id="fd01f-219">Signieren</span><span class="sxs-lookup"><span data-stu-id="fd01f-219">Sign</span></span>
- <span data-ttu-id="fd01f-220">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fd01f-220">Get</span></span>
- <span data-ttu-id="fd01f-221">Liste</span><span class="sxs-lookup"><span data-stu-id="fd01f-221">List</span></span>
- <span data-ttu-id="fd01f-222">Update</span><span class="sxs-lookup"><span data-stu-id="fd01f-222">Update</span></span>
- <span data-ttu-id="fd01f-223">Erstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-223">Create</span></span>
- <span data-ttu-id="fd01f-224">Importieren</span><span class="sxs-lookup"><span data-stu-id="fd01f-224">Import</span></span>
- <span data-ttu-id="fd01f-225">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-225">Delete</span></span>
- <span data-ttu-id="fd01f-226">Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd01f-226">Backup</span></span>
- <span data-ttu-id="fd01f-227">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-227">Restore</span></span>
- <span data-ttu-id="fd01f-228">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-228">Recover</span></span>
- <span data-ttu-id="fd01f-229">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-229">Purge</span></span>

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

### <span data-ttu-id="fd01f-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="fd01f-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="fd01f-231">Gibt ein Array mit geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd01f-232">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="fd01f-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd01f-233">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fd01f-233">Get</span></span>
- <span data-ttu-id="fd01f-234">Liste</span><span class="sxs-lookup"><span data-stu-id="fd01f-234">List</span></span>
- <span data-ttu-id="fd01f-235">Festlegen</span><span class="sxs-lookup"><span data-stu-id="fd01f-235">Set</span></span>
- <span data-ttu-id="fd01f-236">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-236">Delete</span></span>
- <span data-ttu-id="fd01f-237">Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd01f-237">Backup</span></span>
- <span data-ttu-id="fd01f-238">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-238">Restore</span></span>
- <span data-ttu-id="fd01f-239">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="fd01f-239">Recover</span></span>
- <span data-ttu-id="fd01f-240">Löschen</span><span class="sxs-lookup"><span data-stu-id="fd01f-240">Purge</span></span>

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

### <span data-ttu-id="fd01f-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="fd01f-241">-PermissionsToStorage</span></span>
<span data-ttu-id="fd01f-242">Gibt die Berechtigungen für verwaltetes Speicherkonto und SaS-Definitionsvorgang an, die einem Benutzer oder Dienstprinzipal gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="fd01f-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd01f-243">-ResourceGroupName</span></span>
<span data-ttu-id="fd01f-244">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fd01f-244">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fd01f-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd01f-245">-ResourceId</span></span>
<span data-ttu-id="fd01f-246">Ressourcen-ID des Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="fd01f-246">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="fd01f-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-247">-ServicePrincipalName</span></span>
<span data-ttu-id="fd01f-248">Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd01f-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="fd01f-249">Geben Sie die Anwendungs-ID( auch bekannt als Client-ID) an, die für die Anwendung in AzureActive Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="fd01f-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="fd01f-250">Die Anwendung mit dem von diesem Parameter angegebenen Dienstprinzipalnamen muss im Azure-Verzeichnis registriert sein, das Ihr aktuelles Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="fd01f-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="fd01f-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd01f-251">-UserPrincipalName</span></span>
<span data-ttu-id="fd01f-252">Gibt den Benutzerprinzipalnamen des Benutzers an, dem Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd01f-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fd01f-253">Dieser Benutzerprinzipalname muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fd01f-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="fd01f-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd01f-254">-VaultName</span></span>
<span data-ttu-id="fd01f-255">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="fd01f-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="fd01f-256">Dieses Cmdlet ändert die Zugriffsrichtlinie für den Schlüsseltresor, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd01f-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd01f-257">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd01f-257">-Confirm</span></span>
<span data-ttu-id="fd01f-258">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd01f-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd01f-259">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd01f-259">-WhatIf</span></span>
<span data-ttu-id="fd01f-260">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd01f-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd01f-261">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd01f-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd01f-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd01f-262">CommonParameters</span></span>
<span data-ttu-id="fd01f-263">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd01f-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd01f-264">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd01f-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd01f-265">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd01f-265">INPUTS</span></span>

### <span data-ttu-id="fd01f-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fd01f-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="fd01f-267">System.String</span><span class="sxs-lookup"><span data-stu-id="fd01f-267">System.String</span></span>

## <span data-ttu-id="fd01f-268">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd01f-268">OUTPUTS</span></span>

### <span data-ttu-id="fd01f-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd01f-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fd01f-270">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd01f-270">NOTES</span></span>

## <span data-ttu-id="fd01f-271">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd01f-271">RELATED LINKS</span></span>

[<span data-ttu-id="fd01f-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd01f-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="fd01f-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd01f-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

