---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167252"
---
# <span data-ttu-id="d886a-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d886a-101">New-AzKeyVault</span></span>

## <span data-ttu-id="d886a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d886a-102">SYNOPSIS</span></span>
<span data-ttu-id="d886a-103">Erstellt einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d886a-103">Creates a key vault.</span></span>

## <span data-ttu-id="d886a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d886a-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d886a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d886a-105">DESCRIPTION</span></span>
<span data-ttu-id="d886a-106">Das **Cmdlet "New-AzKeyVault"** erstellt einen Schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d886a-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="d886a-107">Dieses Cmdlet erteilt dem derzeit angemeldeten Benutzer außerdem berechtigungen zum Hinzufügen, Entfernen oder Auflisten von Schlüsseln und geheimen Daten im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d886a-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="d886a-108">Hinweis: Wenn die Fehlermeldung angezeigt wird, ist das Abonnement nicht für die Verwendung des **Namespaces 'Microsoft.KeyVault'** registriert, wenn Sie versuchen, Ihren neuen Schlüsseltresor zu erstellen, führen Sie **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** aus, und führen Sie dann den Befehl **"New-AzKeyVault"** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d886a-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="d886a-109">Weitere Informationen finden Sie unter "Register-AzResourceProvider".</span><span class="sxs-lookup"><span data-stu-id="d886a-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="d886a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d886a-110">EXAMPLES</span></span>

### <span data-ttu-id="d886a-111">Beispiel 1: Erstellen eines Standardschlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d886a-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
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
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d886a-112">Mit diesem Befehl wird ein Schlüsseltresor namens "Contoso03Vault" in der Region Azure im Osten der USA erstellt.</span><span class="sxs-lookup"><span data-stu-id="d886a-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="d886a-113">Mit dem Befehl wird der Ressourcengruppe mit dem Namen "Gruppe14" der Schlüsseltresor hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d886a-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="d886a-114">Da der Befehl keinen Wert für den *SKU-Parameter* anfordert, erstellt er einen Standardschlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="d886a-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="d886a-115">Beispiel 2: Erstellen eines Premium-Key-Tresors</span><span class="sxs-lookup"><span data-stu-id="d886a-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d886a-116">Mit diesem Befehl wird wie im vorherigen Beispiel ein Schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="d886a-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="d886a-117">Es gibt jedoch den Wert "Premium" für den *SKU-Parameter* an, um einen Premium-Schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d886a-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="d886a-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d886a-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="d886a-119">Erstellen eines Schlüsseltresor und Angeben von Netzwerkregeln, um den Zugriff auf die angegebene IP-Adresse aus dem virtuellen Netzwerk zu ermöglichen, das von $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="d886a-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="d886a-120">Weitere `New-AzKeyVaultNetworkRuleSetObject` Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="d886a-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="d886a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d886a-121">PARAMETERS</span></span>

### <span data-ttu-id="d886a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d886a-122">-DefaultProfile</span></span>
<span data-ttu-id="d886a-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d886a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d886a-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d886a-124">-EnabledForDeployment</span></span>
<span data-ttu-id="d886a-125">Ermöglicht es dem Microsoft.Compute-Ressourcenanbieter, geheime Daten aus diesem Schlüsseltresor abzurufen, wenn bei der Ressourcenerstellung auf diesen Schlüsseltresor verwiesen wird, z. B. beim Erstellen eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d886a-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d886a-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d886a-127">Ermöglicht dem Azure-Datenträgerverschlüsselungsdienst, geheime Daten und Schlüssel zum Entpacken aus diesem Schlüsseltresor zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d886a-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d886a-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d886a-129">Ermöglicht Azure Resource Manager, geheime Daten aus diesem Schlüsseltresor zu erhalten, wenn in einer Vorlagenbereitstellung auf diesen Schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d886a-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="d886a-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="d886a-131">Falls angegeben, ist der Schutz vor sofortiger Löschung für diesen Tresor aktiviert. erfordert, dass das weiche Löschen ebenfalls aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d886a-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="d886a-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="d886a-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="d886a-133">Sofern angegeben, können Datenaktionen über rollenbasierte Zugriffssteuerung (Role Based Access Control, RBAC) autorisiert werden. Dann werden die in den Tresoreigenschaften angegebenen Zugriffsrichtlinien ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d886a-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="d886a-134">Beachten Sie, dass Verwaltungsaktionen immer mit RBAC autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="d886a-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="d886a-135">-Location</span><span class="sxs-lookup"><span data-stu-id="d886a-135">-Location</span></span>
<span data-ttu-id="d886a-136">Gibt die Azure-Region an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d886a-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="d886a-137">Verwenden Sie den Befehl ["Get-AzLocation",](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) um Ihre Auswahlmöglichkeiten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="d886a-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d886a-138">-Name</span></span>
<span data-ttu-id="d886a-139">Gibt einen Namen für den zu erstellenden Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="d886a-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="d886a-140">Bei dem Namen kann es sich um eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen geben.</span><span class="sxs-lookup"><span data-stu-id="d886a-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="d886a-141">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="d886a-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="d886a-142">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d886a-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d886a-143">-NetworkRuleSet</span></span>
<span data-ttu-id="d886a-144">Gibt den Netzwerkregelsatz des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="d886a-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="d886a-145">Er regelt die Barrierefreiheit des Schlüsseltresor von bestimmten Netzwerkstandorten aus.</span><span class="sxs-lookup"><span data-stu-id="d886a-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="d886a-146">Erstellt `New-AzKeyVaultNetworkRuleSetObject` von.</span><span class="sxs-lookup"><span data-stu-id="d886a-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d886a-147">-ResourceGroupName</span></span>
<span data-ttu-id="d886a-148">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d886a-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="d886a-149">-Sku</span></span>
<span data-ttu-id="d886a-150">Gibt die SKU der Schlüsseltresorinstanz an.</span><span class="sxs-lookup"><span data-stu-id="d886a-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="d886a-151">Informationen dazu, welche Features für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault Pricing-Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="d886a-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d886a-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="d886a-153">Gibt an, wie lange gelöschte Ressourcen aufbewahrt werden und wie lange ein Tresor oder objekt im gelöschten Zustand gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="d886a-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="d886a-154">Der Standardwert ist 90 Tage.</span><span class="sxs-lookup"><span data-stu-id="d886a-154">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="d886a-155">-Tag</span></span>
<span data-ttu-id="d886a-156">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d886a-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d886a-157">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d886a-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d886a-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d886a-158">-Confirm</span></span>
<span data-ttu-id="d886a-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d886a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d886a-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d886a-160">-WhatIf</span></span>
<span data-ttu-id="d886a-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d886a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d886a-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d886a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d886a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d886a-163">CommonParameters</span></span>
<span data-ttu-id="d886a-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d886a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d886a-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d886a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d886a-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d886a-166">INPUTS</span></span>

### <span data-ttu-id="d886a-167">System.String</span><span class="sxs-lookup"><span data-stu-id="d886a-167">System.String</span></span>

### <span data-ttu-id="d886a-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d886a-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d886a-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="d886a-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="d886a-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d886a-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d886a-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d886a-171">OUTPUTS</span></span>

### <span data-ttu-id="d886a-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d886a-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d886a-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d886a-173">NOTES</span></span>

## <span data-ttu-id="d886a-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d886a-174">RELATED LINKS</span></span>

[<span data-ttu-id="d886a-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d886a-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d886a-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d886a-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
