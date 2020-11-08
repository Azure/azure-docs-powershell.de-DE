---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166739"
---
# <span data-ttu-id="4b965-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b965-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="4b965-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b965-102">SYNOPSIS</span></span>
<span data-ttu-id="4b965-103">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4b965-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4b965-104">Ohne mindestens einen Cloud-Endpunkt können keine anderen Server Endpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b965-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="4b965-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b965-105">SYNTAX</span></span>

### <span data-ttu-id="4b965-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b965-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b965-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b965-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b965-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b965-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b965-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b965-109">DESCRIPTION</span></span>
<span data-ttu-id="4b965-110">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4b965-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4b965-111">Die Azure-Dateifreigabe die Verweise auf den cloudbasierten Endpunkt bleiben durch diesen Prozess unberührt.</span><span class="sxs-lookup"><span data-stu-id="4b965-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="4b965-112">Dieser Befehl ist nur für die Außerbetriebnahme vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4b965-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="4b965-113">Das Entfernen eines Cloud-Endpunkts ist ein zerstörerischer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4b965-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="4b965-114">Server Endpunkte können nicht synchronisiert werden, ohne dass mindestens ein Cloud-Endpunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4b965-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="4b965-115">Dieser Vorgang sollte nicht zum Beheben von Synchronisierungsproblemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4b965-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="4b965-116">Wenn diese Azure-Dateifreigabe erneut zur gleichen Synchronisierungsgruppe wie ein Cloud-Endpunkt hinzugefügt wird, kann dies zu Konfliktdateien und anderen unbeabsichtigten Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="4b965-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="4b965-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b965-117">EXAMPLES</span></span>

### <span data-ttu-id="4b965-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b965-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="4b965-119">Mit diesem Befehl wird der Cloud-Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b965-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="4b965-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b965-120">PARAMETERS</span></span>

### <span data-ttu-id="4b965-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b965-121">-AsJob</span></span>
<span data-ttu-id="4b965-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4b965-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b965-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b965-123">-DefaultProfile</span></span>
<span data-ttu-id="4b965-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b965-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b965-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4b965-125">-Force</span></span>
<span data-ttu-id="4b965-126">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="4b965-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4b965-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b965-127">-InputObject</span></span>
<span data-ttu-id="4b965-128">CloudEndpoint-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b965-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4b965-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4b965-129">-Name</span></span>
<span data-ttu-id="4b965-130">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b965-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="4b965-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b965-131">-PassThru</span></span>
<span data-ttu-id="4b965-132">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="4b965-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4b965-133">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b965-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4b965-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b965-134">-ResourceGroupName</span></span>
<span data-ttu-id="4b965-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b965-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b965-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4b965-136">-ResourceId</span></span>
<span data-ttu-id="4b965-137">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4b965-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4b965-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4b965-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="4b965-139">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4b965-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4b965-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4b965-140">-SyncGroupName</span></span>
<span data-ttu-id="4b965-141">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4b965-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4b965-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b965-142">-Confirm</span></span>
<span data-ttu-id="4b965-143">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b965-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b965-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b965-144">-WhatIf</span></span>
<span data-ttu-id="4b965-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b965-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b965-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b965-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b965-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b965-147">CommonParameters</span></span>
<span data-ttu-id="4b965-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b965-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b965-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b965-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b965-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b965-150">INPUTS</span></span>

### <span data-ttu-id="4b965-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b965-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="4b965-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4b965-152">System.String</span></span>

## <span data-ttu-id="4b965-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b965-153">OUTPUTS</span></span>

### <span data-ttu-id="4b965-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="4b965-154">System.Object</span></span>
## <span data-ttu-id="4b965-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b965-155">NOTES</span></span>

## <span data-ttu-id="4b965-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b965-156">RELATED LINKS</span></span>
