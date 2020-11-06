---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ba8d917c33f2ab7ac6c82db303df08c01c648bf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501617"
---
# <span data-ttu-id="d4e28-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="d4e28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4e28-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e28-103">Erstellt einen Speicher Warteschlangenauftrag.</span><span class="sxs-lookup"><span data-stu-id="d4e28-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4e28-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4e28-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e28-106">Das Cmdlet **New-AzureRmSchedulerStorageQueueJob** erstellt einen Speicher Warteschlangenauftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d4e28-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="d4e28-107">Dieses Cmdlet unterstützt dynamische Parameter auf Grundlage des *ErrorActionType* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="d4e28-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="d4e28-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="d4e28-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="d4e28-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d4e28-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4e28-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="d4e28-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4e28-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4e28-111">EXAMPLES</span></span>

## <span data-ttu-id="d4e28-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4e28-112">PARAMETERS</span></span>

### <span data-ttu-id="d4e28-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d4e28-113">-EndTime</span></span>
<span data-ttu-id="d4e28-114">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d4e28-115">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4e28-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d4e28-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d4e28-116">-ErrorActionType</span></span>
<span data-ttu-id="d4e28-117">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d4e28-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4e28-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4e28-119">Http</span><span class="sxs-lookup"><span data-stu-id="d4e28-119">Http</span></span> 
- <span data-ttu-id="d4e28-120">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d4e28-120">Https</span></span> 
- <span data-ttu-id="d4e28-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d4e28-121">StorageQueue</span></span> 
- <span data-ttu-id="d4e28-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d4e28-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="d4e28-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d4e28-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d4e28-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d4e28-124">-ExecutionCount</span></span>
<span data-ttu-id="d4e28-125">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e28-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d4e28-126">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="d4e28-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d4e28-127">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="d4e28-127">-Frequency</span></span>
<span data-ttu-id="d4e28-128">Gibt eine Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="d4e28-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4e28-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4e28-130">Minuten</span><span class="sxs-lookup"><span data-stu-id="d4e28-130">Minute</span></span> 
- <span data-ttu-id="d4e28-131">Stunde</span><span class="sxs-lookup"><span data-stu-id="d4e28-131">Hour</span></span> 
- <span data-ttu-id="d4e28-132">Tag</span><span class="sxs-lookup"><span data-stu-id="d4e28-132">Day</span></span> 
- <span data-ttu-id="d4e28-133">Woche</span><span class="sxs-lookup"><span data-stu-id="d4e28-133">Week</span></span> 
- <span data-ttu-id="d4e28-134">Monat</span><span class="sxs-lookup"><span data-stu-id="d4e28-134">Month</span></span>

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

### <span data-ttu-id="d4e28-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="d4e28-135">-Interval</span></span>
<span data-ttu-id="d4e28-136">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d4e28-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d4e28-137">-JobCollectionName</span></span>
<span data-ttu-id="d4e28-138">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="d4e28-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d4e28-139">-Jobname</span><span class="sxs-lookup"><span data-stu-id="d4e28-139">-JobName</span></span>
<span data-ttu-id="d4e28-140">Gibt einen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="d4e28-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="d4e28-141">-JobState</span></span>
<span data-ttu-id="d4e28-142">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-142">Specifies the state of the job.</span></span>
<span data-ttu-id="d4e28-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4e28-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4e28-144">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d4e28-144">Enabled</span></span> 
- <span data-ttu-id="d4e28-145">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d4e28-145">Disabled</span></span>

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

### <span data-ttu-id="d4e28-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e28-146">-ResourceGroupName</span></span>
<span data-ttu-id="d4e28-147">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="d4e28-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d4e28-148">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="d4e28-148">-StartTime</span></span>
<span data-ttu-id="d4e28-149">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d4e28-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="d4e28-150">-StorageQueueAccount</span></span>
<span data-ttu-id="d4e28-151">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="d4e28-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="d4e28-152">-StorageQueueMessage</span></span>
<span data-ttu-id="d4e28-153">Gibt eine Warteschlangen Meldung für den Speicherauftrag an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-153">Specifies a queue message for the storage job.</span></span>

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

### <span data-ttu-id="d4e28-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="d4e28-154">-StorageQueueName</span></span>
<span data-ttu-id="d4e28-155">Gibt den Namen einer Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="d4e28-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="d4e28-156">-StorageSASToken</span></span>
<span data-ttu-id="d4e28-157">Gibt ein freigegebenes zugriffssignatur Token für eine Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="d4e28-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="d4e28-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4e28-158">-Confirm</span></span>
<span data-ttu-id="d4e28-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4e28-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e28-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e28-160">-WhatIf</span></span>
<span data-ttu-id="d4e28-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e28-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e28-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4e28-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e28-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e28-163">-DefaultProfile</span></span>
<span data-ttu-id="d4e28-164">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4e28-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4e28-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e28-165">CommonParameters</span></span>
<span data-ttu-id="d4e28-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e28-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e28-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e28-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e28-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4e28-168">INPUTS</span></span>

## <span data-ttu-id="d4e28-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4e28-169">OUTPUTS</span></span>

### <span data-ttu-id="d4e28-170">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d4e28-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d4e28-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4e28-171">NOTES</span></span>

## <span data-ttu-id="d4e28-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4e28-172">RELATED LINKS</span></span>

[<span data-ttu-id="d4e28-173">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d4e28-174">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4e28-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d4e28-175">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d4e28-176">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d4e28-177">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-177">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d4e28-178">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4e28-178">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d4e28-179">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-179">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d4e28-180">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-180">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d4e28-181">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4e28-181">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


