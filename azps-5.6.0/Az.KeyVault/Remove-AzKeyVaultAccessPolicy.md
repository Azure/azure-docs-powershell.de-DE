---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 0062b345a78063028ffe0c0c983ab73af66cf674
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918923"
---
# <span data-ttu-id="bf57f-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf57f-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="bf57f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf57f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf57f-103">Entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="bf57f-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="bf57f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf57f-104">SYNTAX</span></span>

### <span data-ttu-id="bf57f-105">ByUserPrincipalName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf57f-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="bf57f-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf57f-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf57f-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="bf57f-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="bf57f-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="bf57f-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="bf57f-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="bf57f-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="bf57f-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="bf57f-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf57f-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="bf57f-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf57f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf57f-120">DESCRIPTION</span></span>
<span data-ttu-id="bf57f-121">Das **Cmdlet Remove-AzKeyVaultAccessPolicy** entfernt alle Berechtigungen für einen Benutzer oder eine Anwendung oder für alle Benutzer und Anwendungen aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="bf57f-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="bf57f-122">Selbst wenn Sie alle Berechtigungen entfernen, kann der Besitzer des Azure-Abonnements, das den Schlüsseltresor enthält, Dem Schlüsseltresor Berechtigungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf57f-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="bf57f-123">Beachten Sie, dass die Angabe der Ressourcengruppe für dieses Cmdlet zwar optional ist, Sie dies aber tun sollten, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="bf57f-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="bf57f-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf57f-124">EXAMPLES</span></span>

### <span data-ttu-id="bf57f-125">Beispiel 1: Entfernen von Berechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf57f-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="bf57f-126">Mit diesem Befehl werden alle Berechtigungen entfernt, die ein Benutzer für den Schlüsseltresor PattiFuller@contoso.com "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="bf57f-127">Wenn -PassThru angegeben ist, wird das KeyVault-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf57f-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="bf57f-128">Beispiel 2: Entfernen von Berechtigungen für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="bf57f-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="bf57f-129">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung für den Schlüsseltresor "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="bf57f-130">In diesem Beispiel wird die Anwendung anhand des Dienstprinzipalnamens identifiziert, der in Azure Active Directory registriert `http://payroll.contoso.com` ist.</span><span class="sxs-lookup"><span data-stu-id="bf57f-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="bf57f-131">Beispiel 3: Entfernen von Berechtigungen für eine Anwendung mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="bf57f-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="bf57f-132">Mit diesem Befehl werden alle Berechtigungen entfernt, die eine Anwendung für den Schlüsseltresor "Contoso03Vault" besitzt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="bf57f-133">In diesem Beispiel wird die Anwendung durch die Objekt-ID des Dienstprinzipal identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bf57f-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="bf57f-134">Beispiel 4: Entfernen von Berechtigungen für den Microsoft.Compute-Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="bf57f-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="bf57f-135">Mit diesem Befehl werden die Berechtigungen für den Microsoft.Compute-Ressourcenanbieter entfernt, um Geheiminformationen aus Contoso03Vault zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf57f-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="bf57f-136">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf57f-136">PARAMETERS</span></span>

### <span data-ttu-id="bf57f-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf57f-137">-ApplicationId</span></span>
<span data-ttu-id="bf57f-138">Gibt die ID der Anwendung an, deren Berechtigungen entfernt werden sollen</span><span class="sxs-lookup"><span data-stu-id="bf57f-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="bf57f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf57f-139">-DefaultProfile</span></span>
<span data-ttu-id="bf57f-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bf57f-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf57f-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="bf57f-141">-EmailAddress</span></span>
<span data-ttu-id="bf57f-142">Gibt die E-Mail-Adresse des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="bf57f-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="bf57f-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="bf57f-143">-EnabledForDeployment</span></span>
<span data-ttu-id="bf57f-144">Wenn angegeben, deaktiviert das Abrufen von Geheiminformationen aus diesem Schlüsseltresor durch den Microsoft.Compute-Ressourcenanbieter, wenn in der Ressourcenerstellung auf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bf57f-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="bf57f-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bf57f-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="bf57f-146">Wenn angegeben, deaktiviert das Abrufen von Geheimnissen aus diesem Schlüsseltresor durch azure disk encryption.</span><span class="sxs-lookup"><span data-stu-id="bf57f-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="bf57f-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="bf57f-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="bf57f-148">Wenn angegeben, wird das Abrufen von Geheiminformationen aus diesem Schlüsseltresor durch Azure Resource Manager deaktiviert, wenn in Vorlagen auf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bf57f-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="bf57f-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf57f-149">-InputObject</span></span>
<span data-ttu-id="bf57f-150">Key Vault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-150">Key Vault object.</span></span>

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

### <span data-ttu-id="bf57f-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bf57f-151">-ObjectId</span></span>
<span data-ttu-id="bf57f-152">Gibt die Objekt-ID des Benutzers oder Dienstprinzipals in Azure Active Directory an, für die Berechtigungen entfernt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bf57f-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="bf57f-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf57f-153">-PassThru</span></span>
<span data-ttu-id="bf57f-154">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf57f-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf57f-155">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bf57f-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf57f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf57f-156">-ResourceGroupName</span></span>
<span data-ttu-id="bf57f-157">Gibt den Namen der Ressourcengruppe an, die dem Schlüsseltresor zugeordnet ist, dessen Zugriffsrichtlinie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bf57f-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="bf57f-158">Wenn nicht angegeben, sucht dieses Cmdlet nach dem Schlüsseltresor im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf57f-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="bf57f-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf57f-159">-ResourceId</span></span>
<span data-ttu-id="bf57f-160">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bf57f-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="bf57f-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-161">-ServicePrincipalName</span></span>
<span data-ttu-id="bf57f-162">Gibt den Dienstprinzipalnamen der Anwendung an, deren Berechtigungen Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="bf57f-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="bf57f-163">Geben Sie die Anwendungs-ID an, die auch als Client-ID bezeichnet wird und für die Anwendung in Azure Active Directory registriert ist.</span><span class="sxs-lookup"><span data-stu-id="bf57f-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="bf57f-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf57f-164">-UserPrincipalName</span></span>
<span data-ttu-id="bf57f-165">Gibt den Benutzernamen des Benutzers an, dessen Zugriff Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="bf57f-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="bf57f-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bf57f-166">-VaultName</span></span>
<span data-ttu-id="bf57f-167">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="bf57f-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="bf57f-168">Dieses Cmdlet entfernt Berechtigungen für den Schlüsseltresor, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf57f-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf57f-169">-Confirm</span></span>
<span data-ttu-id="bf57f-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf57f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf57f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf57f-171">-WhatIf</span></span>
<span data-ttu-id="bf57f-172">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf57f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf57f-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf57f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf57f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf57f-174">CommonParameters</span></span>
<span data-ttu-id="bf57f-175">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf57f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf57f-176">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf57f-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf57f-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf57f-177">INPUTS</span></span>

### <span data-ttu-id="bf57f-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf57f-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bf57f-179">System.String</span><span class="sxs-lookup"><span data-stu-id="bf57f-179">System.String</span></span>

## <span data-ttu-id="bf57f-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf57f-180">OUTPUTS</span></span>

### <span data-ttu-id="bf57f-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf57f-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="bf57f-182">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf57f-182">NOTES</span></span>

## <span data-ttu-id="bf57f-183">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf57f-183">RELATED LINKS</span></span>

[<span data-ttu-id="bf57f-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf57f-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

