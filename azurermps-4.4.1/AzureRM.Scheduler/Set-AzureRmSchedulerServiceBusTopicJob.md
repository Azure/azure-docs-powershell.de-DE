---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503957"
---
# <span data-ttu-id="2232b-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2232b-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="2232b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2232b-102">SYNOPSIS</span></span>
<span data-ttu-id="2232b-103">Ändert einen Service Bus-Themen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2232b-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2232b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2232b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2232b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2232b-105">DESCRIPTION</span></span>
<span data-ttu-id="2232b-106">Das Cmdlet " **Satz-AzureRmSchedulerServiceBusTopicJob** " ändert einen Service Bus-Themen Auftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="2232b-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="2232b-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="2232b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="2232b-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="2232b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="2232b-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2232b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2232b-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="2232b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2232b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2232b-111">EXAMPLES</span></span>

## <span data-ttu-id="2232b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2232b-112">PARAMETERS</span></span>

### <span data-ttu-id="2232b-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2232b-113">-EndTime</span></span>
<span data-ttu-id="2232b-114">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2232b-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="2232b-115">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2232b-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="2232b-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="2232b-116">-ErrorActionType</span></span>
<span data-ttu-id="2232b-117">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2232b-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="2232b-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2232b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2232b-119">Http</span><span class="sxs-lookup"><span data-stu-id="2232b-119">Http</span></span> 
- <span data-ttu-id="2232b-120">HTTPS</span><span class="sxs-lookup"><span data-stu-id="2232b-120">Https</span></span> 
- <span data-ttu-id="2232b-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="2232b-121">StorageQueue</span></span> 
- <span data-ttu-id="2232b-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2232b-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="2232b-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2232b-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="2232b-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="2232b-124">-ExecutionCount</span></span>
<span data-ttu-id="2232b-125">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2232b-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="2232b-126">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="2232b-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="2232b-127">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="2232b-127">-Frequency</span></span>
<span data-ttu-id="2232b-128">Gibt die maximale Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2232b-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="2232b-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2232b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2232b-130">Minuten</span><span class="sxs-lookup"><span data-stu-id="2232b-130">Minute</span></span> 
- <span data-ttu-id="2232b-131">Stunde</span><span class="sxs-lookup"><span data-stu-id="2232b-131">Hour</span></span> 
- <span data-ttu-id="2232b-132">Tag</span><span class="sxs-lookup"><span data-stu-id="2232b-132">Day</span></span> 
- <span data-ttu-id="2232b-133">Woche</span><span class="sxs-lookup"><span data-stu-id="2232b-133">Week</span></span> 
- <span data-ttu-id="2232b-134">Monat</span><span class="sxs-lookup"><span data-stu-id="2232b-134">Month</span></span>

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

### <span data-ttu-id="2232b-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="2232b-135">-Interval</span></span>
<span data-ttu-id="2232b-136">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2232b-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="2232b-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2232b-137">-JobCollectionName</span></span>
<span data-ttu-id="2232b-138">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="2232b-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="2232b-139">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2232b-139">-JobName</span></span>
<span data-ttu-id="2232b-140">Gibt den Namen des Auftrags an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2232b-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2232b-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="2232b-141">-JobState</span></span>
<span data-ttu-id="2232b-142">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2232b-142">Specifies the state of the job.</span></span>
<span data-ttu-id="2232b-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2232b-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2232b-144">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2232b-144">Enabled</span></span> 
- <span data-ttu-id="2232b-145">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="2232b-145">Disabled</span></span>

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

### <span data-ttu-id="2232b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2232b-146">-ResourceGroupName</span></span>
<span data-ttu-id="2232b-147">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="2232b-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="2232b-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="2232b-148">-ServiceBusMessage</span></span>
<span data-ttu-id="2232b-149">Gibt eine Service Bus-Themen Meldung an.</span><span class="sxs-lookup"><span data-stu-id="2232b-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="2232b-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="2232b-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="2232b-151">Gibt einen ServiceBus-Namespace an.</span><span class="sxs-lookup"><span data-stu-id="2232b-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="2232b-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="2232b-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="2232b-153">Gibt einen freigegebenen zugriffssignatur Schlüsselnamen an.</span><span class="sxs-lookup"><span data-stu-id="2232b-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="2232b-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="2232b-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="2232b-155">Gibt einen freigegebenen zugriffssignatur Schlüsselwert an.</span><span class="sxs-lookup"><span data-stu-id="2232b-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="2232b-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="2232b-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="2232b-157">Gibt einen ServiceBus-Themenpfad an.</span><span class="sxs-lookup"><span data-stu-id="2232b-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="2232b-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="2232b-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="2232b-159">Gibt einen ServiceBus-Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="2232b-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="2232b-160">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2232b-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2232b-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="2232b-161">NetMessaging</span></span>
- <span data-ttu-id="2232b-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="2232b-162">AMQP</span></span>

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

### <span data-ttu-id="2232b-163">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="2232b-163">-StartTime</span></span>
<span data-ttu-id="2232b-164">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2232b-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="2232b-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2232b-165">-Confirm</span></span>
<span data-ttu-id="2232b-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2232b-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2232b-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2232b-167">-WhatIf</span></span>
<span data-ttu-id="2232b-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2232b-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2232b-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2232b-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2232b-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2232b-170">-DefaultProfile</span></span>
<span data-ttu-id="2232b-171">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2232b-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2232b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2232b-172">CommonParameters</span></span>
<span data-ttu-id="2232b-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2232b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2232b-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2232b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2232b-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2232b-175">INPUTS</span></span>

## <span data-ttu-id="2232b-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2232b-176">OUTPUTS</span></span>

### <span data-ttu-id="2232b-177">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2232b-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="2232b-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="2232b-178">NOTES</span></span>

## <span data-ttu-id="2232b-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2232b-179">RELATED LINKS</span></span>

[<span data-ttu-id="2232b-180">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2232b-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2232b-181">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2232b-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2232b-182">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2232b-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2232b-183">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2232b-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="2232b-184">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2232b-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="2232b-185">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2232b-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2232b-186">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2232b-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2232b-187">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2232b-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2232b-188">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2232b-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


