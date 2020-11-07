---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 7cc4af3e849a6cd24c2144c6e92c990da261e9d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664229"
---
# <span data-ttu-id="2f834-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2f834-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="2f834-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f834-102">SYNOPSIS</span></span>
<span data-ttu-id="2f834-103">Erstellt einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2f834-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f834-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f834-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f834-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f834-105">DESCRIPTION</span></span>
<span data-ttu-id="2f834-106">Das Cmdlet **New-AzureRmKeyVault** erstellt einen schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f834-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="2f834-107">Mit diesem Cmdlet werden dem aktuell angemeldeten Benutzer auch Berechtigungen zum Hinzufügen, entfernen oder Auflisten von Schlüsseln und Geheimnissen im schlüsseltresor gewährt.</span><span class="sxs-lookup"><span data-stu-id="2f834-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="2f834-108">Hinweis: Wenn der Fehler angezeigt **wird, dass das Abonnement nicht registriert ist, um den Namespace "Microsoft. keyvault" zu verwenden** , wenn Sie versuchen, ihren neuen schlüsseltresor zu erstellen, führen Sie **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. keyvault"** aus, und führen Sie dann den Befehl **neu-AzureRmKeyVault** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="2f834-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="2f834-109">Weitere Informationen finden Sie unter Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="2f834-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="2f834-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f834-110">EXAMPLES</span></span>

### <span data-ttu-id="2f834-111">Beispiel 1: Erstellen eines Standard mäßigen Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="2f834-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="2f834-112">Mit diesem Befehl wird ein Schlüsseldepot mit dem Namen Contoso03Vault im Azure Region East US erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f834-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="2f834-113">Der Befehl fügt den schlüsseltresor zur Ressourcengruppe namens Gruppe14betrachteten hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f834-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="2f834-114">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f834-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="2f834-115">Beispiel 2: Erstellen eines Premium-Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="2f834-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="2f834-116">Mit diesem Befehl wird ein schlüsseltresor erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2f834-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="2f834-117">Es gibt jedoch den Wert Premium für den *SKU* -Parameter an, um einen Premium-schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f834-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="2f834-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f834-118">PARAMETERS</span></span>

### <span data-ttu-id="2f834-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f834-119">-DefaultProfile</span></span>
<span data-ttu-id="2f834-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2f834-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f834-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2f834-121">-EnabledForDeployment</span></span>
<span data-ttu-id="2f834-122">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="2f834-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2f834-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2f834-124">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="2f834-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2f834-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2f834-126">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2f834-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="2f834-127">-EnableSoftDelete</span></span>
<span data-ttu-id="2f834-128">Gibt an, dass die Soft-Delete-Funktion für diesen schlüsseltresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f834-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="2f834-129">Wenn "Soft-Delete" aktiviert ist, können Sie diesen schlüsseltresor und dessen Inhalt für eine Kulanzzeit wiederherstellen, nachdem er gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="2f834-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="2f834-130">Weitere Informationen zu dieser Funktion finden Sie unter [Übersicht über Azure Key Vault (Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)).</span><span class="sxs-lookup"><span data-stu-id="2f834-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="2f834-131">Anleitungen finden Sie unter so wird es [gemacht: Verwenden von Key Vault Soft-Delete mit PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="2f834-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="2f834-132">-Location</span></span>
<span data-ttu-id="2f834-133">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f834-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="2f834-134">Verwenden Sie den Befehl [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) , um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2f834-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2f834-135">-Name</span></span>
<span data-ttu-id="2f834-136">Gibt den Namen des zu erstellende Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="2f834-136">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="2f834-137">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="2f834-137">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="2f834-138">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="2f834-138">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="2f834-139">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2f834-139">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f834-140">-ResourceGroupName</span></span>
<span data-ttu-id="2f834-141">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f834-141">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="2f834-142">-Sku</span></span>
<span data-ttu-id="2f834-143">Gibt die SKU der Key Vault-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="2f834-143">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="2f834-144">Informationen zu den Features, die für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault-Preis Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="2f834-144">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f834-145">-Tag</span></span>
<span data-ttu-id="2f834-146">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2f834-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f834-147">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2f834-147">For example:</span></span>

<span data-ttu-id="2f834-148">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2f834-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f834-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f834-149">-Confirm</span></span>
<span data-ttu-id="2f834-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f834-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f834-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f834-151">-WhatIf</span></span>
<span data-ttu-id="2f834-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f834-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f834-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f834-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f834-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f834-154">CommonParameters</span></span>
<span data-ttu-id="2f834-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f834-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f834-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f834-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f834-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f834-157">INPUTS</span></span>

### <span data-ttu-id="2f834-158">Keine</span><span class="sxs-lookup"><span data-stu-id="2f834-158">None</span></span>
<span data-ttu-id="2f834-159">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2f834-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f834-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f834-160">OUTPUTS</span></span>

### <span data-ttu-id="2f834-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2f834-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2f834-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f834-162">NOTES</span></span>

## <span data-ttu-id="2f834-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f834-163">RELATED LINKS</span></span>

[<span data-ttu-id="2f834-164">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2f834-164">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="2f834-165">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2f834-165">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
