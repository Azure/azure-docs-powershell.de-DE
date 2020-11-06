---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504913"
---
# <span data-ttu-id="63e61-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63e61-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="63e61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63e61-102">SYNOPSIS</span></span>
<span data-ttu-id="63e61-103">Erstellt einen Schlüssel in einem schlüsseltresor aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="63e61-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e61-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e61-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63e61-105">DESCRIPTION</span></span>
<span data-ttu-id="63e61-106">Das Cmdlet **Restore-AzureKeyVaultKey** erstellt einen Schlüssel im angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="63e61-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="63e61-107">Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="63e61-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="63e61-108">Wenn der schlüsseltresor bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="63e61-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="63e61-109">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="63e61-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="63e61-110">Der schlüsseltresor, in den Sie den Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="63e61-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="63e61-111">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="63e61-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="63e61-112">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="63e61-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="63e61-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63e61-113">EXAMPLES</span></span>

### <span data-ttu-id="63e61-114">Beispiel 1: Wiederherstellen eines gesicherten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="63e61-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="63e61-115">Mit diesem Befehl wird ein Schlüssel, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="63e61-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="63e61-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="63e61-116">PARAMETERS</span></span>

### <span data-ttu-id="63e61-117">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="63e61-117">-InputFile</span></span>
<span data-ttu-id="63e61-118">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="63e61-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e61-119">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="63e61-119">-VaultName</span></span>
<span data-ttu-id="63e61-120">Gibt den Namen des Schlüssel Tresors an, in den der Schlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63e61-120">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="63e61-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63e61-121">-Confirm</span></span>
<span data-ttu-id="63e61-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63e61-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e61-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e61-123">-WhatIf</span></span>
<span data-ttu-id="63e61-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63e61-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e61-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63e61-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e61-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e61-126">-DefaultProfile</span></span>
<span data-ttu-id="63e61-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63e61-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e61-128">CommonParameters</span></span>
<span data-ttu-id="63e61-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e61-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e61-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e61-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63e61-131">INPUTS</span></span>

## <span data-ttu-id="63e61-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63e61-132">OUTPUTS</span></span>

### <span data-ttu-id="63e61-133">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="63e61-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="63e61-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="63e61-134">NOTES</span></span>

## <span data-ttu-id="63e61-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63e61-135">RELATED LINKS</span></span>

[<span data-ttu-id="63e61-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63e61-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="63e61-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63e61-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="63e61-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63e61-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="63e61-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63e61-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

