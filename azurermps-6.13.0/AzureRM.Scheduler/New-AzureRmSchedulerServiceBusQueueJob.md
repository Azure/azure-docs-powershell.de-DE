---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477713"
---
# <span data-ttu-id="eb2f6-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="eb2f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2f6-103">Erstellt einen Service Bus-Warteschlangenauftrag.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb2f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb2f6-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb2f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="eb2f6-106">Das Cmdlet **New-AzureRmSchedulerServiceBusQueueJob** erstellt einen Service Bus-Warteschlangenauftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="eb2f6-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="eb2f6-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="eb2f6-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="eb2f6-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="eb2f6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb2f6-111">EXAMPLES</span></span>

## <span data-ttu-id="eb2f6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb2f6-112">PARAMETERS</span></span>

### <span data-ttu-id="eb2f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2f6-113">-DefaultProfile</span></span>
<span data-ttu-id="eb2f6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb2f6-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="eb2f6-115">-EndTime</span></span>
<span data-ttu-id="eb2f6-116">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="eb2f6-117">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="eb2f6-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="eb2f6-118">-ErrorActionType</span></span>
<span data-ttu-id="eb2f6-119">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="eb2f6-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eb2f6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2f6-121">Http</span><span class="sxs-lookup"><span data-stu-id="eb2f6-121">Http</span></span> 
- <span data-ttu-id="eb2f6-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="eb2f6-122">Https</span></span> 
- <span data-ttu-id="eb2f6-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="eb2f6-123">StorageQueue</span></span> 
- <span data-ttu-id="eb2f6-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="eb2f6-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="eb2f6-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="eb2f6-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="eb2f6-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="eb2f6-126">-ExecutionCount</span></span>
<span data-ttu-id="eb2f6-127">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="eb2f6-128">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="eb2f6-129">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="eb2f6-129">-Frequency</span></span>
<span data-ttu-id="eb2f6-130">Gibt eine Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="eb2f6-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eb2f6-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2f6-132">Minuten</span><span class="sxs-lookup"><span data-stu-id="eb2f6-132">Minute</span></span> 
- <span data-ttu-id="eb2f6-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="eb2f6-133">Hour</span></span> 
- <span data-ttu-id="eb2f6-134">Tag</span><span class="sxs-lookup"><span data-stu-id="eb2f6-134">Day</span></span> 
- <span data-ttu-id="eb2f6-135">Woche</span><span class="sxs-lookup"><span data-stu-id="eb2f6-135">Week</span></span> 
- <span data-ttu-id="eb2f6-136">Monat</span><span class="sxs-lookup"><span data-stu-id="eb2f6-136">Month</span></span>

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

### <span data-ttu-id="eb2f6-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="eb2f6-137">-Interval</span></span>
<span data-ttu-id="eb2f6-138">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="eb2f6-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="eb2f6-139">-JobCollectionName</span></span>
<span data-ttu-id="eb2f6-140">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="eb2f6-141">-Jobname</span><span class="sxs-lookup"><span data-stu-id="eb2f6-141">-JobName</span></span>
<span data-ttu-id="eb2f6-142">Gibt einen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="eb2f6-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="eb2f6-143">-JobState</span></span>
<span data-ttu-id="eb2f6-144">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-144">Specifies the state of the job.</span></span>
<span data-ttu-id="eb2f6-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eb2f6-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2f6-146">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="eb2f6-146">Enabled</span></span> 
- <span data-ttu-id="eb2f6-147">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="eb2f6-147">Disabled</span></span>

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

### <span data-ttu-id="eb2f6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2f6-148">-ResourceGroupName</span></span>
<span data-ttu-id="eb2f6-149">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="eb2f6-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="eb2f6-150">-ServiceBusMessage</span></span>
<span data-ttu-id="eb2f6-151">Gibt eine ServiceBus-Warteschlangen Meldung an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="eb2f6-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="eb2f6-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="eb2f6-153">Gibt einen ServiceBus-Namespace an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="eb2f6-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="eb2f6-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="eb2f6-155">Gibt einen ServiceBus-Warteschlangennamen an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="eb2f6-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="eb2f6-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="eb2f6-157">Gibt einen freigegebenen zugriffssignatur Schlüsselnamen an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="eb2f6-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="eb2f6-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="eb2f6-159">Gibt einen freigegebenen zugriffssignatur Schlüsselwert an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="eb2f6-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="eb2f6-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="eb2f6-161">Gibt einen ServiceBus-Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="eb2f6-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eb2f6-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2f6-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="eb2f6-163">NetMessaging</span></span> 
- <span data-ttu-id="eb2f6-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="eb2f6-164">AMQP</span></span>

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

### <span data-ttu-id="eb2f6-165">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="eb2f6-165">-StartTime</span></span>
<span data-ttu-id="eb2f6-166">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="eb2f6-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb2f6-167">-Confirm</span></span>
<span data-ttu-id="eb2f6-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb2f6-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb2f6-169">-WhatIf</span></span>
<span data-ttu-id="eb2f6-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb2f6-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb2f6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2f6-172">CommonParameters</span></span>
<span data-ttu-id="eb2f6-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb2f6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2f6-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb2f6-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2f6-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb2f6-175">INPUTS</span></span>

### <span data-ttu-id="eb2f6-176">System. String</span><span class="sxs-lookup"><span data-stu-id="eb2f6-176">System.String</span></span>

## <span data-ttu-id="eb2f6-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb2f6-177">OUTPUTS</span></span>

### <span data-ttu-id="eb2f6-178">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb2f6-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="eb2f6-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb2f6-179">NOTES</span></span>

## <span data-ttu-id="eb2f6-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb2f6-180">RELATED LINKS</span></span>

[<span data-ttu-id="eb2f6-181">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="eb2f6-182">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eb2f6-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eb2f6-183">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="eb2f6-184">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="eb2f6-185">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="eb2f6-186">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eb2f6-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eb2f6-187">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="eb2f6-188">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="eb2f6-189">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="eb2f6-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


