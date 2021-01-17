---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460103"
---
# <span data-ttu-id="4e5f6-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5f6-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="4e5f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5f6-103">Mit diesem Befehl wird der angegebene Cloudendpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4e5f6-104">Ohne mindestens einen Cloudendpunkt können keine anderen Serverendpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="4e5f6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e5f6-105">SYNTAX</span></span>

### <span data-ttu-id="4e5f6-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e5f6-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5f6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e5f6-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5f6-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e5f6-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5f6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e5f6-109">DESCRIPTION</span></span>
<span data-ttu-id="4e5f6-110">Mit diesem Befehl wird der angegebene Cloudendpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="4e5f6-111">Die Verweise auf den Cloudendpunkt werden von diesem Prozess nicht für die Freigabe der Azure-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="4e5f6-112">Dieser Befehl ist nur für die Außerbetriebnahme vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="4e5f6-113">Das Entfernen eines Cloudendpunkts ist ein truktiver Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="4e5f6-114">Serverendpunkte können nur synchronisiert werden, wenn mindestens ein Cloudendpunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="4e5f6-115">Dieser Vorgang sollte nicht zum Beheben von Synchronisierungsproblemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="4e5f6-116">Wenn diese Azure-Dateifreigabe erneut derselben Synchronisierungsgruppe hinzugefügt wird, wie es ein Cloudendpunkt ist, kann sie zu Konfliktdateien und anderen unbeabsichtigten Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="4e5f6-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e5f6-117">EXAMPLES</span></span>

### <span data-ttu-id="4e5f6-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e5f6-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="4e5f6-119">Mit diesem Befehl wird der Cloudendpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="4e5f6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e5f6-120">PARAMETERS</span></span>

### <span data-ttu-id="4e5f6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e5f6-121">-AsJob</span></span>
<span data-ttu-id="4e5f6-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4e5f6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e5f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5f6-123">-DefaultProfile</span></span>
<span data-ttu-id="4e5f6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e5f6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4e5f6-125">-Force</span></span>
<span data-ttu-id="4e5f6-126">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="4e5f6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e5f6-127">-InputObject</span></span>
<span data-ttu-id="4e5f6-128">CloudEndpoint-Eingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e5f6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4e5f6-129">-Name</span></span>
<span data-ttu-id="4e5f6-130">Der Name von CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="4e5f6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e5f6-131">-PassThru</span></span>
<span data-ttu-id="4e5f6-132">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4e5f6-133">Wenn Sie den Parameter "PassThru" angeben, schreibt das Cmdlet nach erfolgreicher Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4e5f6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5f6-134">-ResourceGroupName</span></span>
<span data-ttu-id="4e5f6-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e5f6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5f6-136">-ResourceId</span></span>
<span data-ttu-id="4e5f6-137">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4e5f6-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4e5f6-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4e5f6-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="4e5f6-139">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4e5f6-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5f6-140">-SyncGroupName</span></span>
<span data-ttu-id="4e5f6-141">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="4e5f6-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e5f6-142">-Confirm</span></span>
<span data-ttu-id="4e5f6-143">Fordert vor dem Ausführen des Cmdlets zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5f6-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4e5f6-144">-WhatIf</span></span>
<span data-ttu-id="4e5f6-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e5f6-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5f6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5f6-147">CommonParameters</span></span>
<span data-ttu-id="4e5f6-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5f6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5f6-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5f6-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5f6-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e5f6-150">INPUTS</span></span>

### <span data-ttu-id="4e5f6-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5f6-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="4e5f6-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4e5f6-152">System.String</span></span>

## <span data-ttu-id="4e5f6-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e5f6-153">OUTPUTS</span></span>

### <span data-ttu-id="4e5f6-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e5f6-154">System.Object</span></span>
## <span data-ttu-id="4e5f6-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e5f6-155">NOTES</span></span>

## <span data-ttu-id="4e5f6-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e5f6-156">RELATED LINKS</span></span>
