---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179524"
---
# <span data-ttu-id="15c5e-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c5e-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="15c5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="15c5e-103">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="15c5e-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="15c5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15c5e-104">SYNTAX</span></span>

### <span data-ttu-id="15c5e-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="15c5e-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c5e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c5e-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c5e-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="15c5e-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15c5e-108">DESCRIPTION</span></span>
<span data-ttu-id="15c5e-109">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="15c5e-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="15c5e-110">So können beispielsweise Cloud-Tiering-und Cloud-Tiering-Richtlinien jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="15c5e-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="15c5e-111">Nach dem Erstellen des Server Endpunkts können verschiedene Aspekte eines Server Endpunkts, beispielsweise des lokalen Pfads, nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="15c5e-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="15c5e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15c5e-112">EXAMPLES</span></span>

### <span data-ttu-id="15c5e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15c5e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="15c5e-114">In diesem Beispiel werden zwei Aktionen ausgeführt, und es wird eine neue Richtlinie für die Cloud-tierung auf dem angegebenen Serverendpunkt festgelegt, die den Server an alle Dateien weiterleitet, auf die in den letzten 30 Tagen nicht zugegriffen wurde, und außerdem den Offline Datenübertragungsmodus deaktiviert, der während der Erstellung zunächst für diesen Serverendpunkt aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="15c5e-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="15c5e-115">Die Offline-Datenübertragung wird im Rahmen der Interoperabilität mit Massen Migrationsdiensten wie Azure Data Box verwendet.</span><span class="sxs-lookup"><span data-stu-id="15c5e-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="15c5e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="15c5e-116">PARAMETERS</span></span>

### <span data-ttu-id="15c5e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15c5e-117">-AsJob</span></span>
<span data-ttu-id="15c5e-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="15c5e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15c5e-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="15c5e-119">-CloudTiering</span></span>
<span data-ttu-id="15c5e-120">Cloud-Tiering-Parameter</span><span class="sxs-lookup"><span data-stu-id="15c5e-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="15c5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c5e-121">-DefaultProfile</span></span>
<span data-ttu-id="15c5e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15c5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c5e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15c5e-123">-InputObject</span></span>
<span data-ttu-id="15c5e-124">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="15c5e-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="15c5e-125">-Name</span></span>
<span data-ttu-id="15c5e-126">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15c5e-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="15c5e-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="15c5e-128">Daten Parameter für Cloud-seeddaten</span><span class="sxs-lookup"><span data-stu-id="15c5e-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="15c5e-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="15c5e-129">-localCacheMode</span></span>
<span data-ttu-id="15c5e-130">Parameter für lokalen Cachemodus</span><span class="sxs-lookup"><span data-stu-id="15c5e-130">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c5e-131">-ResourceGroupName</span></span>
<span data-ttu-id="15c5e-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15c5e-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15c5e-133">-ResourceId</span></span>
<span data-ttu-id="15c5e-134">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="15c5e-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="15c5e-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="15c5e-136">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="15c5e-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="15c5e-137">-SyncGroupName</span></span>
<span data-ttu-id="15c5e-138">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="15c5e-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="15c5e-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="15c5e-140">Statusdateien, die älter als Tag-Parameter sind</span><span class="sxs-lookup"><span data-stu-id="15c5e-140">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="15c5e-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="15c5e-142">Volumen freier Speicherplatz Prozent Parameter</span><span class="sxs-lookup"><span data-stu-id="15c5e-142">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c5e-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15c5e-143">-Confirm</span></span>
<span data-ttu-id="15c5e-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15c5e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c5e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c5e-145">-WhatIf</span></span>
<span data-ttu-id="15c5e-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15c5e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15c5e-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15c5e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c5e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c5e-148">CommonParameters</span></span>
<span data-ttu-id="15c5e-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c5e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c5e-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c5e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c5e-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15c5e-151">INPUTS</span></span>

### <span data-ttu-id="15c5e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="15c5e-152">System.String</span></span>

### <span data-ttu-id="15c5e-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c5e-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="15c5e-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15c5e-154">OUTPUTS</span></span>

### <span data-ttu-id="15c5e-155">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c5e-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="15c5e-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="15c5e-156">NOTES</span></span>

## <span data-ttu-id="15c5e-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15c5e-157">RELATED LINKS</span></span>
