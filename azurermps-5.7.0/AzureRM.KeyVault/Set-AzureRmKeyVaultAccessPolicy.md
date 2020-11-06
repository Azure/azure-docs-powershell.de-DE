---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481162"
---
# <span data-ttu-id="c88e9-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c88e9-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="c88e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c88e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c88e9-103">Gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um Vorgänge mit einem schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c88e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c88e9-104">SYNTAX</span></span>

### <span data-ttu-id="c88e9-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c88e9-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88e9-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="c88e9-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88e9-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c88e9-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88e9-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c88e9-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e9-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="c88e9-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88e9-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="c88e9-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88e9-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c88e9-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e9-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c88e9-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e9-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c88e9-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e9-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="c88e9-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c88e9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c88e9-115">DESCRIPTION</span></span>
<span data-ttu-id="c88e9-116">Das Cmdlet " **Satz-AzureRmKeyVaultAccessPolicy** " gewährt oder ändert vorhandene Berechtigungen für einen Benutzer, eine Anwendung oder eine Sicherheitsgruppe, um die angegebenen Vorgänge mit einem schlüsseltresor durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="c88e9-117">Die Berechtigungen, die andere Benutzer, Anwendungen oder Sicherheitsgruppen im schlüsseltresor haben, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c88e9-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="c88e9-118">Wenn Sie Berechtigungen für eine Sicherheitsgruppe festlegen, betrifft dieser Vorgang nur Benutzer in dieser Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c88e9-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="c88e9-119">Die folgenden Verzeichnisse müssen alle das gleiche Azure-Verzeichnis aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c88e9-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="c88e9-120">Das Standardverzeichnis des Azure-Abonnements, in dem sich der Schlüsselspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="c88e9-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="c88e9-121">Das Azure-Verzeichnis, in dem sich der Benutzer oder die Anwendungsgruppe befindet, dem Sie Berechtigungen erteilen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="c88e9-122">Beispiele für Szenarien, in denen diese Bedingungen nicht erfüllt sind und dieses Cmdlet nicht funktioniert, sind:</span><span class="sxs-lookup"><span data-stu-id="c88e9-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="c88e9-123">Autorisieren eines Benutzers aus einer anderen Organisation zum Verwalten Ihres Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="c88e9-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="c88e9-124">Jede Organisation verfügt über ein eigenes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c88e9-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="c88e9-125">Ihr Azure-Konto verfügt über mehrere Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="c88e9-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="c88e9-126">Wenn Sie eine Anwendung in einem anderen Verzeichnis als dem Standardverzeichnis registrieren, können Sie diese Anwendung nicht autorisieren, um Ihren schlüsseltresor zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c88e9-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="c88e9-127">Die Anwendung muss sich im Standardverzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="c88e9-127">The application must be in the default directory.</span></span>

<span data-ttu-id="c88e9-128">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="c88e9-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c88e9-129">EXAMPLES</span></span>

