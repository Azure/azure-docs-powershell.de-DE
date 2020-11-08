---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996119"
---
# <span data-ttu-id="7e394-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="7e394-101">Set-AzIotHub</span></span>

## <span data-ttu-id="7e394-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e394-102">SYNOPSIS</span></span>
<span data-ttu-id="7e394-103">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e394-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="7e394-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e394-104">SYNTAX</span></span>

### <span data-ttu-id="7e394-105">UpdateSku (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e394-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e394-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="7e394-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e394-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e394-112">DESCRIPTION</span></span>
<span data-ttu-id="7e394-113">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e394-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="7e394-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e394-114">EXAMPLES</span></span>

### <span data-ttu-id="7e394-115">Beispiel 1 Aktualisieren der SKU</span><span class="sxs-lookup"><span data-stu-id="7e394-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="7e394-116">Aktualisieren Sie die SKU auf S1 und die Einheiten auf 5 für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7e394-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="7e394-117">Beispiel 2 Aktualisieren der eventhub-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e394-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="7e394-118">Aktualisieren Sie die Aufbewahrungszeit der Telemetrie in Tagen auf 4 für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7e394-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7e394-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e394-119">PARAMETERS</span></span>

### <span data-ttu-id="7e394-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="7e394-120">-CloudToDevice</span></span>
<span data-ttu-id="7e394-121">Die Eigenschaften für die Befehlswarteschlange des Cloud-zu-Geräts.</span><span class="sxs-lookup"><span data-stu-id="7e394-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="7e394-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e394-122">-DefaultProfile</span></span>
<span data-ttu-id="7e394-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e394-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e394-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="7e394-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="7e394-125">Flag, das angibt, ob Benachrichtigungen für den Dateiupload aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e394-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="7e394-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="7e394-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="7e394-127">Aufbewahrungszeit in Tagen.</span><span class="sxs-lookup"><span data-stu-id="7e394-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="7e394-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="7e394-128">-FallbackRoute</span></span>
<span data-ttu-id="7e394-129">Fall Back Route für Routing</span><span class="sxs-lookup"><span data-stu-id="7e394-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="7e394-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="7e394-130">-FileUploadContainerName</span></span>
<span data-ttu-id="7e394-131">Der Name des Containers, in den die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e394-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="7e394-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="7e394-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="7e394-133">Die maximale Anzahl von Zustellungen für Dateiupload-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="7e394-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="7e394-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="7e394-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="7e394-135">Zeit zum Live-Wert für die Nachrichten in der Benachrichtigungswarteschlange für Dateiuploads.</span><span class="sxs-lookup"><span data-stu-id="7e394-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="7e394-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="7e394-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="7e394-137">Zeit zum Leben für den für den SAS-URI, der für den Dateiupload generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7e394-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="7e394-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="7e394-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="7e394-139">Die Speicher Verbindungszeichenfolge, auf die die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e394-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="7e394-140">-Name</span><span class="sxs-lookup"><span data-stu-id="7e394-140">-Name</span></span>
<span data-ttu-id="7e394-141">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="7e394-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="7e394-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e394-142">-ResourceGroupName</span></span>
<span data-ttu-id="7e394-143">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7e394-143">Resource Group Name</span></span>

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

### <span data-ttu-id="7e394-144">-Routen</span><span class="sxs-lookup"><span data-stu-id="7e394-144">-Routes</span></span>
<span data-ttu-id="7e394-145">Routen, die für das Routing hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="7e394-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="7e394-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="7e394-146">-RoutingProperties</span></span>
<span data-ttu-id="7e394-147">Die Routingeigenschaften für das Weiterleiten von Nachrichten an externe Endpunkte</span><span class="sxs-lookup"><span data-stu-id="7e394-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="7e394-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e394-148">-SkuName</span></span>
<span data-ttu-id="7e394-149">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="7e394-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="7e394-150">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="7e394-150">-Units</span></span>
<span data-ttu-id="7e394-151">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="7e394-151">Number of Units</span></span>

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

### <span data-ttu-id="7e394-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e394-152">-Confirm</span></span>
<span data-ttu-id="7e394-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e394-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e394-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e394-154">-WhatIf</span></span>
<span data-ttu-id="7e394-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e394-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e394-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e394-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e394-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e394-157">CommonParameters</span></span>
<span data-ttu-id="7e394-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e394-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e394-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e394-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e394-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e394-160">INPUTS</span></span>

### <span data-ttu-id="7e394-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7e394-161">System.String</span></span>

## <span data-ttu-id="7e394-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e394-162">OUTPUTS</span></span>

### <span data-ttu-id="7e394-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7e394-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="7e394-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e394-164">NOTES</span></span>

## <span data-ttu-id="7e394-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e394-165">RELATED LINKS</span></span>
