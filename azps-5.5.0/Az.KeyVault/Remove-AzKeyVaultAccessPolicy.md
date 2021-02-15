---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175220"
---
# <span data-ttu-id="7db09-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7db09-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="7db09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db09-102">SYNOPSIS</span></span>
<span data-ttu-id="7db09-103">Entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7db09-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="7db09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7db09-104">SYNTAX</span></span>

### <span data-ttu-id="7db09-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7db09-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="7db09-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7db09-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7db09-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="7db09-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="7db09-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="7db09-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="7db09-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="7db09-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="7db09-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="7db09-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db09-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="7db09-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7db09-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7db09-120">DESCRIPTION</span></span>
<span data-ttu-id="7db09-121">Das **Cmdlet "Remove-AzKeyVaultAccessPolicy"** entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung oder für alle Benutzer und Anwendungen aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7db09-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="7db09-122">Selbst wenn Sie alle Berechtigungen entfernen, kann der Besitzer des Azure-Abonnements, das den Schlüsseltresor enthält, Dem Schlüsseltresor Berechtigungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7db09-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="7db09-123">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet zwar optional ist, dies aber zur Leistungssteigerung ist.</span><span class="sxs-lookup"><span data-stu-id="7db09-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="7db09-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7db09-124">EXAMPLES</span></span>

### <span data-ttu-id="7db09-125">Beispiel 1: Entfernen von Berechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="7db09-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="7db09-126">Mit diesem Befehl werden alle Berechtigungen entfernt, die ein Benutzer für den Schlüsseltresor PattiFuller@contoso.com "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="7db09-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="7db09-127">Wenn "-PassThru" angegeben wird, wird das "KeyVault"-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7db09-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="7db09-128">Beispiel 2: Entfernen von Berechtigungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="7db09-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="7db09-129">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung für den Schlüsseltresor "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="7db09-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="7db09-130">In diesem Beispiel wird die Anwendung anhand des Dienstprinzipalnamens identifiziert, der in Azure Active Directory registriert `http://payroll.contoso.com` ist.</span><span class="sxs-lookup"><span data-stu-id="7db09-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="7db09-131">Beispiel 3: Entfernen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="7db09-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="7db09-132">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung für den Schlüsseltresor "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="7db09-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="7db09-133">In diesem Beispiel wird die Anwendung durch die Objekt-ID des Dienstprinzipal identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7db09-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="7db09-134">Beispiel 4: Entfernen von Berechtigungen für den Ressourcenanbieter "Microsoft.Compute"</span><span class="sxs-lookup"><span data-stu-id="7db09-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="7db09-135">Mit diesem Befehl wird die Berechtigung für den Ressourcenanbieter "Microsoft.Compute" entfernt, um geheime Daten aus Contoso03Vault zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7db09-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="7db09-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7db09-136">PARAMETERS</span></span>

### <span data-ttu-id="7db09-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7db09-137">-ApplicationId</span></span>
<span data-ttu-id="7db09-138">Gibt die ID der Anwendung an, deren Berechtigungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7db09-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="7db09-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db09-139">-DefaultProfile</span></span>
<span data-ttu-id="7db09-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7db09-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7db09-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7db09-141">-EmailAddress</span></span>
<span data-ttu-id="7db09-142">Gibt die E-Mail-Adresse des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="7db09-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db09-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7db09-143">-EnabledForDeployment</span></span>
<span data-ttu-id="7db09-144">Wenn angegeben, wird das Abrufen von geheimen Daten aus diesem Schlüsseltresor durch den Microsoft.Compute-Ressourcenanbieter deaktiviert, wenn bei der Ressourcenerstellung darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7db09-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="7db09-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7db09-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7db09-146">Wenn angegeben, deaktiviert die Azure-Datenträgerverschlüsselung das Abrufen von geheimen Daten aus diesem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7db09-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="7db09-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7db09-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7db09-148">Wenn angegeben, wird das Abrufen von geheimen Daten aus diesem Schlüsseltresor durch Azure Resource Manager deaktiviert, wenn in Vorlagen darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7db09-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="7db09-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7db09-149">-InputObject</span></span>
<span data-ttu-id="7db09-150">Key Vault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7db09-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db09-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7db09-151">-ObjectId</span></span>
<span data-ttu-id="7db09-152">Gibt die Objekt-ID des Benutzers oder Dienstprinzipal in Azure Active Directory an, für den Berechtigungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7db09-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="7db09-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7db09-153">-PassThru</span></span>
<span data-ttu-id="7db09-154">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7db09-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7db09-155">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7db09-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7db09-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db09-156">-ResourceGroupName</span></span>
<span data-ttu-id="7db09-157">Gibt den Namen der Ressourcengruppe an, die dem Schlüsseltresor zugeordnet ist, dessen Zugriffsrichtlinie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7db09-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="7db09-158">Wenn diese Angabe nicht angegeben ist, sucht dieses Cmdlet nach dem Schlüsseltresor im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7db09-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db09-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7db09-159">-ResourceId</span></span>
<span data-ttu-id="7db09-160">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7db09-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db09-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-161">-ServicePrincipalName</span></span>
<span data-ttu-id="7db09-162">Gibt den Dienstprinzipalnamen der Anwendung an, deren Berechtigungen Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="7db09-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="7db09-163">Geben Sie die Anwendungs-ID( auch bekannt als Client-ID) an, die für die Anwendung in Azure Active Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="7db09-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="7db09-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7db09-164">-UserPrincipalName</span></span>
<span data-ttu-id="7db09-165">Gibt den Benutzerprinzipalnamen des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="7db09-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="7db09-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7db09-166">-VaultName</span></span>
<span data-ttu-id="7db09-167">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="7db09-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="7db09-168">Mit diesem Cmdlet werden Berechtigungen für den Schlüsseltresor entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7db09-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db09-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7db09-169">-Confirm</span></span>
<span data-ttu-id="7db09-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7db09-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db09-171">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7db09-171">-WhatIf</span></span>
<span data-ttu-id="7db09-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7db09-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db09-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7db09-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db09-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db09-174">CommonParameters</span></span>
<span data-ttu-id="7db09-175">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db09-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db09-176">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7db09-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db09-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7db09-177">INPUTS</span></span>

### <span data-ttu-id="7db09-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7db09-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7db09-179">System.String</span><span class="sxs-lookup"><span data-stu-id="7db09-179">System.String</span></span>

## <span data-ttu-id="7db09-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7db09-180">OUTPUTS</span></span>

### <span data-ttu-id="7db09-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7db09-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="7db09-182">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7db09-182">NOTES</span></span>

## <span data-ttu-id="7db09-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7db09-183">RELATED LINKS</span></span>

[<span data-ttu-id="7db09-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7db09-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

