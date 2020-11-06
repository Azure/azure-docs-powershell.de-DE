---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: aad54e42d628239f087e376eabe6b9950c07b6f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504126"
---
# <span data-ttu-id="d7702-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="d7702-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="d7702-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7702-102">SYNOPSIS</span></span>
<span data-ttu-id="d7702-103">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="d7702-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7702-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7702-104">SYNTAX</span></span>

### <span data-ttu-id="d7702-105">UpdateSku (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7702-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7702-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="d7702-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7702-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7702-113">DESCRIPTION</span></span>
<span data-ttu-id="d7702-114">Aktualisiert die Eigenschaften eines IotHub.</span><span class="sxs-lookup"><span data-stu-id="d7702-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="d7702-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7702-115">EXAMPLES</span></span>

### <span data-ttu-id="d7702-116">Beispiel 1 Aktualisieren der SKU</span><span class="sxs-lookup"><span data-stu-id="d7702-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="d7702-117">Aktualisieren Sie die SKU auf S1 und die Einheiten auf 5 für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d7702-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d7702-118">Beispiel 2 Aktualisieren der eventhub-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7702-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="d7702-119">Aktualisieren Sie die Aufbewahrungszeit in Tagen auf 4 für die Telemetrie-und operationsmonitoringevents-Ereignisse für die IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d7702-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d7702-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7702-120">PARAMETERS</span></span>

### <span data-ttu-id="d7702-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="d7702-121">-CloudToDevice</span></span>
<span data-ttu-id="d7702-122">Die Eigenschaften für die Befehlswarteschlange des Cloud-zu-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d7702-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="d7702-123">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="d7702-123">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="d7702-124">Flag, das angibt, ob Benachrichtigungen für den Dateiupload aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7702-124">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="d7702-125">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="d7702-125">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="d7702-126">Aufbewahrungszeit in Tagen.</span><span class="sxs-lookup"><span data-stu-id="d7702-126">Retention time in days.</span></span> 

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

### <span data-ttu-id="d7702-127">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="d7702-127">-FallbackRoute</span></span>
<span data-ttu-id="d7702-128">Fall Back Route für Routing</span><span class="sxs-lookup"><span data-stu-id="d7702-128">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="d7702-129">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="d7702-129">-FileUploadContainerName</span></span>
<span data-ttu-id="d7702-130">Der Name des Containers, in den die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7702-130">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="d7702-131">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d7702-131">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="d7702-132">Die maximale Anzahl von Zustellungen für Dateiupload-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d7702-132">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="d7702-133">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="d7702-133">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="d7702-134">Zeit zum Live-Wert für die Nachrichten in der Benachrichtigungswarteschlange für Dateiuploads.</span><span class="sxs-lookup"><span data-stu-id="d7702-134">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="d7702-135">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="d7702-135">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="d7702-136">Zeit zum Leben für den für den SAS-URI, der für den Dateiupload generiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7702-136">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="d7702-137">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="d7702-137">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="d7702-138">Die Speicher Verbindungszeichenfolge, auf die die Dateien hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7702-138">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="d7702-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d7702-139">-Name</span></span>
<span data-ttu-id="d7702-140">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="d7702-140">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7702-141">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-141">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="d7702-142">Die Eigenschaften im Zusammenhang mit der Betriebsüberwachung.</span><span class="sxs-lookup"><span data-stu-id="d7702-142">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7702-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7702-143">-ResourceGroupName</span></span>
<span data-ttu-id="d7702-144">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d7702-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7702-145">-Routen</span><span class="sxs-lookup"><span data-stu-id="d7702-145">-Routes</span></span>
<span data-ttu-id="d7702-146">Routen, die für das Routing hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="d7702-146">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="d7702-147">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-147">-RoutingProperties</span></span>
<span data-ttu-id="d7702-148">Die Routingeigenschaften für das Weiterleiten von Nachrichten an externe Endpunkte</span><span class="sxs-lookup"><span data-stu-id="d7702-148">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="d7702-149">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7702-149">-SkuName</span></span>
<span data-ttu-id="d7702-150">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="d7702-150">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7702-151">-Einheiten</span><span class="sxs-lookup"><span data-stu-id="d7702-151">-Units</span></span>
<span data-ttu-id="d7702-152">Anzahl der Einheiten</span><span class="sxs-lookup"><span data-stu-id="d7702-152">Number of Units</span></span>

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

### <span data-ttu-id="d7702-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7702-153">-Confirm</span></span>
<span data-ttu-id="d7702-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7702-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7702-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7702-155">-WhatIf</span></span>
<span data-ttu-id="d7702-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7702-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7702-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7702-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7702-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7702-158">-DefaultProfile</span></span>
<span data-ttu-id="d7702-159">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7702-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7702-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7702-160">CommonParameters</span></span>
<span data-ttu-id="d7702-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7702-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7702-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7702-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7702-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7702-163">INPUTS</span></span>

### <span data-ttu-id="d7702-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d7702-164">System.String</span></span>
<span data-ttu-id="d7702-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d7702-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="d7702-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7702-166">OUTPUTS</span></span>

### <span data-ttu-id="d7702-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d7702-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d7702-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7702-168">NOTES</span></span>

## <span data-ttu-id="d7702-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7702-169">RELATED LINKS</span></span>

