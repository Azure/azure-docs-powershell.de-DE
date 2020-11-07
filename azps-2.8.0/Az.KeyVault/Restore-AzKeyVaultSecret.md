---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 9fb79628b123b5d35ae5d55ba31fd07dcbd85775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650853"
---
# <span data-ttu-id="ea9b9-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ea9b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9b9-103">Erstellt in einem schlüsseltresor einen geheimen Schlüssel aus einem gesicherten Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="ea9b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea9b9-104">SYNTAX</span></span>

### <span data-ttu-id="ea9b9-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea9b9-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea9b9-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9b9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea9b9-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9b9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea9b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ea9b9-109">Das Cmdlet " **Restore-AzKeyVaultSecret** " erstellt im angegebenen schlüsseltresor ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="ea9b9-110">Dieser Geheimtipp ist eine Replik des gesicherten Geheimnisses in der Eingabedatei und hat denselben Namen wie der ursprüngliche Secret-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="ea9b9-111">Wenn der schlüsseltresor bereits über ein Kennwort mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Kennwort zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="ea9b9-112">Wenn die Sicherung mehrere Versionen eines Geheimnisses enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="ea9b9-113">Der schlüsseltresor, in den Sie den geheimen Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="ea9b9-114">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="ea9b9-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ea9b9-115">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ea9b9-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea9b9-116">EXAMPLES</span></span>

### <span data-ttu-id="ea9b9-117">Beispiel 1: Wiederherstellen eines gesicherten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="ea9b9-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="ea9b9-118">Mit diesem Befehl wird ein geheimer, einschließlich aller seiner Versionen, aus der Sicherungsdatei "Backup. BLOB" in den schlüsseltresor mit dem Namen "Contoso" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="ea9b9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea9b9-119">PARAMETERS</span></span>

### <span data-ttu-id="ea9b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9b9-120">-DefaultProfile</span></span>
<span data-ttu-id="ea9b9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea9b9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9b9-122">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="ea9b9-122">-InputFile</span></span>
<span data-ttu-id="ea9b9-123">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="ea9b9-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea9b9-124">-InputObject</span></span>
<span data-ttu-id="ea9b9-125">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="ea9b9-125">KeyVault object</span></span>

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

### <span data-ttu-id="ea9b9-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea9b9-126">-ResourceId</span></span>
<span data-ttu-id="ea9b9-127">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ea9b9-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ea9b9-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ea9b9-128">-VaultName</span></span>
<span data-ttu-id="ea9b9-129">Gibt den Namen des Schlüssel Tresors an, in den das Geheimnis wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="ea9b9-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea9b9-130">-Confirm</span></span>
<span data-ttu-id="ea9b9-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9b9-132">-WhatIf</span></span>
<span data-ttu-id="ea9b9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9b9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9b9-135">CommonParameters</span></span>
<span data-ttu-id="ea9b9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9b9-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9b9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9b9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea9b9-138">INPUTS</span></span>

### <span data-ttu-id="ea9b9-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ea9b9-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ea9b9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ea9b9-140">System.String</span></span>

## <span data-ttu-id="ea9b9-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea9b9-141">OUTPUTS</span></span>

### <span data-ttu-id="ea9b9-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ea9b9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea9b9-143">NOTES</span></span>

## <span data-ttu-id="ea9b9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea9b9-144">RELATED LINKS</span></span>

[<span data-ttu-id="ea9b9-145">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="ea9b9-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="ea9b9-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="ea9b9-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea9b9-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

