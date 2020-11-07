---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665211"
---
# <span data-ttu-id="3308a-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="3308a-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="3308a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3308a-102">SYNOPSIS</span></span>
<span data-ttu-id="3308a-103">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="3308a-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3308a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3308a-104">SYNTAX</span></span>

### <span data-ttu-id="3308a-105">UpdateSku (Standard)</span><span class="sxs-lookup"><span data-stu-id="3308a-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3308a-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="3308a-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3308a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3308a-113">DESCRIPTION</span></span>
<span data-ttu-id="3308a-114">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="3308a-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="3308a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3308a-115">EXAMPLES</span></span>

### <span data-ttu-id="3308a-116">Beispiel 1 Aktualisieren der SKU</span><span class="sxs-lookup"><span data-stu-id="3308a-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="3308a-117">Aktualisieren Sie die SKU auf S1 und die Einheiten auf 5 für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="3308a-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="3308a-118">Beispiel 2 Aktualisieren der eventhub-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3308a-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="3308a-119">Aktualisieren Sie die Aufbewahrungszeit in Tagen auf 4 für die Telemetrie-und operationsmonitoringevents-Ereignisse für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="3308a-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3308a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3308a-120">PARAMETERS</span></span>

### <span data-ttu-id="3308a-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="3308a-121">-CloudToDevice</span></span>
<span data-ttu-id="3308a-122">Die Eigenschaften für die Befehlswarteschlange des Cloud-zu-Geräts.</span><span class="sxs-lookup"><span data-stu-id="3308a-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3308a-123">-DefaultProfile</span></span>
<span data-ttu-id="3308a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3308a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3308a-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="3308a-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="3308a-126">Flag, das angibt, ob Benachrichtigungen für den Dateiupload aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3308a-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="3308a-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="3308a-128">Aufbewahrungszeit in Tagen.</span><span class="sxs-lookup"><span data-stu-id="3308a-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="3308a-129">-FallbackRoute</span></span>
<span data-ttu-id="3308a-130">Fall Back Route für Routing</span><span class="sxs-lookup"><span data-stu-id="3308a-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="3308a-131">-FileUploadContainerName</span></span>
<span data-ttu-id="3308a-132">Der Name des Containers, in den die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3308a-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3308a-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="3308a-134">Die maximale Anzahl von Zustellungen für Dateiupload-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="3308a-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="3308a-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="3308a-136">Zeit zum Live-Wert für die Nachrichten in der Benachrichtigungswarteschlange für Dateiuploads.</span><span class="sxs-lookup"><span data-stu-id="3308a-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="3308a-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="3308a-138">Zeit zum Leben für den für den SAS-URI, der für den Dateiupload generiert wird.</span><span class="sxs-lookup"><span data-stu-id="3308a-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="3308a-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="3308a-140">Die Speicher Verbindungszeichenfolge, auf die die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3308a-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-141">-Name</span><span class="sxs-lookup"><span data-stu-id="3308a-141">-Name</span></span>
<span data-ttu-id="3308a-142">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="3308a-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="3308a-144">Die Eigenschaften im Zusammenhang mit der Betriebsüberwachung.</span><span class="sxs-lookup"><span data-stu-id="3308a-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3308a-145">-ResourceGroupName</span></span>
<span data-ttu-id="3308a-146">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3308a-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-147">-Routen</span><span class="sxs-lookup"><span data-stu-id="3308a-147">-Routes</span></span>
<span data-ttu-id="3308a-148">Routen, die für das Routing hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="3308a-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="3308a-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-149">-RoutingProperties</span></span>
<span data-ttu-id="3308a-150">Die Routingeigenschaften für das Weiterleiten von Nachrichten an externe Endpunkte</span><span class="sxs-lookup"><span data-stu-id="3308a-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3308a-151">-SkuName</span></span>
<span data-ttu-id="3308a-152">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="3308a-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-153">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="3308a-153">-Units</span></span>
<span data-ttu-id="3308a-154">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="3308a-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3308a-155">-Confirm</span></span>
<span data-ttu-id="3308a-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3308a-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3308a-157">-WhatIf</span></span>
<span data-ttu-id="3308a-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3308a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3308a-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3308a-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3308a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3308a-160">CommonParameters</span></span>
<span data-ttu-id="3308a-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3308a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3308a-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3308a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3308a-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3308a-163">INPUTS</span></span>

### <span data-ttu-id="3308a-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3308a-164">System.String</span></span>
<span data-ttu-id="3308a-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="3308a-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="3308a-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3308a-166">OUTPUTS</span></span>

### <span data-ttu-id="3308a-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3308a-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="3308a-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="3308a-168">NOTES</span></span>

## <span data-ttu-id="3308a-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3308a-169">RELATED LINKS</span></span>

