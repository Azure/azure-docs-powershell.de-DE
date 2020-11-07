---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: bcdcda3015c3d6f7e255b8b2778b69254b031cc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650856"
---
# <span data-ttu-id="dbebe-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="dbebe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbebe-102">SYNOPSIS</span></span>
<span data-ttu-id="dbebe-103">Erstellt einen Schlüssel in einem schlüsseltresor aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="dbebe-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="dbebe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbebe-104">SYNTAX</span></span>

### <span data-ttu-id="dbebe-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbebe-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbebe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dbebe-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbebe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbebe-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbebe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbebe-108">DESCRIPTION</span></span>
<span data-ttu-id="dbebe-109">Das Cmdlet **Restore-AzKeyVaultKey** erstellt einen Schlüssel im angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="dbebe-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="dbebe-110">Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="dbebe-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="dbebe-111">Wenn der schlüsseltresor bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="dbebe-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="dbebe-112">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="dbebe-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="dbebe-113">Der schlüsseltresor, in den Sie den Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="dbebe-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="dbebe-114">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="dbebe-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="dbebe-115">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="dbebe-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="dbebe-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbebe-116">EXAMPLES</span></span>

### <span data-ttu-id="dbebe-117">Beispiel 1: Wiederherstellen eines gesicherten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="dbebe-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="dbebe-118">Mit diesem Befehl wird ein Schlüssel, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="dbebe-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="dbebe-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbebe-119">PARAMETERS</span></span>

### <span data-ttu-id="dbebe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbebe-120">-DefaultProfile</span></span>
<span data-ttu-id="dbebe-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dbebe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbebe-122">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="dbebe-122">-InputFile</span></span>
<span data-ttu-id="dbebe-123">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="dbebe-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="dbebe-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbebe-124">-InputObject</span></span>
<span data-ttu-id="dbebe-125">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="dbebe-125">KeyVault object</span></span>

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

### <span data-ttu-id="dbebe-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dbebe-126">-ResourceId</span></span>
<span data-ttu-id="dbebe-127">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dbebe-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="dbebe-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="dbebe-128">-VaultName</span></span>
<span data-ttu-id="dbebe-129">Gibt den Namen des Schlüssel Tresors an, in den der Schlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbebe-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="dbebe-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbebe-130">-Confirm</span></span>
<span data-ttu-id="dbebe-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbebe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbebe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbebe-132">-WhatIf</span></span>
<span data-ttu-id="dbebe-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbebe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbebe-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbebe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbebe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbebe-135">CommonParameters</span></span>
<span data-ttu-id="dbebe-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbebe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbebe-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbebe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbebe-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbebe-138">INPUTS</span></span>

### <span data-ttu-id="dbebe-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dbebe-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="dbebe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dbebe-140">System.String</span></span>

## <span data-ttu-id="dbebe-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbebe-141">OUTPUTS</span></span>

### <span data-ttu-id="dbebe-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="dbebe-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbebe-143">NOTES</span></span>

## <span data-ttu-id="dbebe-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbebe-144">RELATED LINKS</span></span>

[<span data-ttu-id="dbebe-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="dbebe-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="dbebe-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="dbebe-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dbebe-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

