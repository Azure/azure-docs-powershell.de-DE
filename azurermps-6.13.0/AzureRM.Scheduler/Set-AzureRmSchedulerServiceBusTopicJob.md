---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 6f1e92654c038cccf49e32b489ad5face70ae011
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665286"
---
# <span data-ttu-id="b7134-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b7134-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="b7134-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7134-102">SYNOPSIS</span></span>
<span data-ttu-id="b7134-103">Ändert einen Service Bus-Themen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b7134-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7134-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7134-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7134-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7134-105">DESCRIPTION</span></span>
<span data-ttu-id="b7134-106">Das Cmdlet " **Satz-AzureRmSchedulerServiceBusTopicJob** " ändert einen Service Bus-Themen Auftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b7134-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>
<span data-ttu-id="b7134-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="b7134-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="b7134-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="b7134-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="b7134-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b7134-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b7134-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="b7134-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b7134-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7134-111">EXAMPLES</span></span>

## <span data-ttu-id="b7134-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7134-112">PARAMETERS</span></span>

### <span data-ttu-id="b7134-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7134-113">-DefaultProfile</span></span>
<span data-ttu-id="b7134-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7134-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7134-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b7134-115">-EndTime</span></span>
<span data-ttu-id="b7134-116">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7134-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="b7134-117">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b7134-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="b7134-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="b7134-118">-ErrorActionType</span></span>
<span data-ttu-id="b7134-119">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7134-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="b7134-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7134-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7134-121">Http</span><span class="sxs-lookup"><span data-stu-id="b7134-121">Http</span></span> 
- <span data-ttu-id="b7134-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b7134-122">Https</span></span> 
- <span data-ttu-id="b7134-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="b7134-123">StorageQueue</span></span> 
- <span data-ttu-id="b7134-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b7134-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="b7134-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b7134-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="b7134-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="b7134-126">-ExecutionCount</span></span>
<span data-ttu-id="b7134-127">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7134-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="b7134-128">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="b7134-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="b7134-129">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="b7134-129">-Frequency</span></span>
<span data-ttu-id="b7134-130">Gibt die maximale Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7134-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="b7134-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7134-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7134-132">Minuten</span><span class="sxs-lookup"><span data-stu-id="b7134-132">Minute</span></span> 
- <span data-ttu-id="b7134-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="b7134-133">Hour</span></span> 
- <span data-ttu-id="b7134-134">Tag</span><span class="sxs-lookup"><span data-stu-id="b7134-134">Day</span></span> 
- <span data-ttu-id="b7134-135">Woche</span><span class="sxs-lookup"><span data-stu-id="b7134-135">Week</span></span> 
- <span data-ttu-id="b7134-136">Monat</span><span class="sxs-lookup"><span data-stu-id="b7134-136">Month</span></span>

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

### <span data-ttu-id="b7134-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="b7134-137">-Interval</span></span>
<span data-ttu-id="b7134-138">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7134-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="b7134-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b7134-139">-JobCollectionName</span></span>
<span data-ttu-id="b7134-140">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="b7134-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="b7134-141">-Jobname</span><span class="sxs-lookup"><span data-stu-id="b7134-141">-JobName</span></span>
<span data-ttu-id="b7134-142">Gibt den Namen des Auftrags an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b7134-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b7134-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="b7134-143">-JobState</span></span>
<span data-ttu-id="b7134-144">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="b7134-144">Specifies the state of the job.</span></span>
<span data-ttu-id="b7134-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7134-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7134-146">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b7134-146">Enabled</span></span> 
- <span data-ttu-id="b7134-147">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="b7134-147">Disabled</span></span>

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

### <span data-ttu-id="b7134-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7134-148">-ResourceGroupName</span></span>
<span data-ttu-id="b7134-149">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="b7134-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="b7134-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="b7134-150">-ServiceBusMessage</span></span>
<span data-ttu-id="b7134-151">Gibt eine Service Bus-Themen Meldung an.</span><span class="sxs-lookup"><span data-stu-id="b7134-151">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="b7134-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b7134-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="b7134-153">Gibt einen ServiceBus-Namespace an.</span><span class="sxs-lookup"><span data-stu-id="b7134-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="b7134-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="b7134-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="b7134-155">Gibt einen freigegebenen zugriffssignatur Schlüsselnamen an.</span><span class="sxs-lookup"><span data-stu-id="b7134-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="b7134-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="b7134-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="b7134-157">Gibt einen freigegebenen zugriffssignatur Schlüsselwert an.</span><span class="sxs-lookup"><span data-stu-id="b7134-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="b7134-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="b7134-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="b7134-159">Gibt einen ServiceBus-Themenpfad an.</span><span class="sxs-lookup"><span data-stu-id="b7134-159">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="b7134-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="b7134-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="b7134-161">Gibt einen ServiceBus-Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="b7134-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="b7134-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7134-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7134-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="b7134-163">NetMessaging</span></span>
- <span data-ttu-id="b7134-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="b7134-164">AMQP</span></span>

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

### <span data-ttu-id="b7134-165">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b7134-165">-StartTime</span></span>
<span data-ttu-id="b7134-166">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7134-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="b7134-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7134-167">-Confirm</span></span>
<span data-ttu-id="b7134-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7134-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7134-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7134-169">-WhatIf</span></span>
<span data-ttu-id="b7134-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7134-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7134-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7134-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7134-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7134-172">CommonParameters</span></span>
<span data-ttu-id="b7134-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7134-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7134-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7134-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7134-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7134-175">INPUTS</span></span>

### <span data-ttu-id="b7134-176">System. String</span><span class="sxs-lookup"><span data-stu-id="b7134-176">System.String</span></span>

## <span data-ttu-id="b7134-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7134-177">OUTPUTS</span></span>

### <span data-ttu-id="b7134-178">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b7134-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="b7134-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7134-179">NOTES</span></span>

## <span data-ttu-id="b7134-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7134-180">RELATED LINKS</span></span>

[<span data-ttu-id="b7134-181">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b7134-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b7134-182">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b7134-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b7134-183">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b7134-183">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b7134-184">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b7134-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="b7134-185">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b7134-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="b7134-186">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b7134-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b7134-187">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b7134-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b7134-188">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b7134-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b7134-189">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b7134-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


