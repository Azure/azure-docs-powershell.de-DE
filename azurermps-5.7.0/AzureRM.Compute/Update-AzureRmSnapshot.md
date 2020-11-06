---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476893"
---
# <span data-ttu-id="def5d-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="def5d-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="def5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="def5d-102">SYNOPSIS</span></span>
<span data-ttu-id="def5d-103">Aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="def5d-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="def5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="def5d-104">SYNTAX</span></span>

### <span data-ttu-id="def5d-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="def5d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def5d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="def5d-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="def5d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="def5d-107">DESCRIPTION</span></span>
<span data-ttu-id="def5d-108">Das Cmdlet **Update-AzureRmSnapshot** aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="def5d-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="def5d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="def5d-109">EXAMPLES</span></span>

### <span data-ttu-id="def5d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="def5d-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="def5d-111">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="def5d-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="def5d-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="def5d-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="def5d-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="def5d-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="def5d-114">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="def5d-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="def5d-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="def5d-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="def5d-116">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="def5d-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="def5d-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="def5d-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="def5d-118">Diese Befehle aktualisieren auch einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="def5d-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="def5d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="def5d-119">PARAMETERS</span></span>

### <span data-ttu-id="def5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="def5d-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="def5d-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-122">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="def5d-122">-Snapshot</span></span>
<span data-ttu-id="def5d-123">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="def5d-123">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-124">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="def5d-124">-SnapshotName</span></span>
<span data-ttu-id="def5d-125">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="def5d-125">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-126">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="def5d-126">-SnapshotUpdate</span></span>
<span data-ttu-id="def5d-127">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="def5d-127">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="def5d-128">-Confirm</span></span>
<span data-ttu-id="def5d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="def5d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def5d-130">-WhatIf</span></span>
<span data-ttu-id="def5d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="def5d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def5d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="def5d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def5d-133">CommonParameters</span></span>
<span data-ttu-id="def5d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def5d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def5d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def5d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="def5d-136">INPUTS</span></span>

### <span data-ttu-id="def5d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="def5d-137">System.String</span></span>
<span data-ttu-id="def5d-138">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="def5d-138">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="def5d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="def5d-139">OUTPUTS</span></span>

### <span data-ttu-id="def5d-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="def5d-140">System.Object</span></span>

## <span data-ttu-id="def5d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="def5d-141">NOTES</span></span>

## <span data-ttu-id="def5d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="def5d-142">RELATED LINKS</span></span>

