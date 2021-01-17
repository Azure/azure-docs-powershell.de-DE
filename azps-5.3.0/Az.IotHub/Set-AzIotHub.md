---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386601"
---
# <span data-ttu-id="8b6dd-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="8b6dd-101">Set-AzIotHub</span></span>

## <span data-ttu-id="8b6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6dd-103">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="8b6dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b6dd-104">SYNTAX</span></span>

### <span data-ttu-id="8b6dd-105">UpdateSku (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b6dd-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6dd-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="8b6dd-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b6dd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b6dd-112">DESCRIPTION</span></span>
<span data-ttu-id="8b6dd-113">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="8b6dd-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b6dd-114">EXAMPLES</span></span>

### <span data-ttu-id="8b6dd-115">Beispiel 1 Aktualisieren der SKU</span><span class="sxs-lookup"><span data-stu-id="8b6dd-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="8b6dd-116">Aktualisieren Sie die SKU auf S1 und die Einheiten für IotHub mit dem Namen "myiothub" auf 5.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8b6dd-117">Beispiel 2 Aktualisieren der Ereignishubeigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b6dd-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="8b6dd-118">Aktualisieren Sie die Aufbewahrungszeit der Telemetrie in Tagen auf 4 für IotHub namens "myiothub".</span><span class="sxs-lookup"><span data-stu-id="8b6dd-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8b6dd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b6dd-119">PARAMETERS</span></span>

### <span data-ttu-id="8b6dd-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="8b6dd-120">-CloudToDevice</span></span>
<span data-ttu-id="8b6dd-121">Die Eigenschaften für die Befehlswarteschlange "Von der Cloud zum Gerät".</span><span class="sxs-lookup"><span data-stu-id="8b6dd-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6dd-122">-DefaultProfile</span></span>
<span data-ttu-id="8b6dd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8b6dd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b6dd-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="8b6dd-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="8b6dd-125">Flag, das angibt, ob Benachrichtigungen für den Dateiupload aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="8b6dd-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="8b6dd-127">Aufbewahrungszeit in Tagen.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="8b6dd-128">-FallbackRoute</span></span>
<span data-ttu-id="8b6dd-129">Fallbackroute für Routing</span><span class="sxs-lookup"><span data-stu-id="8b6dd-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="8b6dd-130">-FileUploadContainerName</span></span>
<span data-ttu-id="8b6dd-131">Der Name des Containers, in den die Dateien hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="8b6dd-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="8b6dd-133">Die maximale Übermittlungsanzahl für Dateiuploadbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="8b6dd-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="8b6dd-135">Zeit zum Livewert für die Nachrichten in der Dateiuploadbenachrichtigungswarteschlange.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="8b6dd-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="8b6dd-137">Es ist an der Zeit, für den SAS-URI, der für den Dateiupload generiert wird, zu leben.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="8b6dd-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="8b6dd-139">Die Speicherverbindungszeichenfolge zum Hochladen der Dateien.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-140">-Name</span><span class="sxs-lookup"><span data-stu-id="8b6dd-140">-Name</span></span>
<span data-ttu-id="8b6dd-141">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="8b6dd-141">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6dd-142">-ResourceGroupName</span></span>
<span data-ttu-id="8b6dd-143">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8b6dd-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="8b6dd-144">-Routes</span></span>
<span data-ttu-id="8b6dd-145">Für Routing zu verwendende Routen</span><span class="sxs-lookup"><span data-stu-id="8b6dd-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8b6dd-146">-RoutingProperties</span></span>
<span data-ttu-id="8b6dd-147">Die Routingeigenschaften zum Weiterleiten von Nachrichten an externe Endpunkte</span><span class="sxs-lookup"><span data-stu-id="8b6dd-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8b6dd-148">-SkuName</span></span>
<span data-ttu-id="8b6dd-149">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-150">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="8b6dd-150">-Units</span></span>
<span data-ttu-id="8b6dd-151">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="8b6dd-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b6dd-152">-Confirm</span></span>
<span data-ttu-id="8b6dd-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8b6dd-154">-WhatIf</span></span>
<span data-ttu-id="8b6dd-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6dd-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6dd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6dd-157">CommonParameters</span></span>
<span data-ttu-id="8b6dd-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6dd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6dd-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b6dd-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6dd-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b6dd-160">INPUTS</span></span>

### <span data-ttu-id="8b6dd-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8b6dd-161">System.String</span></span>

## <span data-ttu-id="8b6dd-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b6dd-162">OUTPUTS</span></span>

### <span data-ttu-id="8b6dd-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8b6dd-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="8b6dd-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b6dd-164">NOTES</span></span>

## <span data-ttu-id="8b6dd-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b6dd-165">RELATED LINKS</span></span>
