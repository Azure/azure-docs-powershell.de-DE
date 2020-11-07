---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848196"
---
# <span data-ttu-id="469b1-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="469b1-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="469b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="469b1-102">SYNOPSIS</span></span>
<span data-ttu-id="469b1-103">Erstellt in einem schlüsseltresor einen geheimen Schlüssel aus einem gesicherten Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="469b1-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="469b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="469b1-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="469b1-105">DESCRIPTION</span></span>
<span data-ttu-id="469b1-106">Das Cmdlet " **Restore-AzureKeyVaultSecret** " erstellt im angegebenen schlüsseltresor ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="469b1-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="469b1-107">Dieser Geheimtipp ist eine Replik des gesicherten Geheimnisses in der Eingabedatei und hat denselben Namen wie der ursprüngliche Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="469b1-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="469b1-108">Wenn der schlüsseltresor bereits über ein Kennwort mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Kennwort zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="469b1-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="469b1-109">Wenn die Sicherung mehrere Versionen eines Geheimnisses enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="469b1-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="469b1-110">Der schlüsseltresor, in den Sie den geheimen Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="469b1-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="469b1-111">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="469b1-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="469b1-112">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="469b1-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="469b1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="469b1-113">EXAMPLES</span></span>

### <span data-ttu-id="469b1-114">Beispiel 1: Wiederherstellen eines gesicherten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="469b1-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="469b1-115">Mit diesem Befehl wird ein geheimer, einschließlich aller seiner Versionen, aus der Sicherungsdatei "Backup. BLOB" in den schlüsseltresor mit dem Namen "MyKeyVault" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="469b1-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="469b1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="469b1-116">PARAMETERS</span></span>

### <span data-ttu-id="469b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469b1-117">-DefaultProfile</span></span>
<span data-ttu-id="469b1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="469b1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="469b1-119">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="469b1-119">-InputFile</span></span>
<span data-ttu-id="469b1-120">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="469b1-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="469b1-121">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="469b1-121">-VaultName</span></span>
<span data-ttu-id="469b1-122">Gibt den Namen des Schlüssel Tresors an, in den das Geheimnis wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="469b1-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="469b1-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="469b1-123">-Confirm</span></span>
<span data-ttu-id="469b1-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="469b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469b1-125">-WhatIf</span></span>
<span data-ttu-id="469b1-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="469b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469b1-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469b1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469b1-128">CommonParameters</span></span>
<span data-ttu-id="469b1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469b1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469b1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469b1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="469b1-131">INPUTS</span></span>

## <span data-ttu-id="469b1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="469b1-132">OUTPUTS</span></span>

### <span data-ttu-id="469b1-133">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="469b1-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="469b1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="469b1-134">NOTES</span></span>

## <span data-ttu-id="469b1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="469b1-135">RELATED LINKS</span></span>

[<span data-ttu-id="469b1-136">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="469b1-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="469b1-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="469b1-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="469b1-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="469b1-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="469b1-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="469b1-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

