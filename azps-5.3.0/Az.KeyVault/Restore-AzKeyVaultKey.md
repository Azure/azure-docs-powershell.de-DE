---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458312"
---
# <span data-ttu-id="3e137-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="3e137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e137-102">SYNOPSIS</span></span>
<span data-ttu-id="3e137-103">Erstellt einen Schlüssel in einem Schlüsseltresor aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3e137-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="3e137-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e137-104">SYNTAX</span></span>

### <span data-ttu-id="3e137-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e137-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e137-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="3e137-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e137-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e137-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e137-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e137-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e137-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e137-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e137-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e137-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e137-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e137-111">DESCRIPTION</span></span>
<span data-ttu-id="3e137-112">Das **Cmdlet "Restore-AzKeyVaultKey"** erstellt einen Schlüssel im angegebenen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3e137-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="3e137-113">Dieser Schlüssel ist eine Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3e137-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="3e137-114">Wenn der Schlüsseltresor bereits einen Schlüssel mit demselben Namen besitzt, schlägt dieses Cmdlet fehl, statt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3e137-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="3e137-115">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="3e137-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="3e137-116">Der Schlüsseltresor, in dem Sie den Schlüssel wiederherstellen, kann sich vom Schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="3e137-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="3e137-117">Der Schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einer Azure-Region in derselben Geografie (z. B. Nordamerika) befinden.</span><span class="sxs-lookup"><span data-stu-id="3e137-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="3e137-118">Informationen zur Zuordnung von Azure-Regionen zu Regionen finden Sie im Microsoft Azure Trust https://azure.microsoft.com/support/trust-center/) Center.</span><span class="sxs-lookup"><span data-stu-id="3e137-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="3e137-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e137-119">EXAMPLES</span></span>

### <span data-ttu-id="3e137-120">Beispiel 1: Wiederherstellen eines gesicherten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3e137-120">Example 1: Restore a backed-up key</span></span>
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

<span data-ttu-id="3e137-121">Mit diesem Befehl wird ein Schlüssel einschließlich aller Versionen aus der Sicherungsdatei "Backup.blob" im Schlüsseltresor namens "MyKeyVault" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="3e137-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="3e137-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e137-122">PARAMETERS</span></span>

### <span data-ttu-id="3e137-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e137-123">-DefaultProfile</span></span>
<span data-ttu-id="3e137-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3e137-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e137-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3e137-125">-HsmName</span></span>
<span data-ttu-id="3e137-126">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="3e137-126">HSM name.</span></span> <span data-ttu-id="3e137-127">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3e137-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e137-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="3e137-128">-HsmObject</span></span>
<span data-ttu-id="3e137-129">HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="3e137-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e137-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="3e137-130">-HsmResourceId</span></span>
<span data-ttu-id="3e137-131">Hsm Resource Id</span><span class="sxs-lookup"><span data-stu-id="3e137-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e137-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3e137-132">-InputFile</span></span>
<span data-ttu-id="3e137-133">Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="3e137-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="3e137-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e137-134">-InputObject</span></span>
<span data-ttu-id="3e137-135">KeyVault-Objekt</span><span class="sxs-lookup"><span data-stu-id="3e137-135">KeyVault object</span></span>

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

### <span data-ttu-id="3e137-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e137-136">-ResourceId</span></span>
<span data-ttu-id="3e137-137">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="3e137-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="3e137-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e137-138">-VaultName</span></span>
<span data-ttu-id="3e137-139">Gibt den Namen des Schlüsseltresor an, in den der Schlüssel wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e137-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="3e137-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e137-140">-Confirm</span></span>
<span data-ttu-id="3e137-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e137-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e137-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3e137-142">-WhatIf</span></span>
<span data-ttu-id="3e137-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e137-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e137-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e137-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e137-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e137-145">CommonParameters</span></span>
<span data-ttu-id="3e137-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e137-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e137-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e137-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e137-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e137-148">INPUTS</span></span>

### <span data-ttu-id="3e137-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3e137-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3e137-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3e137-150">System.String</span></span>

## <span data-ttu-id="3e137-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e137-151">OUTPUTS</span></span>

### <span data-ttu-id="3e137-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="3e137-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3e137-153">NOTES</span></span>

## <span data-ttu-id="3e137-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3e137-154">RELATED LINKS</span></span>

[<span data-ttu-id="3e137-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="3e137-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="3e137-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="3e137-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e137-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

