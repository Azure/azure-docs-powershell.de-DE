---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843883"
---
# <span data-ttu-id="eb8ac-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eb8ac-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="eb8ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8ac-103">Erstellt einen Schlüssel in einem schlüsseltresor aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="eb8ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb8ac-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8ac-106">Das Cmdlet **Restore-AzKeyVaultKey** erstellt einen Schlüssel im angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="eb8ac-107">Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="eb8ac-108">Wenn der schlüsseltresor bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="eb8ac-109">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="eb8ac-110">Der schlüsseltresor, in den Sie den Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="eb8ac-111">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="eb8ac-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="eb8ac-112">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="eb8ac-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb8ac-113">EXAMPLES</span></span>

### <span data-ttu-id="eb8ac-114">Beispiel 1: Wiederherstellen eines gesicherten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="eb8ac-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="eb8ac-115">Mit diesem Befehl wird ein Schlüssel, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="eb8ac-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb8ac-116">PARAMETERS</span></span>

### <span data-ttu-id="eb8ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8ac-117">-DefaultProfile</span></span>
<span data-ttu-id="eb8ac-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eb8ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb8ac-119">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="eb8ac-119">-InputFile</span></span>
<span data-ttu-id="eb8ac-120">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="eb8ac-121">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="eb8ac-121">-VaultName</span></span>
<span data-ttu-id="eb8ac-122">Gibt den Namen des Schlüssel Tresors an, in den der Schlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="eb8ac-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb8ac-123">-Confirm</span></span>
<span data-ttu-id="eb8ac-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8ac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8ac-125">-WhatIf</span></span>
<span data-ttu-id="eb8ac-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8ac-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8ac-128">CommonParameters</span></span>
<span data-ttu-id="eb8ac-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8ac-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8ac-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8ac-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb8ac-131">INPUTS</span></span>

### <span data-ttu-id="eb8ac-132">Keine</span><span class="sxs-lookup"><span data-stu-id="eb8ac-132">None</span></span>
<span data-ttu-id="eb8ac-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="eb8ac-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb8ac-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb8ac-134">OUTPUTS</span></span>

### <span data-ttu-id="eb8ac-135">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="eb8ac-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="eb8ac-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb8ac-136">NOTES</span></span>

## <span data-ttu-id="eb8ac-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb8ac-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb8ac-138">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eb8ac-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="eb8ac-139">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eb8ac-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="eb8ac-140">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eb8ac-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="eb8ac-141">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eb8ac-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

