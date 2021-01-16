---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366553"
---
# <span data-ttu-id="25dcc-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25dcc-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="25dcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="25dcc-103">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="25dcc-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="25dcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25dcc-104">SYNTAX</span></span>

### <span data-ttu-id="25dcc-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25dcc-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25dcc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25dcc-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25dcc-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25dcc-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25dcc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25dcc-108">DESCRIPTION</span></span>
<span data-ttu-id="25dcc-109">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="25dcc-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="25dcc-110">Richtlinien für cloud tiering und cloud tiering können z. B. jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="25dcc-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="25dcc-111">Mehrere Aspekte eines Serverendpunkts, z. B. der lokale Pfad, können nach dem Erstellen des Serverendpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="25dcc-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="25dcc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25dcc-112">EXAMPLES</span></span>

### <span data-ttu-id="25dcc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25dcc-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="25dcc-114">In diesem Beispiel werden zwei Aktionen ausgeführt. Es legt eine neue Cloud tiering policy für den angegebenen Serverendpunkt fest, die den Server dazu bringt, alle Dateien, auf die in den letzten 30 Tagen nicht zugegriffen wurde, zu stufen, und es deaktiviert außerdem den Offlinedatenübertragungsmodus, der während seiner Erstellung auf diesem Serverendpunkt ursprünglich aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="25dcc-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="25dcc-115">Die Offlinedatenübertragung wird als Teil der Interoperabilität mit Massenmigrationsdiensten wie Azure Data Box verwendet.</span><span class="sxs-lookup"><span data-stu-id="25dcc-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="25dcc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25dcc-116">PARAMETERS</span></span>

### <span data-ttu-id="25dcc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25dcc-117">-AsJob</span></span>
<span data-ttu-id="25dcc-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25dcc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25dcc-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="25dcc-119">-CloudTiering</span></span>
<span data-ttu-id="25dcc-120">Cloud Tiering Parameter</span><span class="sxs-lookup"><span data-stu-id="25dcc-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="25dcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25dcc-121">-DefaultProfile</span></span>
<span data-ttu-id="25dcc-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25dcc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25dcc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25dcc-123">-InputObject</span></span>
<span data-ttu-id="25dcc-124">SyncGroup-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="25dcc-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="25dcc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="25dcc-125">-Name</span></span>
<span data-ttu-id="25dcc-126">Der Name von ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="25dcc-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="25dcc-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="25dcc-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="25dcc-128">Parameter für Daten mit Cloud-Startwert</span><span class="sxs-lookup"><span data-stu-id="25dcc-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="25dcc-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="25dcc-129">-localCacheMode</span></span>
<span data-ttu-id="25dcc-130">Parameter für den lokalen Cachemodus</span><span class="sxs-lookup"><span data-stu-id="25dcc-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="25dcc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25dcc-131">-ResourceGroupName</span></span>
<span data-ttu-id="25dcc-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="25dcc-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="25dcc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25dcc-133">-ResourceId</span></span>
<span data-ttu-id="25dcc-134">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="25dcc-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="25dcc-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="25dcc-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="25dcc-136">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="25dcc-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="25dcc-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="25dcc-137">-SyncGroupName</span></span>
<span data-ttu-id="25dcc-138">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="25dcc-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="25dcc-139">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="25dcc-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="25dcc-140">Parameter 'Dateien stufen, die älter als Tage' sind</span><span class="sxs-lookup"><span data-stu-id="25dcc-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="25dcc-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="25dcc-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="25dcc-142">Parameter "Volume Free Space Percent"</span><span class="sxs-lookup"><span data-stu-id="25dcc-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="25dcc-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25dcc-143">-Confirm</span></span>
<span data-ttu-id="25dcc-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25dcc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25dcc-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25dcc-145">-WhatIf</span></span>
<span data-ttu-id="25dcc-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25dcc-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25dcc-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25dcc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25dcc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dcc-148">CommonParameters</span></span>
<span data-ttu-id="25dcc-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25dcc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dcc-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25dcc-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dcc-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25dcc-151">INPUTS</span></span>

### <span data-ttu-id="25dcc-152">System.String</span><span class="sxs-lookup"><span data-stu-id="25dcc-152">System.String</span></span>

### <span data-ttu-id="25dcc-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25dcc-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="25dcc-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25dcc-154">OUTPUTS</span></span>

### <span data-ttu-id="25dcc-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25dcc-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="25dcc-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25dcc-156">NOTES</span></span>

## <span data-ttu-id="25dcc-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25dcc-157">RELATED LINKS</span></span>
