---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 2d9ad2417041f39ea43f48813310869f1ea7f353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658688"
---
# <span data-ttu-id="a56a9-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a56a9-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="a56a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a56a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a56a9-103">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a56a9-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="a56a9-104">Ohne mindestens einen Cloud-Endpunkt können keine anderen Server Endpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a56a9-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="a56a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a56a9-105">SYNTAX</span></span>

### <span data-ttu-id="a56a9-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a56a9-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a56a9-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a56a9-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a56a9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a56a9-109">DESCRIPTION</span></span>
<span data-ttu-id="a56a9-110">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a56a9-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="a56a9-111">Die Azure-Dateifreigabe die Verweise auf den cloudbasierten Endpunkt bleiben durch diesen Prozess unberührt.</span><span class="sxs-lookup"><span data-stu-id="a56a9-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="a56a9-112">Dieser Befehl ist nur für die Außerbetriebnahme vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a56a9-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="a56a9-113">Das Entfernen eines Cloud-Endpunkts ist ein zerstörerischer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a56a9-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="a56a9-114">Server Endpunkte können nicht synchronisiert werden, ohne dass mindestens ein Cloud-Endpunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a56a9-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="a56a9-115">Dieser Vorgang sollte nicht zum Beheben von Synchronisierungsproblemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a56a9-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="a56a9-116">Wenn diese Azure-Dateifreigabe erneut zur gleichen Synchronisierungsgruppe wie ein Cloud-Endpunkt hinzugefügt wird, kann dies zu Konfliktdateien und anderen unbeabsichtigten Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="a56a9-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="a56a9-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a56a9-117">EXAMPLES</span></span>

### <span data-ttu-id="a56a9-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a56a9-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="a56a9-119">Mit diesem Befehl wird der Cloud-Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a56a9-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="a56a9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56a9-120">PARAMETERS</span></span>

### <span data-ttu-id="a56a9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a56a9-121">-AsJob</span></span>
<span data-ttu-id="a56a9-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a56a9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a56a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a56a9-123">-DefaultProfile</span></span>
<span data-ttu-id="a56a9-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a56a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a56a9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a56a9-125">-Force</span></span>
<span data-ttu-id="a56a9-126">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="a56a9-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="a56a9-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a56a9-127">-InputObject</span></span>
<span data-ttu-id="a56a9-128">CloudEndpoint-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56a9-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a56a9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a56a9-129">-Name</span></span>
<span data-ttu-id="a56a9-130">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a56a9-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a56a9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a56a9-131">-PassThru</span></span>
<span data-ttu-id="a56a9-132">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a56a9-132">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a56a9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a56a9-133">-ResourceGroupName</span></span>
<span data-ttu-id="a56a9-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a56a9-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="a56a9-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a56a9-135">-ResourceId</span></span>
<span data-ttu-id="a56a9-136">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a56a9-136">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a56a9-137">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a56a9-137">-StorageSyncServiceName</span></span>
<span data-ttu-id="a56a9-138">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a56a9-138">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a56a9-139">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a56a9-139">-SyncGroupName</span></span>
<span data-ttu-id="a56a9-140">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="a56a9-140">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a56a9-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a56a9-141">-Confirm</span></span>
<span data-ttu-id="a56a9-142">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a56a9-142">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a56a9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a56a9-143">-WhatIf</span></span>
<span data-ttu-id="a56a9-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a56a9-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a56a9-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a56a9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a56a9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a56a9-146">CommonParameters</span></span>
<span data-ttu-id="a56a9-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a56a9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a56a9-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a56a9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a56a9-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a56a9-149">INPUTS</span></span>

### <span data-ttu-id="a56a9-150">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a56a9-150">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="a56a9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a56a9-151">System.String</span></span>

## <span data-ttu-id="a56a9-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a56a9-152">OUTPUTS</span></span>

### <span data-ttu-id="a56a9-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="a56a9-153">System.Object</span></span>
## <span data-ttu-id="a56a9-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="a56a9-154">NOTES</span></span>

## <span data-ttu-id="a56a9-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a56a9-155">RELATED LINKS</span></span>
