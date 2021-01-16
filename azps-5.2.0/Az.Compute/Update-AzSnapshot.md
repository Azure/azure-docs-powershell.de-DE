---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297598"
---
# <span data-ttu-id="b229e-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b229e-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="b229e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b229e-102">SYNOPSIS</span></span>
<span data-ttu-id="b229e-103">Aktualisiert eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="b229e-103">Updates a snapshot.</span></span>

## <span data-ttu-id="b229e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b229e-104">SYNTAX</span></span>

### <span data-ttu-id="b229e-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b229e-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b229e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b229e-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b229e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b229e-107">DESCRIPTION</span></span>
<span data-ttu-id="b229e-108">Das **Update-AzSnapshot-Cmdlet** aktualisiert eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="b229e-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b229e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b229e-109">EXAMPLES</span></span>

### <span data-ttu-id="b229e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b229e-110">Example 1</span></span>
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

<span data-ttu-id="b229e-111">Der erste Befehl erstellt ein lokales leeres Snapshotupdateobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="b229e-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b229e-112">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b229e-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b229e-113">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Snapshotupdateobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b229e-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b229e-114">Der letzte Befehl erstellt das Snapshotaktualisierungsobjekt und aktualisiert eine vorhandene Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="b229e-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b229e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b229e-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b229e-116">Mit diesem Befehl wird eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b229e-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b229e-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b229e-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b229e-118">Mit diesen Befehlen wird auch eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b229e-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b229e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b229e-119">PARAMETERS</span></span>

### <span data-ttu-id="b229e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b229e-120">-AsJob</span></span>
<span data-ttu-id="b229e-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="b229e-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b229e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b229e-122">-DefaultProfile</span></span>
<span data-ttu-id="b229e-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b229e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b229e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b229e-124">-ResourceGroupName</span></span>
<span data-ttu-id="b229e-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b229e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b229e-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="b229e-126">-Snapshot</span></span>
<span data-ttu-id="b229e-127">Gibt ein lokales Momentaufnahmeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b229e-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="b229e-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b229e-128">-SnapshotName</span></span>
<span data-ttu-id="b229e-129">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="b229e-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b229e-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b229e-130">-SnapshotUpdate</span></span>
<span data-ttu-id="b229e-131">Gibt ein lokales Snapshotaktualisierungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b229e-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="b229e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b229e-132">-Confirm</span></span>
<span data-ttu-id="b229e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b229e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b229e-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b229e-134">-WhatIf</span></span>
<span data-ttu-id="b229e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b229e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b229e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b229e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b229e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b229e-137">CommonParameters</span></span>
<span data-ttu-id="b229e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b229e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b229e-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b229e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b229e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b229e-140">INPUTS</span></span>

### <span data-ttu-id="b229e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b229e-141">System.String</span></span>

### <span data-ttu-id="b229e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b229e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b229e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b229e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b229e-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b229e-144">OUTPUTS</span></span>

### <span data-ttu-id="b229e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b229e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b229e-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b229e-146">NOTES</span></span>

## <span data-ttu-id="b229e-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b229e-147">RELATED LINKS</span></span>
