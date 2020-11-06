---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504922"
---
# <span data-ttu-id="0e4aa-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0e4aa-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="0e4aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4aa-103">Erstellt einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e4aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e4aa-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e4aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e4aa-105">DESCRIPTION</span></span>
<span data-ttu-id="0e4aa-106">Das Cmdlet **New-AzureRmKeyVault** erstellt einen schlüsseltresor in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="0e4aa-107">Mit diesem Cmdlet werden dem aktuell angemeldeten Benutzer auch Berechtigungen zum Hinzufügen, entfernen oder Auflisten von Schlüsseln und Geheimnissen im schlüsseltresor gewährt.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="0e4aa-108">Hinweis: Wenn der Fehler angezeigt **wird, dass das Abonnement nicht registriert ist, um den Namespace "Microsoft. keyvault" zu verwenden** , wenn Sie versuchen, ihren neuen schlüsseltresor zu erstellen, führen Sie **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. keyvault"** aus, und führen Sie dann den Befehl **neu-AzureRmKeyVault** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="0e4aa-109">Weitere Informationen finden Sie unter Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="0e4aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e4aa-110">EXAMPLES</span></span>

### <span data-ttu-id="0e4aa-111">Beispiel 1: Erstellen eines Standard mäßigen Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="0e4aa-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="0e4aa-112">Mit diesem Befehl wird ein Schlüsseldepot mit dem Namen Contoso03Vault im Azure Region East US erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="0e4aa-113">Der Befehl fügt den schlüsseltresor zur Ressourcengruppe namens Gruppe14betrachteten hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="0e4aa-114">Da der Befehl keinen Wert für den *SKU* -Parameter angibt, wird ein Standard schlüsseltresor erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="0e4aa-115">Beispiel 2: Erstellen eines Premium-Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="0e4aa-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="0e4aa-116">Mit diesem Befehl wird ein schlüsseltresor erstellt, genau wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="0e4aa-117">Es gibt jedoch den Wert Premium für den *SKU* -Parameter an, um einen Premium-schlüsseltresor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="0e4aa-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e4aa-118">PARAMETERS</span></span>

### <span data-ttu-id="0e4aa-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="0e4aa-119">-EnabledForDeployment</span></span>
<span data-ttu-id="0e4aa-120">Ermöglicht es dem Microsoft. Compute-Ressourcenanbieter, Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn bei der Ressourcenerstellung auf diesen schlüsseltresor verwiesen wird, beispielsweise beim Erstellen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="0e4aa-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0e4aa-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="0e4aa-122">Aktiviert den Azure Disk Encryption-Dienst, um Geheimnisse zu erhalten und die Schlüssel aus diesem schlüsseltresor zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="0e4aa-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="0e4aa-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="0e4aa-124">Aktiviert den Azure Resource Manager, um Geheimnisse aus diesem Schlüsselspeicher abzurufen, wenn in einer Vorlagenbereitstellung auf diesen schlüsseltresor verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="0e4aa-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="0e4aa-125">-EnableSoftDelete</span></span>
<span data-ttu-id="0e4aa-126">Wenn angegeben, ist die Funktion "Soft Delete" für diesen schlüsseltresor aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

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

### <span data-ttu-id="0e4aa-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e4aa-127">-Location</span></span>
<span data-ttu-id="0e4aa-128">Gibt den Azure-Bereich an, in dem der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="0e4aa-129">Verwenden Sie den Befehl Get-AzureLocation ( https://msdn.microsoft.com/ Library/Azure/mt589064. aspx), um Ihre Auswahlmöglichkeiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="0e4aa-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="0e4aa-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e4aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e4aa-132">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="0e4aa-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="0e4aa-133">-Sku</span></span>
<span data-ttu-id="0e4aa-134">Gibt die SKU der Key Vault-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="0e4aa-135">Informationen zu den Features, die für jede SKU verfügbar sind, finden Sie auf der Azure Key Vault-Preis Website ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="0e4aa-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="0e4aa-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e4aa-136">-Tag</span></span>
<span data-ttu-id="0e4aa-137">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0e4aa-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e4aa-138">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0e4aa-138">For example:</span></span>

<span data-ttu-id="0e4aa-139">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0e4aa-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e4aa-140">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0e4aa-140">-VaultName</span></span>
<span data-ttu-id="0e4aa-141">Gibt den Namen des zu erstellende Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="0e4aa-142">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="0e4aa-143">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="0e4aa-144">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="0e4aa-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e4aa-145">-Confirm</span></span>
<span data-ttu-id="0e4aa-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e4aa-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e4aa-147">-WhatIf</span></span>
<span data-ttu-id="0e4aa-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e4aa-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e4aa-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4aa-150">-DefaultProfile</span></span>
<span data-ttu-id="0e4aa-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4aa-152">CommonParameters</span></span>
<span data-ttu-id="0e4aa-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4aa-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e4aa-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4aa-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e4aa-155">INPUTS</span></span>

## <span data-ttu-id="0e4aa-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e4aa-156">OUTPUTS</span></span>

### <span data-ttu-id="0e4aa-157">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="0e4aa-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="0e4aa-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e4aa-158">NOTES</span></span>

## <span data-ttu-id="0e4aa-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e4aa-159">RELATED LINKS</span></span>

[<span data-ttu-id="0e4aa-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0e4aa-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="0e4aa-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0e4aa-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
