---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 53b27c8144e0016962584baf40543dddf70b7bf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928315"
---
# <span data-ttu-id="b533c-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b533c-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="b533c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b533c-102">SYNOPSIS</span></span>
<span data-ttu-id="b533c-103">Aktualisiert eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="b533c-103">Updates a snapshot.</span></span>

## <span data-ttu-id="b533c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b533c-104">SYNTAX</span></span>

### <span data-ttu-id="b533c-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b533c-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b533c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b533c-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b533c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b533c-107">DESCRIPTION</span></span>
<span data-ttu-id="b533c-108">Das **Cmdlet Update-AzSnapshot** aktualisiert eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="b533c-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b533c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b533c-109">EXAMPLES</span></span>

### <span data-ttu-id="b533c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b533c-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="b533c-111">Mit dem ersten Befehl wird ein lokales leeres Snapshotupdateobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="b533c-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b533c-112">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b533c-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b533c-113">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Snapshotupdateobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b533c-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b533c-114">Der letzte Befehl übernimmt das Snapshotupdateobjekt und aktualisiert eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b533c-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b533c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b533c-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b533c-116">Mit diesem Befehl wird eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b533c-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b533c-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b533c-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b533c-118">Mit diesen Befehlen wird auch eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b533c-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b533c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b533c-119">PARAMETERS</span></span>

### <span data-ttu-id="b533c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b533c-120">-AsJob</span></span>
<span data-ttu-id="b533c-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b533c-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b533c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b533c-122">-DefaultProfile</span></span>
<span data-ttu-id="b533c-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b533c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b533c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b533c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b533c-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b533c-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b533c-126">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="b533c-126">-Snapshot</span></span>
<span data-ttu-id="b533c-127">Gibt ein lokales Snapshotobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b533c-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b533c-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b533c-128">-SnapshotName</span></span>
<span data-ttu-id="b533c-129">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="b533c-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b533c-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b533c-130">-SnapshotUpdate</span></span>
<span data-ttu-id="b533c-131">Gibt ein lokales Snapshotupdateobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b533c-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b533c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b533c-132">-Confirm</span></span>
<span data-ttu-id="b533c-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b533c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b533c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b533c-134">-WhatIf</span></span>
<span data-ttu-id="b533c-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b533c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b533c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b533c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b533c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b533c-137">CommonParameters</span></span>
<span data-ttu-id="b533c-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b533c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b533c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b533c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b533c-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b533c-140">INPUTS</span></span>

### <span data-ttu-id="b533c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b533c-141">System.String</span></span>

### <span data-ttu-id="b533c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b533c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b533c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b533c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b533c-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b533c-144">OUTPUTS</span></span>

### <span data-ttu-id="b533c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b533c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b533c-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b533c-146">NOTES</span></span>

## <span data-ttu-id="b533c-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b533c-147">RELATED LINKS</span></span>
