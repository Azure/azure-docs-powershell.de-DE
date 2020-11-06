---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501621"
---
# <span data-ttu-id="51f29-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="51f29-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="51f29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51f29-102">SYNOPSIS</span></span>
<span data-ttu-id="51f29-103">Erstellt einen Service Bus-Themen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="51f29-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51f29-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51f29-105">DESCRIPTION</span></span>
<span data-ttu-id="51f29-106">Das Cmdlet **New-AzureRmSchedulerServiceBusTopicJob** erstellt einen Service Bus-Themen Auftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="51f29-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="51f29-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="51f29-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="51f29-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="51f29-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="51f29-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="51f29-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="51f29-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="51f29-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="51f29-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51f29-111">EXAMPLES</span></span>

## <span data-ttu-id="51f29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="51f29-112">PARAMETERS</span></span>

### <span data-ttu-id="51f29-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="51f29-113">-EndTime</span></span>
<span data-ttu-id="51f29-114">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="51f29-115">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51f29-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="51f29-116">-ErrorActionType</span></span>
<span data-ttu-id="51f29-117">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="51f29-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51f29-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51f29-119">Http</span><span class="sxs-lookup"><span data-stu-id="51f29-119">Http</span></span> 
- <span data-ttu-id="51f29-120">HTTPS</span><span class="sxs-lookup"><span data-stu-id="51f29-120">Https</span></span> 
- <span data-ttu-id="51f29-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="51f29-121">StorageQueue</span></span> 
- <span data-ttu-id="51f29-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="51f29-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="51f29-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="51f29-123">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="51f29-124">-ExecutionCount</span></span>
<span data-ttu-id="51f29-125">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51f29-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="51f29-126">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="51f29-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="51f29-127">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="51f29-127">-Frequency</span></span>
<span data-ttu-id="51f29-128">Gibt die maximale Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="51f29-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51f29-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51f29-130">Minuten</span><span class="sxs-lookup"><span data-stu-id="51f29-130">Minute</span></span> 
- <span data-ttu-id="51f29-131">Stunde</span><span class="sxs-lookup"><span data-stu-id="51f29-131">Hour</span></span> 
- <span data-ttu-id="51f29-132">Tag</span><span class="sxs-lookup"><span data-stu-id="51f29-132">Day</span></span> 
- <span data-ttu-id="51f29-133">Woche</span><span class="sxs-lookup"><span data-stu-id="51f29-133">Week</span></span> 
- <span data-ttu-id="51f29-134">Monat</span><span class="sxs-lookup"><span data-stu-id="51f29-134">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="51f29-135">-Interval</span></span>
<span data-ttu-id="51f29-136">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="51f29-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="51f29-137">-JobCollectionName</span></span>
<span data-ttu-id="51f29-138">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="51f29-138">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-139">-Jobname</span><span class="sxs-lookup"><span data-stu-id="51f29-139">-JobName</span></span>
<span data-ttu-id="51f29-140">Gibt einen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="51f29-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="51f29-141">-JobState</span></span>
<span data-ttu-id="51f29-142">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="51f29-142">Specifies the state of the job.</span></span>
<span data-ttu-id="51f29-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51f29-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51f29-144">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="51f29-144">Enabled</span></span> 
- <span data-ttu-id="51f29-145">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="51f29-145">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f29-146">-ResourceGroupName</span></span>
<span data-ttu-id="51f29-147">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="51f29-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="51f29-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="51f29-148">-ServiceBusMessage</span></span>
<span data-ttu-id="51f29-149">Gibt eine Service Bus-Themen Meldung an.</span><span class="sxs-lookup"><span data-stu-id="51f29-149">Specifies a service bus topic message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="51f29-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="51f29-151">Gibt einen ServiceBus-Namespace an.</span><span class="sxs-lookup"><span data-stu-id="51f29-151">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="51f29-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="51f29-153">Gibt einen freigegebenen zugriffssignatur Schlüsselnamen an.</span><span class="sxs-lookup"><span data-stu-id="51f29-153">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="51f29-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="51f29-155">Gibt einen freigegebenen zugriffssignatur Schlüsselwert an.</span><span class="sxs-lookup"><span data-stu-id="51f29-155">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="51f29-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="51f29-157">Gibt einen ServiceBus-Themenpfad an.</span><span class="sxs-lookup"><span data-stu-id="51f29-157">Specifies a service bus topic path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="51f29-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="51f29-159">Gibt einen ServiceBus-Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="51f29-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="51f29-160">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51f29-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51f29-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="51f29-161">NetMessaging</span></span>
- <span data-ttu-id="51f29-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="51f29-162">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-163">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="51f29-163">-StartTime</span></span>
<span data-ttu-id="51f29-164">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="51f29-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f29-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51f29-165">-Confirm</span></span>
<span data-ttu-id="51f29-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51f29-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f29-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f29-167">-WhatIf</span></span>
<span data-ttu-id="51f29-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51f29-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f29-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51f29-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f29-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f29-170">-DefaultProfile</span></span>
<span data-ttu-id="51f29-171">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51f29-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f29-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f29-172">CommonParameters</span></span>
<span data-ttu-id="51f29-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f29-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f29-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f29-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f29-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51f29-175">INPUTS</span></span>

## <span data-ttu-id="51f29-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51f29-176">OUTPUTS</span></span>

### <span data-ttu-id="51f29-177">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="51f29-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="51f29-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="51f29-178">NOTES</span></span>

## <span data-ttu-id="51f29-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51f29-179">RELATED LINKS</span></span>

[<span data-ttu-id="51f29-180">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="51f29-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="51f29-181">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51f29-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51f29-182">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="51f29-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="51f29-183">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="51f29-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="51f29-184">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="51f29-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="51f29-185">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51f29-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51f29-186">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="51f29-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="51f29-187">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="51f29-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="51f29-188">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="51f29-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


