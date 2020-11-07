---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663060"
---
# <span data-ttu-id="0d5d1-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="0d5d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5d1-103">Erstellt einen Schlüssel in einem schlüsseltresor aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d5d1-104">SYNTAX</span></span>

### <span data-ttu-id="0d5d1-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d5d1-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5d1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d5d1-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d5d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d5d1-107">DESCRIPTION</span></span>
<span data-ttu-id="0d5d1-108">Das Cmdlet **Restore-AzureKeyVaultKey** erstellt einen Schlüssel im angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="0d5d1-109">Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="0d5d1-110">Wenn der schlüsseltresor bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="0d5d1-111">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="0d5d1-112">Der schlüsseltresor, in den Sie den Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="0d5d1-113">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="0d5d1-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="0d5d1-114">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="0d5d1-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d5d1-115">EXAMPLES</span></span>

### <span data-ttu-id="0d5d1-116">Beispiel 1: Wiederherstellen eines gesicherten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0d5d1-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="0d5d1-117">Mit diesem Befehl wird ein Schlüssel, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="0d5d1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d5d1-118">PARAMETERS</span></span>

### <span data-ttu-id="0d5d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5d1-119">-DefaultProfile</span></span>
<span data-ttu-id="0d5d1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d5d1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d5d1-121">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="0d5d1-121">-InputFile</span></span>
<span data-ttu-id="0d5d1-122">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-122">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5d1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d5d1-123">-InputObject</span></span>
<span data-ttu-id="0d5d1-124">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="0d5d1-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5d1-125">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0d5d1-125">-VaultName</span></span>
<span data-ttu-id="0d5d1-126">Gibt den Namen des Schlüssel Tresors an, in den der Schlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-126">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5d1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d5d1-127">-Confirm</span></span>
<span data-ttu-id="0d5d1-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d5d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5d1-129">-WhatIf</span></span>
<span data-ttu-id="0d5d1-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d5d1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d5d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5d1-132">CommonParameters</span></span>
<span data-ttu-id="0d5d1-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5d1-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5d1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5d1-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d5d1-135">INPUTS</span></span>

### <span data-ttu-id="0d5d1-136">Keine</span><span class="sxs-lookup"><span data-stu-id="0d5d1-136">None</span></span>
<span data-ttu-id="0d5d1-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0d5d1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d5d1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d5d1-138">OUTPUTS</span></span>

### <span data-ttu-id="0d5d1-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0d5d1-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d5d1-140">NOTES</span></span>

## <span data-ttu-id="0d5d1-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d5d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="0d5d1-142">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="0d5d1-143">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="0d5d1-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="0d5d1-145">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d5d1-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