### <span data-ttu-id="c88e9-130">Beispiel 1: Erteilen von Berechtigungen für einen Benutzer für einen schlüsseltresor und Ändern der Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="c88e9-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="c88e9-131">Der erste Befehl gewährt einem Benutzer in Azure Active Directory Berechtigungen, PattiFuller@contoso.com um Vorgänge für Schlüssel und Geheimnisse mit einem schlüsseltresor mit dem Namen Contoso03Vault durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="c88e9-132">Mit dem zweiten Befehl werden die Berechtigungen geändert, die PattiFuller@contoso.com im ersten Befehl gewährt wurden, sodass Sie nun zusätzlich zu den Einstellungen und Löschungen auch Geheimnisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="c88e9-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="c88e9-133">Die Berechtigungen für Schlüsselvorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="c88e9-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="c88e9-134">Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c88e9-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="c88e9-135">Der endgültige Befehl ändert weiterhin die vorhandenen Berechtigungen für PattiFuller@contoso.com , um alle Berechtigungen für wichtige Vorgänge zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="c88e9-136">Die Berechtigungen für geheime Vorgänge bleiben nach diesem Befehl unverändert.</span><span class="sxs-lookup"><span data-stu-id="c88e9-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="c88e9-137">Der *passthru* -Parameter führt dazu, dass das aktualisierte Objekt vom Cmdlet zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c88e9-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="c88e9-138">Beispiel 2: Erteilen von Berechtigungen für einen Anwendungsdienst Prinzipal zum Lesen und Schreiben von Geheimnissen</span><span class="sxs-lookup"><span data-stu-id="c88e9-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="c88e9-139">Dieser Befehl gewährt Berechtigungen für eine Anwendung für einen schlüsseltresor mit dem Namen Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="c88e9-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="c88e9-140">Der *servicePrincipalName* -Parameter gibt die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c88e9-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="c88e9-141">Die Anwendung muss in Ihrem Azure Active Directory registriert sein.</span><span class="sxs-lookup"><span data-stu-id="c88e9-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="c88e9-142">Der Wert des *servicePrincipalName* -Parameters muss entweder der Dienstprinzipalname der Anwendung oder die GUID der Anwendungs-ID sein.</span><span class="sxs-lookup"><span data-stu-id="c88e9-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="c88e9-143">In diesem Beispiel wird der Dienstprinzipalname angegeben http://payroll.contoso.com , und der Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="c88e9-144">Beispiel 3: Erteilen von Berechtigungen für eine Anwendung unter Verwendung der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="c88e9-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="c88e9-145">Dieser Befehl gewährt den Anwendungsberechtigungen das Lesen und Schreiben von Geheimnissen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="c88e9-146">In diesem Beispiel wird die Anwendung mit der Objekt-ID des Dienst Prinzipals der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="c88e9-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="c88e9-147">Beispiel 4: Erteilen von Berechtigungen für einen Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="c88e9-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="c88e9-148">Dieser Befehl gewährt Get-, List-und festgelegte Berechtigungen für den angegebenen Benutzerprinzipalnamen für den Zugriff auf Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="c88e9-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="c88e9-149">Beispiel 5: Aktivieren von Geheimnissen aus einem schlüsseltresor durch den Microsoft. Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="c88e9-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="c88e9-150">Dieser Befehl gewährt die Berechtigungen für Geheimnisse, die vom Contoso03Vault-schlüsseltresor vom Microsoft. Compute-Ressourcenanbieter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c88e9-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="c88e9-151">Beispiel 6: Erteilen von Berechtigungen für eine Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="c88e9-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="c88e9-152">Der erste Befehl verwendet das Get-AzureRmADGroup-Cmdlet, um alle Active Directory-Gruppen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="c88e9-153">In der Ausgabe werden drei zurückgegebene Gruppen mit dem Namen " **group1** ", " **group2** " und " **Gruppe3** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c88e9-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="c88e9-154">Mehrere Gruppen können denselben Namen haben, aber immer eine eindeutige ObjectID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="c88e9-155">Wenn mehr als eine Gruppe mit demselben Namen zurückgegeben wird, verwenden Sie die ObjectID in der Ausgabe, um die gewünschte Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c88e9-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="c88e9-156">Anschließend verwenden Sie die Ausgabe dieses Befehls mit Set-AzureRmKeyVaultAccessPolicy, um group2-Berechtigungen für Ihren schlüsseltresor mit dem Namen **myownvault** zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="c88e9-157">In diesem Beispiel werden die Gruppen mit dem Namen "group2" Inline in der gleichen Befehlszeile aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c88e9-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="c88e9-158">In der zurückgegebenen Liste können mehrere Gruppen mit dem Namen "group2" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c88e9-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="c88e9-159">In diesem Beispiel wird das erste Element mit dem Index \[ 0 \] in der zurückgegebenen Liste markiert.</span><span class="sxs-lookup"><span data-stu-id="c88e9-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="c88e9-160">Beispiel 7: Gewähren des Azure Information Protection-Zugriffs auf den vom Kunden verwalteten Mandanten Schlüssel (BYOK)</span><span class="sxs-lookup"><span data-stu-id="c88e9-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="c88e9-161">Mit diesem Befehl wird der Azure-Informationsschutz autorisiert, einen vom Kunden verwalteten Schlüssel (das Szenario "eigene Schlüssel" oder "BYOK") als Azure Information Protection-Mandanten Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c88e9-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="c88e9-162">Wenn Sie diesen Befehl ausführen, geben Sie Ihren eigenen schlüsseltresor Namen an, aber Sie müssen den *servicePrincipalName* -Parameter mit der GUID **00000012-0000-0000-C000-000000000000** angeben und die Berechtigungen im Beispiel angeben.</span><span class="sxs-lookup"><span data-stu-id="c88e9-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="c88e9-163">Parameter</span><span class="sxs-lookup"><span data-stu-id="c88e9-163">PARAMETERS</span></span>

