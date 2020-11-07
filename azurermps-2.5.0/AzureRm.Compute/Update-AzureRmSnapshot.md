---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 2e8b538e9a6f5f9fce2fb768bc0c77d0c82c55f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850860"
---
# <span data-ttu-id="217e0-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="217e0-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="217e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="217e0-102">SYNOPSIS</span></span>
<span data-ttu-id="217e0-103">Aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="217e0-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="217e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="217e0-104">SYNTAX</span></span>

### <span data-ttu-id="217e0-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="217e0-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="217e0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="217e0-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="217e0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="217e0-107">DESCRIPTION</span></span>
<span data-ttu-id="217e0-108">Das Cmdlet **Update-AzureRmSnapshot** aktualisiert einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="217e0-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="217e0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="217e0-109">EXAMPLES</span></span>

### <span data-ttu-id="217e0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="217e0-110">Example 1</span></span>
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

<span data-ttu-id="217e0-111">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="217e0-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="217e0-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="217e0-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="217e0-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="217e0-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="217e0-114">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="217e0-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="217e0-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="217e0-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="217e0-116">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="217e0-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="217e0-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="217e0-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="217e0-118">Diese Befehle aktualisieren auch einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="217e0-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="217e0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="217e0-119">PARAMETERS</span></span>

### <span data-ttu-id="217e0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="217e0-120">-AsJob</span></span>
<span data-ttu-id="217e0-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="217e0-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="217e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217e0-122">-DefaultProfile</span></span>
<span data-ttu-id="217e0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="217e0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="217e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="217e0-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="217e0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="217e0-126">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="217e0-126">-Snapshot</span></span>
<span data-ttu-id="217e0-127">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="217e0-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="217e0-128">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="217e0-128">-SnapshotName</span></span>
<span data-ttu-id="217e0-129">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="217e0-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="217e0-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="217e0-130">-SnapshotUpdate</span></span>
<span data-ttu-id="217e0-131">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="217e0-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="217e0-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="217e0-132">-Confirm</span></span>
<span data-ttu-id="217e0-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="217e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="217e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="217e0-134">-WhatIf</span></span>
<span data-ttu-id="217e0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="217e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="217e0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="217e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="217e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217e0-137">CommonParameters</span></span>
<span data-ttu-id="217e0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217e0-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217e0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="217e0-140">INPUTS</span></span>

### <span data-ttu-id="217e0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="217e0-141">System.String</span></span>
<span data-ttu-id="217e0-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="217e0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="217e0-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="217e0-143">OUTPUTS</span></span>

### <span data-ttu-id="217e0-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="217e0-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="217e0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="217e0-145">NOTES</span></span>

## <span data-ttu-id="217e0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="217e0-146">RELATED LINKS</span></span>

