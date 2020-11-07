---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843876"
---
# <span data-ttu-id="c3048-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3048-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="c3048-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3048-102">SYNOPSIS</span></span>
<span data-ttu-id="c3048-103">Erstellt in einem schlüsseltresor einen geheimen Schlüssel aus einem gesicherten Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c3048-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="c3048-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3048-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3048-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3048-105">DESCRIPTION</span></span>
<span data-ttu-id="c3048-106">Das Cmdlet " **Restore-AzKeyVaultSecret** " erstellt im angegebenen schlüsseltresor ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="c3048-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="c3048-107">Dieser Geheimtipp ist eine Replik des gesicherten Geheimnisses in der Eingabedatei und hat denselben Namen wie der ursprüngliche Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c3048-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="c3048-108">Wenn der schlüsseltresor bereits über ein Kennwort mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Kennwort zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c3048-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="c3048-109">Wenn die Sicherung mehrere Versionen eines Geheimnisses enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c3048-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="c3048-110">Der schlüsseltresor, in den Sie den geheimen Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="c3048-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="c3048-111">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="c3048-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="c3048-112">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="c3048-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="c3048-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3048-113">EXAMPLES</span></span>

### <span data-ttu-id="c3048-114">Beispiel 1: Wiederherstellen eines gesicherten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="c3048-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="c3048-115">Mit diesem Befehl wird ein geheimer, einschließlich aller seiner Versionen, aus der Sicherungsdatei "Backup. BLOB" in den schlüsseltresor mit dem Namen "MyKeyVault" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c3048-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="c3048-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3048-116">PARAMETERS</span></span>

### <span data-ttu-id="c3048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3048-117">-DefaultProfile</span></span>
<span data-ttu-id="c3048-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3048-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3048-119">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="c3048-119">-InputFile</span></span>
<span data-ttu-id="c3048-120">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="c3048-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="c3048-121">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c3048-121">-VaultName</span></span>
<span data-ttu-id="c3048-122">Gibt den Namen des Schlüssel Tresors an, in den das Geheimnis wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3048-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="c3048-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3048-123">-Confirm</span></span>
<span data-ttu-id="c3048-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3048-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3048-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3048-125">-WhatIf</span></span>
<span data-ttu-id="c3048-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3048-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3048-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3048-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3048-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3048-128">CommonParameters</span></span>
<span data-ttu-id="c3048-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3048-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3048-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3048-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3048-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3048-131">INPUTS</span></span>

### <span data-ttu-id="c3048-132">Keine</span><span class="sxs-lookup"><span data-stu-id="c3048-132">None</span></span>
<span data-ttu-id="c3048-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c3048-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3048-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3048-134">OUTPUTS</span></span>

### <span data-ttu-id="c3048-135">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="c3048-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="c3048-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3048-136">NOTES</span></span>

## <span data-ttu-id="c3048-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3048-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3048-138">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3048-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="c3048-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3048-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="c3048-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3048-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="c3048-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3048-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

