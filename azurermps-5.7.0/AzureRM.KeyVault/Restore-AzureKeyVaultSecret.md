---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498937"
---
# <span data-ttu-id="11e7b-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="11e7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="11e7b-103">Erstellt in einem schlüsseltresor einen geheimen Schlüssel aus einem gesicherten Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11e7b-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e7b-104">SYNTAX</span></span>

### <span data-ttu-id="11e7b-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="11e7b-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e7b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="11e7b-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e7b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="11e7b-108">Das Cmdlet " **Restore-AzureKeyVaultSecret** " erstellt im angegebenen schlüsseltresor ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="11e7b-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="11e7b-109">Dieser Geheimtipp ist eine Replik des gesicherten Geheimnisses in der Eingabedatei und hat denselben Namen wie der ursprüngliche Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11e7b-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="11e7b-110">Wenn der schlüsseltresor bereits über ein Kennwort mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Kennwort zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="11e7b-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="11e7b-111">Wenn die Sicherung mehrere Versionen eines Geheimnisses enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="11e7b-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="11e7b-112">Der schlüsseltresor, in den Sie den geheimen Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="11e7b-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="11e7b-113">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="11e7b-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="11e7b-114">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="11e7b-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="11e7b-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11e7b-115">EXAMPLES</span></span>

### <span data-ttu-id="11e7b-116">Beispiel 1: Wiederherstellen eines gesicherten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="11e7b-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="11e7b-117">Mit diesem Befehl wird ein geheimer, einschließlich aller seiner Versionen, aus der Sicherungsdatei "Backup. BLOB" in den schlüsseltresor mit dem Namen "MyKeyVault" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="11e7b-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="11e7b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="11e7b-118">PARAMETERS</span></span>

### <span data-ttu-id="11e7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e7b-119">-DefaultProfile</span></span>
<span data-ttu-id="11e7b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="11e7b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11e7b-121">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="11e7b-121">-InputFile</span></span>
<span data-ttu-id="11e7b-122">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="11e7b-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="11e7b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11e7b-123">-InputObject</span></span>
<span data-ttu-id="11e7b-124">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="11e7b-124">KeyVault object</span></span>

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

### <span data-ttu-id="11e7b-125">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="11e7b-125">-VaultName</span></span>
<span data-ttu-id="11e7b-126">Gibt den Namen des Schlüssel Tresors an, in den das Geheimnis wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11e7b-126">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="11e7b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11e7b-127">-Confirm</span></span>
<span data-ttu-id="11e7b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11e7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e7b-129">-WhatIf</span></span>
<span data-ttu-id="11e7b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11e7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e7b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11e7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e7b-132">CommonParameters</span></span>
<span data-ttu-id="11e7b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e7b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e7b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11e7b-135">INPUTS</span></span>

### <span data-ttu-id="11e7b-136">Keine</span><span class="sxs-lookup"><span data-stu-id="11e7b-136">None</span></span>
<span data-ttu-id="11e7b-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="11e7b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11e7b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11e7b-138">OUTPUTS</span></span>

### <span data-ttu-id="11e7b-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="11e7b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="11e7b-140">NOTES</span></span>

## <span data-ttu-id="11e7b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11e7b-141">RELATED LINKS</span></span>

[<span data-ttu-id="11e7b-142">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e7b-143">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e7b-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e7b-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e7b-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