### <span data-ttu-id="c88e9-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c88e9-164">-ApplicationId</span></span>
<span data-ttu-id="c88e9-165">Für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c88e9-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="c88e9-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="c88e9-167">Ermöglicht es Ihnen, eine Objekt-ID anzugeben, ohne zu überprüfen, ob das Objekt in Azure Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c88e9-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="c88e9-168">Verwenden Sie diesen Parameter nur, wenn Sie einer Objekt-ID, die sich auf eine delegierte Sicherheitsgruppe aus einem anderen Azure-Mandanten bezieht, Zugriff auf Ihren schlüsseltresor gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="c88e9-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88e9-169">-DefaultProfile</span></span>
<span data-ttu-id="c88e9-170">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c88e9-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-171">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="c88e9-171">-EmailAddress</span></span>
<span data-ttu-id="c88e9-172">Gibt die e-Mail-Adresse des Benutzers an, dem Sie Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="c88e9-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="c88e9-173">Diese e-Mail-Adresse muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist, und eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c88e9-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="c88e9-174">-EnabledForDeployment</span></span>
<span data-ttu-id="c88e9-175">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c88e9-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c88e9-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="c88e9-177">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="c88e9-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="c88e9-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="c88e9-179">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c88e9-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-180">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c88e9-180">-InputObject</span></span>
<span data-ttu-id="c88e9-181">Vault-Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="c88e9-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-182">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c88e9-182">-ObjectId</span></span>
<span data-ttu-id="c88e9-183">Gibt die Objekt-ID des Benutzers oder Dienst Prinzipals in Azure Active Directory an, für den Berechtigungen erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c88e9-184">-PassThru</span></span>
<span data-ttu-id="c88e9-185">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c88e9-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="c88e9-186">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c88e9-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="c88e9-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="c88e9-188">Gibt ein Array von Zertifikat Berechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="c88e9-189">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="c88e9-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="c88e9-190">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c88e9-190">Get</span></span>
- <span data-ttu-id="c88e9-191">Liste</span><span class="sxs-lookup"><span data-stu-id="c88e9-191">List</span></span>
- <span data-ttu-id="c88e9-192">Löschen</span><span class="sxs-lookup"><span data-stu-id="c88e9-192">Delete</span></span>
- <span data-ttu-id="c88e9-193">Erstellen</span><span class="sxs-lookup"><span data-stu-id="c88e9-193">Create</span></span>
- <span data-ttu-id="c88e9-194">Importieren</span><span class="sxs-lookup"><span data-stu-id="c88e9-194">Import</span></span>
- <span data-ttu-id="c88e9-195">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c88e9-195">Update</span></span>
- <span data-ttu-id="c88e9-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="c88e9-196">Managecontacts</span></span>
- <span data-ttu-id="c88e9-197">Getissuer</span><span class="sxs-lookup"><span data-stu-id="c88e9-197">Getissuers</span></span>
- <span data-ttu-id="c88e9-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="c88e9-198">Listissuers</span></span>
- <span data-ttu-id="c88e9-199">Setissuer</span><span class="sxs-lookup"><span data-stu-id="c88e9-199">Setissuers</span></span>
- <span data-ttu-id="c88e9-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="c88e9-200">Deleteissuers</span></span>
- <span data-ttu-id="c88e9-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="c88e9-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="c88e9-202">-PermissionsToKeys</span></span>
<span data-ttu-id="c88e9-203">Gibt ein Array von Schlüssel Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="c88e9-204">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="c88e9-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="c88e9-205">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="c88e9-205">Decrypt</span></span>
- <span data-ttu-id="c88e9-206">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="c88e9-206">Encrypt</span></span>
- <span data-ttu-id="c88e9-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="c88e9-207">UnwrapKey</span></span>
- <span data-ttu-id="c88e9-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="c88e9-208">WrapKey</span></span>
- <span data-ttu-id="c88e9-209">Prüfen</span><span class="sxs-lookup"><span data-stu-id="c88e9-209">Verify</span></span>
- <span data-ttu-id="c88e9-210">Melden sich</span><span class="sxs-lookup"><span data-stu-id="c88e9-210">Sign</span></span>
- <span data-ttu-id="c88e9-211">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c88e9-211">Get</span></span>
- <span data-ttu-id="c88e9-212">Liste</span><span class="sxs-lookup"><span data-stu-id="c88e9-212">List</span></span>
- <span data-ttu-id="c88e9-213">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c88e9-213">Update</span></span>
- <span data-ttu-id="c88e9-214">Erstellen</span><span class="sxs-lookup"><span data-stu-id="c88e9-214">Create</span></span>
- <span data-ttu-id="c88e9-215">Importieren</span><span class="sxs-lookup"><span data-stu-id="c88e9-215">Import</span></span>
- <span data-ttu-id="c88e9-216">Löschen</span><span class="sxs-lookup"><span data-stu-id="c88e9-216">Delete</span></span>
- <span data-ttu-id="c88e9-217">Backup</span><span class="sxs-lookup"><span data-stu-id="c88e9-217">Backup</span></span>
- <span data-ttu-id="c88e9-218">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="c88e9-218">Restore</span></span>
- <span data-ttu-id="c88e9-219">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="c88e9-219">Recover</span></span>
- <span data-ttu-id="c88e9-220">Purge</span><span class="sxs-lookup"><span data-stu-id="c88e9-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="c88e9-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="c88e9-222">Gibt ein Array von geheimen Vorgangsberechtigungen an, die einem Benutzer oder Dienstprinzipal gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="c88e9-223">Die zulässigen Werte für diesen Parameter:</span><span class="sxs-lookup"><span data-stu-id="c88e9-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="c88e9-224">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c88e9-224">Get</span></span>
- <span data-ttu-id="c88e9-225">Liste</span><span class="sxs-lookup"><span data-stu-id="c88e9-225">List</span></span>
- <span data-ttu-id="c88e9-226">Einrichten</span><span class="sxs-lookup"><span data-stu-id="c88e9-226">Set</span></span>
- <span data-ttu-id="c88e9-227">Löschen</span><span class="sxs-lookup"><span data-stu-id="c88e9-227">Delete</span></span>
- <span data-ttu-id="c88e9-228">Backup</span><span class="sxs-lookup"><span data-stu-id="c88e9-228">Backup</span></span>
- <span data-ttu-id="c88e9-229">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="c88e9-229">Restore</span></span>
- <span data-ttu-id="c88e9-230">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="c88e9-230">Recover</span></span>
- <span data-ttu-id="c88e9-231">Purge</span><span class="sxs-lookup"><span data-stu-id="c88e9-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="c88e9-232">-PermissionsToStorage</span></span>
<span data-ttu-id="c88e9-233">Gibt die Berechtigungen des verwalteten speicherkontos und des SAS-Definitionsvorgangs an, die einem Benutzer oder Dienstprinzipal gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="c88e9-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88e9-234">-ResourceGroupName</span></span>
<span data-ttu-id="c88e9-235">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c88e9-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c88e9-236">-ServicePrincipalName</span></span>
<span data-ttu-id="c88e9-237">Gibt den Dienstprinzipalnamen der Anwendung an, der Berechtigungen erteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="c88e9-238">Geben Sie die Anwendungs-ID (auch Client-ID genannt) an, die für die Anwendung im AzureActive-Verzeichnis registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c88e9-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="c88e9-239">Die Anwendung mit dem Dienstprinzipalnamen, den dieser Parameter angibt, muss im Azure-Verzeichnis registriert sein, in dem sich das aktuelle Abonnement befindet.</span><span class="sxs-lookup"><span data-stu-id="c88e9-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c88e9-240">-UserPrincipalName</span></span>
<span data-ttu-id="c88e9-241">Gibt den Benutzerprinzipalnamen des Benutzers an, dem Sie Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="c88e9-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="c88e9-242">Dieser Benutzerprinzipalname muss in dem Verzeichnis vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c88e9-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-243">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c88e9-243">-VaultName</span></span>
<span data-ttu-id="c88e9-244">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="c88e9-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="c88e9-245">Mit diesem Cmdlet wird die Zugriffsrichtlinie für den schlüsseltresor geändert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c88e9-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-246">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c88e9-246">-Confirm</span></span>
<span data-ttu-id="c88e9-247">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c88e9-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88e9-248">-WhatIf</span></span>
<span data-ttu-id="c88e9-249">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c88e9-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c88e9-250">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c88e9-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e9-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88e9-251">CommonParameters</span></span>
<span data-ttu-id="c88e9-252">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88e9-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88e9-253">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88e9-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88e9-254">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c88e9-254">INPUTS</span></span>

### <span data-ttu-id="c88e9-255">String, Guid, String [], Switch</span><span class="sxs-lookup"><span data-stu-id="c88e9-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="c88e9-256">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c88e9-256">OUTPUTS</span></span>

### <span data-ttu-id="c88e9-257">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c88e9-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c88e9-258">Notizen</span><span class="sxs-lookup"><span data-stu-id="c88e9-258">NOTES</span></span>

## <span data-ttu-id="c88e9-259">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c88e9-259">RELATED LINKS</span></span>

[<span data-ttu-id="c88e9-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c88e9-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="c88e9-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c88e9-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

