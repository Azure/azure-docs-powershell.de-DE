---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 90c61e97821b8caebf9c3f5b84da0b13db2e36b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003378"
---
# <span data-ttu-id="586ea-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="586ea-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="586ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="586ea-102">SYNOPSIS</span></span>
<span data-ttu-id="586ea-103">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="586ea-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="586ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="586ea-104">SYNTAX</span></span>

### <span data-ttu-id="586ea-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="586ea-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586ea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="586ea-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586ea-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="586ea-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="586ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="586ea-108">DESCRIPTION</span></span>
<span data-ttu-id="586ea-109">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="586ea-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="586ea-110">So können beispielsweise Cloud-Tiering-und Cloud-Tiering-Richtlinien jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="586ea-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="586ea-111">Nach dem Erstellen des Server Endpunkts können verschiedene Aspekte eines Server Endpunkts, beispielsweise des lokalen Pfads, nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="586ea-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="586ea-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="586ea-112">EXAMPLES</span></span>

### <span data-ttu-id="586ea-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="586ea-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="586ea-114">In diesem Beispiel werden zwei Aktionen ausgeführt, und es wird eine neue Richtlinie für die Cloud-tierung auf dem angegebenen Serverendpunkt festgelegt, die den Server an alle Dateien weiterleitet, auf die in den letzten 30 Tagen nicht zugegriffen wurde, und außerdem den Offline Datenübertragungsmodus deaktiviert, der während der Erstellung zunächst für diesen Serverendpunkt aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="586ea-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="586ea-115">Die Offline-Datenübertragung wird im Rahmen der Interoperabilität mit Massen Migrationsdiensten wie Azure Data Box verwendet.</span><span class="sxs-lookup"><span data-stu-id="586ea-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="586ea-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="586ea-116">PARAMETERS</span></span>

### <span data-ttu-id="586ea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="586ea-117">-AsJob</span></span>
<span data-ttu-id="586ea-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="586ea-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="586ea-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="586ea-119">-CloudTiering</span></span>
<span data-ttu-id="586ea-120">Cloud-Tiering-Parameter</span><span class="sxs-lookup"><span data-stu-id="586ea-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="586ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586ea-121">-DefaultProfile</span></span>
<span data-ttu-id="586ea-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="586ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="586ea-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="586ea-123">-InputObject</span></span>
<span data-ttu-id="586ea-124">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="586ea-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="586ea-125">-Name</span><span class="sxs-lookup"><span data-stu-id="586ea-125">-Name</span></span>
<span data-ttu-id="586ea-126">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="586ea-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="586ea-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="586ea-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="586ea-128">Daten Parameter für Cloud-seeddaten</span><span class="sxs-lookup"><span data-stu-id="586ea-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="586ea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586ea-129">-ResourceGroupName</span></span>
<span data-ttu-id="586ea-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="586ea-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="586ea-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="586ea-131">-ResourceId</span></span>
<span data-ttu-id="586ea-132">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="586ea-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="586ea-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="586ea-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="586ea-134">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="586ea-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="586ea-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="586ea-135">-SyncGroupName</span></span>
<span data-ttu-id="586ea-136">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="586ea-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="586ea-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="586ea-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="586ea-138">Statusdateien, die älter als Tag-Parameter sind</span><span class="sxs-lookup"><span data-stu-id="586ea-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="586ea-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="586ea-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="586ea-140">Volumen freier Speicherplatz Prozent Parameter</span><span class="sxs-lookup"><span data-stu-id="586ea-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="586ea-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="586ea-141">-Confirm</span></span>
<span data-ttu-id="586ea-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="586ea-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="586ea-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="586ea-143">-WhatIf</span></span>
<span data-ttu-id="586ea-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="586ea-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="586ea-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="586ea-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="586ea-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586ea-146">CommonParameters</span></span>
<span data-ttu-id="586ea-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586ea-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586ea-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="586ea-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586ea-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="586ea-149">INPUTS</span></span>

### <span data-ttu-id="586ea-150">System. String</span><span class="sxs-lookup"><span data-stu-id="586ea-150">System.String</span></span>

### <span data-ttu-id="586ea-151">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="586ea-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="586ea-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="586ea-152">OUTPUTS</span></span>

### <span data-ttu-id="586ea-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="586ea-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="586ea-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="586ea-154">NOTES</span></span>

## <span data-ttu-id="586ea-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="586ea-155">RELATED LINKS</span></span>
