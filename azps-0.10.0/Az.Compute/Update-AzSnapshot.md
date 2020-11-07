---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: db26ee59bfeab521658d990836062da7dac594d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842439"
---
# <span data-ttu-id="18d13-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="18d13-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="18d13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18d13-102">SYNOPSIS</span></span>
<span data-ttu-id="18d13-103">Aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="18d13-103">Updates a snapshot.</span></span>

## <span data-ttu-id="18d13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18d13-104">SYNTAX</span></span>

### <span data-ttu-id="18d13-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="18d13-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18d13-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="18d13-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18d13-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18d13-107">DESCRIPTION</span></span>
<span data-ttu-id="18d13-108">Das Cmdlet **Update-AzSnapshot** aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="18d13-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="18d13-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18d13-109">EXAMPLES</span></span>

### <span data-ttu-id="18d13-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="18d13-110">Example 1</span></span>
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

<span data-ttu-id="18d13-111">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="18d13-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="18d13-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="18d13-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="18d13-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="18d13-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="18d13-114">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="18d13-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="18d13-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="18d13-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="18d13-116">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="18d13-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="18d13-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="18d13-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="18d13-118">Diese Befehle aktualisieren auch einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="18d13-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="18d13-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="18d13-119">PARAMETERS</span></span>

### <span data-ttu-id="18d13-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18d13-120">-AsJob</span></span>
<span data-ttu-id="18d13-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="18d13-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d13-122">-DefaultProfile</span></span>
<span data-ttu-id="18d13-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18d13-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18d13-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d13-124">-ResourceGroupName</span></span>
<span data-ttu-id="18d13-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="18d13-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18d13-126">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="18d13-126">-Snapshot</span></span>
<span data-ttu-id="18d13-127">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="18d13-127">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18d13-128">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="18d13-128">-SnapshotName</span></span>
<span data-ttu-id="18d13-129">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="18d13-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="18d13-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="18d13-130">-SnapshotUpdate</span></span>
<span data-ttu-id="18d13-131">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="18d13-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18d13-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18d13-132">-Confirm</span></span>
<span data-ttu-id="18d13-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18d13-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18d13-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18d13-134">-WhatIf</span></span>
<span data-ttu-id="18d13-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18d13-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18d13-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18d13-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18d13-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d13-137">CommonParameters</span></span>
<span data-ttu-id="18d13-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d13-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d13-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d13-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d13-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18d13-140">INPUTS</span></span>

### <span data-ttu-id="18d13-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18d13-141">System.String</span></span>
<span data-ttu-id="18d13-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="18d13-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="18d13-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18d13-143">OUTPUTS</span></span>

### <span data-ttu-id="18d13-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="18d13-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="18d13-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="18d13-145">NOTES</span></span>

## <span data-ttu-id="18d13-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18d13-146">RELATED LINKS</span></span>

