---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 65df82b189442a32738e445a1b48093c18816bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929616"
---
# <span data-ttu-id="e6515-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6515-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="e6515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6515-102">SYNOPSIS</span></span>
<span data-ttu-id="e6515-103">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="e6515-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="e6515-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6515-104">SYNTAX</span></span>

### <span data-ttu-id="e6515-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6515-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6515-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6515-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6515-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6515-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6515-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6515-108">DESCRIPTION</span></span>
<span data-ttu-id="e6515-109">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="e6515-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="e6515-110">Beispielsweise können Richtlinien für Cloud tiering und cloud tiering jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e6515-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="e6515-111">Mehrere Aspekte eines Serverendpunkts, z. B. der lokale Pfad, können nach dem Erstellen des Serverendpunkts nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e6515-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="e6515-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6515-112">EXAMPLES</span></span>

### <span data-ttu-id="e6515-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6515-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="e6515-114">In diesem Beispiel werden zwei Aktionen ausgeführt, es legt eine neue Cloud tiering-Richtlinie für den angegebenen Serverendpunkt fest. Dadurch wird der Server dazu geleitet, alle Dateien zu stufen, auf die in den letzten 30 Tagen nicht zugegriffen wurde, und es deaktiviert außerdem den Offlinedatenübertragungsmodus, der während der Erstellung für diesen Serverendpunkt anfänglich aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="e6515-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="e6515-115">Die Offlinedatenübertragung wird als Teil der Interoperabilität mit Massenmigrationsdiensten wie Azure Data Box verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6515-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="e6515-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e6515-116">PARAMETERS</span></span>

### <span data-ttu-id="e6515-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6515-117">-AsJob</span></span>
<span data-ttu-id="e6515-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e6515-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6515-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="e6515-119">-CloudTiering</span></span>
<span data-ttu-id="e6515-120">Parameter "Cloud tiering"</span><span class="sxs-lookup"><span data-stu-id="e6515-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="e6515-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6515-121">-DefaultProfile</span></span>
<span data-ttu-id="e6515-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6515-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6515-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6515-123">-InputObject</span></span>
<span data-ttu-id="e6515-124">SyncGroup-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6515-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e6515-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e6515-125">-Name</span></span>
<span data-ttu-id="e6515-126">Name des ServerEndpoints.</span><span class="sxs-lookup"><span data-stu-id="e6515-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="e6515-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="e6515-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="e6515-128">Parameter "Cloud Seeded Data"</span><span class="sxs-lookup"><span data-stu-id="e6515-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="e6515-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="e6515-129">-localCacheMode</span></span>
<span data-ttu-id="e6515-130">Parameter für den lokalen Cachemodus</span><span class="sxs-lookup"><span data-stu-id="e6515-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="e6515-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6515-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6515-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e6515-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="e6515-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6515-133">-ResourceId</span></span>
<span data-ttu-id="e6515-134">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e6515-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="e6515-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e6515-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="e6515-136">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e6515-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e6515-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e6515-137">-SyncGroupName</span></span>
<span data-ttu-id="e6515-138">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e6515-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="e6515-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e6515-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="e6515-140">Parameter "Tier Files Older Than Days"</span><span class="sxs-lookup"><span data-stu-id="e6515-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="e6515-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="e6515-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="e6515-142">Parameter "Volume Free Space Percent"</span><span class="sxs-lookup"><span data-stu-id="e6515-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="e6515-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6515-143">-Confirm</span></span>
<span data-ttu-id="e6515-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6515-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6515-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6515-145">-WhatIf</span></span>
<span data-ttu-id="e6515-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6515-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6515-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6515-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6515-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6515-148">CommonParameters</span></span>
<span data-ttu-id="e6515-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6515-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6515-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6515-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6515-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6515-151">INPUTS</span></span>

### <span data-ttu-id="e6515-152">System.String</span><span class="sxs-lookup"><span data-stu-id="e6515-152">System.String</span></span>

### <span data-ttu-id="e6515-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6515-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e6515-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6515-154">OUTPUTS</span></span>

### <span data-ttu-id="e6515-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6515-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e6515-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e6515-156">NOTES</span></span>

## <span data-ttu-id="e6515-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e6515-157">RELATED LINKS</span></span>
