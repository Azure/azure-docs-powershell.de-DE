---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997265"
---
# <span data-ttu-id="c0770-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0770-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="c0770-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0770-102">SYNOPSIS</span></span>
<span data-ttu-id="c0770-103">Aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="c0770-103">Updates a snapshot.</span></span>

## <span data-ttu-id="c0770-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0770-104">SYNTAX</span></span>

### <span data-ttu-id="c0770-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0770-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0770-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c0770-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0770-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0770-107">DESCRIPTION</span></span>
<span data-ttu-id="c0770-108">Das Cmdlet **Update-AzSnapshot** aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="c0770-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="c0770-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0770-109">EXAMPLES</span></span>

### <span data-ttu-id="c0770-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0770-110">Example 1</span></span>
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

<span data-ttu-id="c0770-111">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0770-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c0770-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c0770-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c0770-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="c0770-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="c0770-114">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c0770-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c0770-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c0770-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="c0770-116">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c0770-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="c0770-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c0770-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="c0770-118">Diese Befehle aktualisieren auch einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="c0770-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="c0770-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0770-119">PARAMETERS</span></span>

### <span data-ttu-id="c0770-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0770-120">-AsJob</span></span>
<span data-ttu-id="c0770-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="c0770-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0770-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0770-122">-DefaultProfile</span></span>
<span data-ttu-id="c0770-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0770-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0770-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0770-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0770-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c0770-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c0770-126">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="c0770-126">-Snapshot</span></span>
<span data-ttu-id="c0770-127">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c0770-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="c0770-128">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="c0770-128">-SnapshotName</span></span>
<span data-ttu-id="c0770-129">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="c0770-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c0770-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c0770-130">-SnapshotUpdate</span></span>
<span data-ttu-id="c0770-131">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="c0770-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="c0770-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0770-132">-Confirm</span></span>
<span data-ttu-id="c0770-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0770-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0770-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0770-134">-WhatIf</span></span>
<span data-ttu-id="c0770-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0770-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0770-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0770-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0770-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0770-137">CommonParameters</span></span>
<span data-ttu-id="c0770-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0770-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0770-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0770-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0770-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0770-140">INPUTS</span></span>

### <span data-ttu-id="c0770-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c0770-141">System.String</span></span>

### <span data-ttu-id="c0770-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c0770-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="c0770-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0770-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c0770-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0770-144">OUTPUTS</span></span>

### <span data-ttu-id="c0770-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0770-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c0770-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0770-146">NOTES</span></span>

## <span data-ttu-id="c0770-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0770-147">RELATED LINKS</span></span>
