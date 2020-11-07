---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: ea2478225c3e5b3c0a3746a44aca13745e1af963
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662453"
---
# <span data-ttu-id="21d2a-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="21d2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="21d2a-103">Erstellt in einem schlüsseltresor einen geheimen Schlüssel aus einem gesicherten Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="21d2a-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21d2a-104">SYNTAX</span></span>

### <span data-ttu-id="21d2a-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="21d2a-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d2a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21d2a-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d2a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21d2a-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21d2a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="21d2a-109">Das Cmdlet " **Restore-AzureKeyVaultSecret** " erstellt im angegebenen schlüsseltresor ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="21d2a-109">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="21d2a-110">Dieser Geheimtipp ist eine Replik des gesicherten Geheimnisses in der Eingabedatei und hat denselben Namen wie der ursprüngliche Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="21d2a-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="21d2a-111">Wenn der schlüsseltresor bereits über ein Kennwort mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Kennwort zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="21d2a-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="21d2a-112">Wenn die Sicherung mehrere Versionen eines Geheimnisses enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="21d2a-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="21d2a-113">Der schlüsseltresor, in den Sie den geheimen Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="21d2a-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="21d2a-114">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="21d2a-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="21d2a-115">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="21d2a-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="21d2a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21d2a-116">EXAMPLES</span></span>

### <span data-ttu-id="21d2a-117">Beispiel 1: Wiederherstellen eines gesicherten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="21d2a-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="21d2a-118">Mit diesem Befehl wird ein geheimer, einschließlich aller seiner Versionen, aus der Sicherungsdatei "Backup. BLOB" in den schlüsseltresor mit dem Namen "Contoso" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="21d2a-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="21d2a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="21d2a-119">PARAMETERS</span></span>

### <span data-ttu-id="21d2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d2a-120">-DefaultProfile</span></span>
<span data-ttu-id="21d2a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="21d2a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21d2a-122">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="21d2a-122">-InputFile</span></span>
<span data-ttu-id="21d2a-123">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="21d2a-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21d2a-124">-InputObject</span></span>
<span data-ttu-id="21d2a-125">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="21d2a-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="21d2a-126">-ResourceId</span></span>
<span data-ttu-id="21d2a-127">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="21d2a-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="21d2a-128">-VaultName</span></span>
<span data-ttu-id="21d2a-129">Gibt den Namen des Schlüssel Tresors an, in den das Geheimnis wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21d2a-129">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21d2a-130">-Confirm</span></span>
<span data-ttu-id="21d2a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21d2a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d2a-132">-WhatIf</span></span>
<span data-ttu-id="21d2a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21d2a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d2a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21d2a-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d2a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d2a-135">CommonParameters</span></span>
<span data-ttu-id="21d2a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d2a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d2a-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d2a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d2a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21d2a-138">INPUTS</span></span>

### <span data-ttu-id="21d2a-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="21d2a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="21d2a-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="21d2a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="21d2a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="21d2a-141">System.String</span></span>

## <span data-ttu-id="21d2a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21d2a-142">OUTPUTS</span></span>

### <span data-ttu-id="21d2a-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="21d2a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="21d2a-144">NOTES</span></span>

## <span data-ttu-id="21d2a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21d2a-145">RELATED LINKS</span></span>

[<span data-ttu-id="21d2a-146">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-146">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="21d2a-147">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-147">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="21d2a-148">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-148">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="21d2a-149">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21d2a-149">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

