---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650888"
---
# <span data-ttu-id="f5e7a-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f5e7a-101">New-AzKeyVault</span></span>

## <span data-ttu-id="f5e7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e7a-103">Erstellt einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-103">Creates a key vault.</span></span>

## <span data-ttu-id="f5e7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5e7a-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e7a-106">Das Cmdlet **New-AzKeyVault** erstellt einen schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="f5e7a-107">Mit diesem Cmdlet werden dem aktuell angemeldeten Benutzer auch Berechtigungen zum Hinzufügen, entfernen oder Auflisten von Schlüsseln und Geheimnissen im schlüsseltresor gewährt.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="f5e7a-108">Hinweis: Wenn der Fehler angezeigt **wird, dass das Abonnement nicht registriert ist, um den Namespace "Microsoft. keyvault" zu verwenden** , wenn Sie versuchen, ihren neuen schlüsseltresor zu erstellen, führen Sie **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** aus, und führen Sie dann den Befehl **neu-AzKeyVault** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="f5e7a-109">Weitere Informationen finden Sie unter Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="f5e7a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e7a-111">Beispiel 1: Erstellen eines Standard mäßigen Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="f5e7a-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="f5e7a-112">Mit diesem Befehl wird ein Schlüsseldepot mit dem Namen Contoso03Vault im Azure Region East US erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="f5e7a-113">Der Befehl fügt den schlüsseltresor zur Ressourcengruppe namens Gruppe14betrachteten hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="f5e7a-114">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="f5e7a-115">Beispiel 2: Erstellen eines Premium-Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="f5e7a-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="f5e7a-116">Mit diesem Befehl wird ein schlüsseltresor erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="f5e7a-117">Es gibt jedoch den Wert Premium für den *SKU* -Parameter an, um einen Premium-schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="f5e7a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5e7a-118">PARAMETERS</span></span>

### <span data-ttu-id="f5e7a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e7a-119">-DefaultProfile</span></span>
<span data-ttu-id="f5e7a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f5e7a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5e7a-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f5e7a-121">-EnabledForDeployment</span></span>
<span data-ttu-id="f5e7a-122">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="f5e7a-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f5e7a-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f5e7a-124">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="f5e7a-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f5e7a-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f5e7a-126">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="f5e7a-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="f5e7a-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="f5e7a-128">Falls angegeben, ist der Schutz vor sofortiger Löschung für diesen Tresor aktiviert. erfordert, dass Soft Delete ebenfalls aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="f5e7a-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="f5e7a-129">-EnableSoftDelete</span></span>
<span data-ttu-id="f5e7a-130">Gibt an, dass die Soft-Delete-Funktion für diesen schlüsseltresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="f5e7a-131">Wenn "Soft-Delete" aktiviert ist, können Sie diesen schlüsseltresor und dessen Inhalt für eine Kulanzzeit wiederherstellen, nachdem er gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="f5e7a-132">Weitere Informationen zu dieser Funktion finden Sie unter [Übersicht über Azure Key Vault (Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)).</span><span class="sxs-lookup"><span data-stu-id="f5e7a-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="f5e7a-133">Anleitungen finden Sie unter so wird es [gemacht: Verwenden von Key Vault Soft-Delete mit PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="f5e7a-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="f5e7a-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5e7a-134">-Location</span></span>
<span data-ttu-id="f5e7a-135">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="f5e7a-136">Verwenden Sie den Befehl [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) , um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="f5e7a-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f5e7a-137">-Name</span></span>
<span data-ttu-id="f5e7a-138">Gibt den Namen des zu erstellende Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="f5e7a-139">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="f5e7a-140">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="f5e7a-141">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="f5e7a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e7a-142">-ResourceGroupName</span></span>
<span data-ttu-id="f5e7a-143">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="f5e7a-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="f5e7a-144">-Sku</span></span>
<span data-ttu-id="f5e7a-145">Gibt die SKU der Key Vault-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="f5e7a-146">Informationen zu den Features, die für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault-Preis Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="f5e7a-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e7a-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5e7a-147">-Tag</span></span>
<span data-ttu-id="f5e7a-148">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f5e7a-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5e7a-149">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f5e7a-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f5e7a-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5e7a-150">-Confirm</span></span>
<span data-ttu-id="f5e7a-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e7a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e7a-152">-WhatIf</span></span>
<span data-ttu-id="f5e7a-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e7a-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e7a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e7a-155">CommonParameters</span></span>
<span data-ttu-id="f5e7a-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e7a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e7a-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e7a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e7a-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5e7a-158">INPUTS</span></span>

### <span data-ttu-id="f5e7a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e7a-159">System.String</span></span>

### <span data-ttu-id="f5e7a-160">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f5e7a-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f5e7a-161">Microsoft. Azure. Management. keyvault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="f5e7a-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="f5e7a-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f5e7a-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5e7a-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5e7a-163">OUTPUTS</span></span>

### <span data-ttu-id="f5e7a-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f5e7a-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f5e7a-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5e7a-165">NOTES</span></span>

## <span data-ttu-id="f5e7a-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5e7a-166">RELATED LINKS</span></span>

[<span data-ttu-id="f5e7a-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f5e7a-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f5e7a-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f5e7a-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
