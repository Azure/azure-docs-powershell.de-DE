---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180420"
---
# <span data-ttu-id="7b7ff-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7b7ff-101">New-AzKeyVault</span></span>

## <span data-ttu-id="7b7ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7ff-103">Erstellt einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-103">Creates a key vault.</span></span>

## <span data-ttu-id="7b7ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b7ff-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b7ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7ff-106">Das Cmdlet **New-AzKeyVault** erstellt einen schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="7b7ff-107">Mit diesem Cmdlet werden dem aktuell angemeldeten Benutzer auch Berechtigungen zum Hinzufügen, entfernen oder Auflisten von Schlüsseln und Geheimnissen im schlüsseltresor gewährt.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="7b7ff-108">Hinweis: Wenn der Fehler angezeigt **wird, dass das Abonnement nicht registriert ist, um den Namespace "Microsoft. keyvault" zu verwenden** , wenn Sie versuchen, ihren neuen schlüsseltresor zu erstellen, führen Sie **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** aus, und führen Sie dann den Befehl **neu-AzKeyVault** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="7b7ff-109">Weitere Informationen finden Sie unter Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="7b7ff-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b7ff-110">EXAMPLES</span></span>

### <span data-ttu-id="7b7ff-111">Beispiel 1: Erstellen eines Standard mäßigen Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="7b7ff-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="7b7ff-112">Mit diesem Befehl wird ein Schlüsseldepot mit dem Namen Contoso03Vault im Azure Region East US erstellt.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="7b7ff-113">Der Befehl fügt den schlüsseltresor zur Ressourcengruppe namens Gruppe14betrachteten hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="7b7ff-114">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="7b7ff-115">Beispiel 2: Erstellen eines Premium-Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="7b7ff-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="7b7ff-116">Mit diesem Befehl wird ein schlüsseltresor erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="7b7ff-117">Es gibt jedoch den Wert Premium für den *SKU* -Parameter an, um einen Premium-schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="7b7ff-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7b7ff-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="7b7ff-119">Erstellen eines Schlüsseldepots und Angeben von Netzwerkregeln, um den Zugriff auf die angegebene IP-Adresse aus dem virtuellen Netzwerk zu ermöglichen, das von $myNetworkResId identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="7b7ff-120">Weitere Informationen finden Sie unter `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="7b7ff-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="7b7ff-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b7ff-121">PARAMETERS</span></span>

### <span data-ttu-id="7b7ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7ff-122">-DefaultProfile</span></span>
<span data-ttu-id="7b7ff-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7b7ff-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b7ff-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7b7ff-124">-EnabledForDeployment</span></span>
<span data-ttu-id="7b7ff-125">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="7b7ff-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7b7ff-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7b7ff-127">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="7b7ff-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7b7ff-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7b7ff-129">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="7b7ff-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="7b7ff-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="7b7ff-131">Falls angegeben, ist der Schutz vor sofortiger Löschung für diesen Tresor aktiviert. erfordert, dass Soft Delete ebenfalls aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="7b7ff-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b7ff-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="7b7ff-133">Wenn angegeben, wird das Autorisieren von Daten Aktionen durch rollenbasierte Zugriffssteuerung (Role Based Access Control, RBAC) ermöglicht, und die in Vault-Eigenschaften angegebenen Zugriffsrichtlinien werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="7b7ff-134">Beachten Sie, dass Verwaltungsaktionen immer mit RBAC autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="7b7ff-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="7b7ff-135">-Location</span></span>
<span data-ttu-id="7b7ff-136">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="7b7ff-137">Verwenden Sie den Befehl [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) , um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="7b7ff-138">-Name</span><span class="sxs-lookup"><span data-stu-id="7b7ff-138">-Name</span></span>
<span data-ttu-id="7b7ff-139">Gibt den Namen des zu erstellende Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="7b7ff-140">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="7b7ff-141">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="7b7ff-142">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="7b7ff-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b7ff-143">-NetworkRuleSet</span></span>
<span data-ttu-id="7b7ff-144">Gibt den Netzwerkregel Satz des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="7b7ff-145">Sie steuert die Barrierefreiheit des Schlüsseldepots von bestimmten Netzwerkstandorten aus.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="7b7ff-146">Erstellt von `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="7b7ff-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="7b7ff-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b7ff-147">-ResourceGroupName</span></span>
<span data-ttu-id="7b7ff-148">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="7b7ff-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="7b7ff-149">-Sku</span></span>
<span data-ttu-id="7b7ff-150">Gibt die SKU der Key Vault-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="7b7ff-151">Informationen zu den Features, die für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault-Preis Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="7b7ff-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="7b7ff-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7b7ff-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="7b7ff-153">Gibt an, wie lange gelöschte Ressourcen aufbewahrt werden, und wie lange es dauert, bis ein Tresor oder ein Objekt im gelöschten Zustand bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="7b7ff-154">Der Standardwert ist 90 Tage.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="7b7ff-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b7ff-155">-Tag</span></span>
<span data-ttu-id="7b7ff-156">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="7b7ff-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b7ff-157">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7b7ff-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b7ff-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b7ff-158">-Confirm</span></span>
<span data-ttu-id="7b7ff-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b7ff-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b7ff-160">-WhatIf</span></span>
<span data-ttu-id="7b7ff-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b7ff-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b7ff-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7ff-163">CommonParameters</span></span>
<span data-ttu-id="7b7ff-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7ff-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b7ff-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7ff-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b7ff-166">INPUTS</span></span>

### <span data-ttu-id="7b7ff-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7b7ff-167">System.String</span></span>

### <span data-ttu-id="7b7ff-168">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7b7ff-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7b7ff-169">Microsoft. Azure. Management. keyvault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="7b7ff-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="7b7ff-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b7ff-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7b7ff-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b7ff-171">OUTPUTS</span></span>

### <span data-ttu-id="7b7ff-172">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7b7ff-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="7b7ff-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b7ff-173">NOTES</span></span>

## <span data-ttu-id="7b7ff-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b7ff-174">RELATED LINKS</span></span>

[<span data-ttu-id="7b7ff-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7b7ff-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="7b7ff-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7b7ff-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
