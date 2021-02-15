---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152756"
---
# <span data-ttu-id="6494a-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6494a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6494a-102">SYNOPSIS</span></span>
<span data-ttu-id="6494a-103">Erstellt einen Geheimschlüssel in einem Schlüsseltresor aus einem gesicherten Geheimschlüssel.</span><span class="sxs-lookup"><span data-stu-id="6494a-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="6494a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6494a-104">SYNTAX</span></span>

### <span data-ttu-id="6494a-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6494a-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6494a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6494a-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6494a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6494a-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6494a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6494a-108">DESCRIPTION</span></span>
<span data-ttu-id="6494a-109">Das **Cmdlet "Restore-AzKeyVaultSecret"** erstellt einen geheimen Schlüssel im angegebenen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="6494a-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="6494a-110">Dieses Geheimnis ist eine Replikate des gesicherten geheimen Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Geheime.</span><span class="sxs-lookup"><span data-stu-id="6494a-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="6494a-111">Wenn der Schlüsseltresor bereits einen geheimen Schlüssel mit demselben Namen hat, schlägt dieses Cmdlet fehl, statt den ursprünglichen Geheimschlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6494a-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="6494a-112">Wenn die Sicherung mehrere Versionen eines geheimen Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="6494a-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="6494a-113">Der Schlüsseltresor, in dem Sie das Geheimnis wiederherstellen, kann sich vom Schlüsseltresor unterscheiden, von dem Sie das Geheimnis gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="6494a-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="6494a-114">Der Schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einer Azure-Region in derselben Geografie (z. B. Nordamerika) befinden.</span><span class="sxs-lookup"><span data-stu-id="6494a-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6494a-115">Informationen zur Zuordnung von Azure-Regionen zu Regionen finden Sie im Microsoft Azure Trust https://azure.microsoft.com/support/trust-center/) Center.</span><span class="sxs-lookup"><span data-stu-id="6494a-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6494a-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6494a-116">EXAMPLES</span></span>

### <span data-ttu-id="6494a-117">Beispiel 1: Wiederherstellen eines gesicherten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6494a-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="6494a-118">Mit diesem Befehl wird ein Geheimschlüssel einschließlich aller Versionen aus der Sicherungsdatei mit dem Namen "Backup.blob" im Schlüsseltresor "contoso" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="6494a-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="6494a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6494a-119">PARAMETERS</span></span>

### <span data-ttu-id="6494a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6494a-120">-DefaultProfile</span></span>
<span data-ttu-id="6494a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6494a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6494a-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6494a-122">-InputFile</span></span>
<span data-ttu-id="6494a-123">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Geheim geheimen Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="6494a-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="6494a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6494a-124">-InputObject</span></span>
<span data-ttu-id="6494a-125">KeyVault-Objekt</span><span class="sxs-lookup"><span data-stu-id="6494a-125">KeyVault object</span></span>

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

### <span data-ttu-id="6494a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6494a-126">-ResourceId</span></span>
<span data-ttu-id="6494a-127">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="6494a-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="6494a-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6494a-128">-VaultName</span></span>
<span data-ttu-id="6494a-129">Gibt den Namen des Schlüsseltresor an, in den der Geheimschlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6494a-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="6494a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6494a-130">-Confirm</span></span>
<span data-ttu-id="6494a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6494a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6494a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6494a-132">-WhatIf</span></span>
<span data-ttu-id="6494a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6494a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6494a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6494a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6494a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6494a-135">CommonParameters</span></span>
<span data-ttu-id="6494a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6494a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6494a-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6494a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6494a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6494a-138">INPUTS</span></span>

### <span data-ttu-id="6494a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6494a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6494a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6494a-140">System.String</span></span>

## <span data-ttu-id="6494a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6494a-141">OUTPUTS</span></span>

### <span data-ttu-id="6494a-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6494a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6494a-143">NOTES</span></span>

## <span data-ttu-id="6494a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6494a-144">RELATED LINKS</span></span>

[<span data-ttu-id="6494a-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="6494a-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="6494a-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6494a-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6494a-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

