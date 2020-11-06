---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: eb72b64576524d85730e89f6eece094591a12158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502441"
---
# <span data-ttu-id="4bc2d-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="4bc2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc2d-103">Erstellt einen Speicher Warteschlangenauftrag.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc2d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bc2d-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc2d-106">Das Cmdlet **New-AzureRmSchedulerStorageQueueJob** erstellt einen Speicher Warteschlangenauftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="4bc2d-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="4bc2d-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="4bc2d-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4bc2d-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4bc2d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bc2d-111">EXAMPLES</span></span>

## <span data-ttu-id="4bc2d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bc2d-112">PARAMETERS</span></span>

### <span data-ttu-id="4bc2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc2d-113">-DefaultProfile</span></span>
<span data-ttu-id="4bc2d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc2d-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4bc2d-115">-EndTime</span></span>
<span data-ttu-id="4bc2d-116">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4bc2d-117">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4bc2d-118">-ErrorActionType</span></span>
<span data-ttu-id="4bc2d-119">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4bc2d-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4bc2d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bc2d-121">Http</span><span class="sxs-lookup"><span data-stu-id="4bc2d-121">Http</span></span> 
- <span data-ttu-id="4bc2d-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="4bc2d-122">Https</span></span> 
- <span data-ttu-id="4bc2d-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4bc2d-123">StorageQueue</span></span> 
- <span data-ttu-id="4bc2d-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4bc2d-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4bc2d-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4bc2d-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4bc2d-126">-ExecutionCount</span></span>
<span data-ttu-id="4bc2d-127">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4bc2d-128">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-129">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="4bc2d-129">-Frequency</span></span>
<span data-ttu-id="4bc2d-130">Gibt eine Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="4bc2d-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4bc2d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bc2d-132">Minuten</span><span class="sxs-lookup"><span data-stu-id="4bc2d-132">Minute</span></span> 
- <span data-ttu-id="4bc2d-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="4bc2d-133">Hour</span></span> 
- <span data-ttu-id="4bc2d-134">Tag</span><span class="sxs-lookup"><span data-stu-id="4bc2d-134">Day</span></span> 
- <span data-ttu-id="4bc2d-135">Woche</span><span class="sxs-lookup"><span data-stu-id="4bc2d-135">Week</span></span> 
- <span data-ttu-id="4bc2d-136">Monat</span><span class="sxs-lookup"><span data-stu-id="4bc2d-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="4bc2d-137">-Interval</span></span>
<span data-ttu-id="4bc2d-138">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4bc2d-139">-JobCollectionName</span></span>
<span data-ttu-id="4bc2d-140">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-141">-Jobname</span><span class="sxs-lookup"><span data-stu-id="4bc2d-141">-JobName</span></span>
<span data-ttu-id="4bc2d-142">Gibt einen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="4bc2d-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="4bc2d-143">-JobState</span></span>
<span data-ttu-id="4bc2d-144">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-144">Specifies the state of the job.</span></span>
<span data-ttu-id="4bc2d-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4bc2d-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bc2d-146">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="4bc2d-146">Enabled</span></span> 
- <span data-ttu-id="4bc2d-147">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="4bc2d-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc2d-148">-ResourceGroupName</span></span>
<span data-ttu-id="4bc2d-149">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4bc2d-150">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4bc2d-150">-StartTime</span></span>
<span data-ttu-id="4bc2d-151">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="4bc2d-152">-StorageQueueAccount</span></span>
<span data-ttu-id="4bc2d-153">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="4bc2d-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="4bc2d-154">-StorageQueueMessage</span></span>
<span data-ttu-id="4bc2d-155">Gibt eine Warteschlangen Meldung für den Speicherauftrag an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-155">Specifies a queue message for the storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc2d-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="4bc2d-156">-StorageQueueName</span></span>
<span data-ttu-id="4bc2d-157">Gibt den Namen einer Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="4bc2d-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="4bc2d-158">-StorageSASToken</span></span>
<span data-ttu-id="4bc2d-159">Gibt ein freigegebenes zugriffssignatur Token für eine Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="4bc2d-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bc2d-160">-Confirm</span></span>
<span data-ttu-id="4bc2d-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc2d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc2d-162">-WhatIf</span></span>
<span data-ttu-id="4bc2d-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc2d-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc2d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc2d-165">CommonParameters</span></span>
<span data-ttu-id="4bc2d-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc2d-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc2d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc2d-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bc2d-168">INPUTS</span></span>

### <span data-ttu-id="4bc2d-169">Keine</span><span class="sxs-lookup"><span data-stu-id="4bc2d-169">None</span></span>
<span data-ttu-id="4bc2d-170">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4bc2d-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bc2d-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bc2d-171">OUTPUTS</span></span>

### <span data-ttu-id="4bc2d-172">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4bc2d-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4bc2d-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bc2d-173">NOTES</span></span>

## <span data-ttu-id="4bc2d-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bc2d-174">RELATED LINKS</span></span>

[<span data-ttu-id="4bc2d-175">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4bc2d-176">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4bc2d-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4bc2d-177">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4bc2d-178">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4bc2d-179">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4bc2d-180">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4bc2d-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4bc2d-181">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4bc2d-182">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4bc2d-183">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4bc2d-183">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


