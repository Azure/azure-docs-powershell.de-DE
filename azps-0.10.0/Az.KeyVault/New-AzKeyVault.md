---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 41fcea2b0afc7c18da2f3e4e71764bff1ab2920c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843887"
---
# <span data-ttu-id="922e7-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="922e7-101">New-AzKeyVault</span></span>

## <span data-ttu-id="922e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="922e7-102">SYNOPSIS</span></span>
<span data-ttu-id="922e7-103">Erstellt einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="922e7-103">Creates a key vault.</span></span>

## <span data-ttu-id="922e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="922e7-104">SYNTAX</span></span>

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="922e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="922e7-105">DESCRIPTION</span></span>
<span data-ttu-id="922e7-106">Das Cmdlet **New-AzKeyVault** erstellt einen schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="922e7-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="922e7-107">Mit diesem Cmdlet werden dem aktuell angemeldeten Benutzer auch Berechtigungen zum Hinzufügen, entfernen oder Auflisten von Schlüsseln und Geheimnissen im schlüsseltresor gewährt.</span><span class="sxs-lookup"><span data-stu-id="922e7-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="922e7-108">Hinweis: Wenn der Fehler angezeigt **wird, dass das Abonnement nicht registriert ist, um den Namespace "Microsoft. keyvault" zu verwenden** , wenn Sie versuchen, ihren neuen schlüsseltresor zu erstellen, führen Sie **Register-AzResourceProvider-ProviderNamespace "Microsoft. keyvault"** aus, und führen Sie dann den Befehl **neu-AzKeyVault** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="922e7-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="922e7-109">Weitere Informationen finden Sie unter Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="922e7-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="922e7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="922e7-110">EXAMPLES</span></span>

### <span data-ttu-id="922e7-111">Beispiel 1: Erstellen eines Standard mäßigen Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="922e7-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="922e7-112">Mit diesem Befehl wird ein Schlüsseldepot mit dem Namen Contoso03Vault im Azure Region East US erstellt.</span><span class="sxs-lookup"><span data-stu-id="922e7-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="922e7-113">Der Befehl fügt den schlüsseltresor zur Ressourcengruppe namens Gruppe14betrachteten hinzu.</span><span class="sxs-lookup"><span data-stu-id="922e7-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="922e7-114">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="922e7-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="922e7-115">Beispiel 2: Erstellen eines Premium-Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="922e7-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="922e7-116">Mit diesem Befehl wird ein schlüsseltresor erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="922e7-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="922e7-117">Es gibt jedoch den Wert Premium für den *SKU* -Parameter an, um einen Premium-schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="922e7-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="922e7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="922e7-118">PARAMETERS</span></span>

### <span data-ttu-id="922e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922e7-119">-DefaultProfile</span></span>
<span data-ttu-id="922e7-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="922e7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922e7-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="922e7-121">-EnabledForDeployment</span></span>
<span data-ttu-id="922e7-122">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="922e7-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="922e7-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="922e7-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="922e7-124">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="922e7-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="922e7-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="922e7-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="922e7-126">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="922e7-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="922e7-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="922e7-127">-EnableSoftDelete</span></span>
<span data-ttu-id="922e7-128">Gibt an, dass die Soft-Delete-Funktion für diesen schlüsseltresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="922e7-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="922e7-129">Wenn "Soft-Delete" aktiviert ist, können Sie diesen schlüsseltresor und dessen Inhalt für eine Kulanzzeit wiederherstellen, nachdem er gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="922e7-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="922e7-130">Weitere Informationen zu dieser Funktion finden Sie unter [Übersicht über Azure Key Vault (Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)).</span><span class="sxs-lookup"><span data-stu-id="922e7-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="922e7-131">Anleitungen finden Sie unter so wird es [gemacht: Verwenden von Key Vault Soft-Delete mit PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="922e7-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="922e7-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="922e7-132">-Location</span></span>
<span data-ttu-id="922e7-133">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="922e7-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="922e7-134">Verwenden Sie den Befehl [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) , um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="922e7-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

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

### <span data-ttu-id="922e7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922e7-135">-ResourceGroupName</span></span>
<span data-ttu-id="922e7-136">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="922e7-136">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="922e7-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="922e7-137">-Sku</span></span>
<span data-ttu-id="922e7-138">Gibt die SKU der Key Vault-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="922e7-138">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="922e7-139">Informationen zu den Features, die für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault-Preis Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="922e7-139">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="922e7-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="922e7-140">-Tag</span></span>
<span data-ttu-id="922e7-141">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="922e7-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="922e7-142">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="922e7-142">For example:</span></span>

<span data-ttu-id="922e7-143">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="922e7-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="922e7-144">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="922e7-144">-VaultName</span></span>
<span data-ttu-id="922e7-145">Gibt den Namen des zu erstellende Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="922e7-145">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="922e7-146">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="922e7-146">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="922e7-147">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="922e7-147">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="922e7-148">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="922e7-148">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922e7-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="922e7-149">-Confirm</span></span>
<span data-ttu-id="922e7-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="922e7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922e7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922e7-151">-WhatIf</span></span>
<span data-ttu-id="922e7-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="922e7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922e7-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="922e7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922e7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922e7-154">CommonParameters</span></span>
<span data-ttu-id="922e7-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922e7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922e7-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922e7-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922e7-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="922e7-157">INPUTS</span></span>

### <span data-ttu-id="922e7-158">Keine</span><span class="sxs-lookup"><span data-stu-id="922e7-158">None</span></span>
<span data-ttu-id="922e7-159">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="922e7-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="922e7-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="922e7-160">OUTPUTS</span></span>

### <span data-ttu-id="922e7-161">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="922e7-161">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="922e7-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="922e7-162">NOTES</span></span>

## <span data-ttu-id="922e7-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="922e7-163">RELATED LINKS</span></span>

[<span data-ttu-id="922e7-164">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="922e7-164">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="922e7-165">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="922e7-165">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
