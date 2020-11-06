---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 9f43780cc7684c897b7b6d42e381e47f6ff8e106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501398"
---
# <span data-ttu-id="0a6e0-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="0a6e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6e0-103">Ändert einen Scheduler http-Job.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6e0-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6e0-106">Das Cmdlet " **Satz-AzureRmSchedulerHttpJob** " ändert einen HTTP-Auftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="0a6e0-107">Dieses Cmdlet unterstützt dynamische Parameter basierend auf den Parametern *ErrorActionType* und *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="0a6e0-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="0a6e0-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="0a6e0-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a6e0-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a6e0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a6e0-111">EXAMPLES</span></span>

## <span data-ttu-id="0a6e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a6e0-112">PARAMETERS</span></span>

### <span data-ttu-id="0a6e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6e0-113">-DefaultProfile</span></span>
<span data-ttu-id="0a6e0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a6e0-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0a6e0-115">-EndTime</span></span>
<span data-ttu-id="0a6e0-116">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="0a6e0-117">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0a6e0-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="0a6e0-118">-ErrorActionType</span></span>
<span data-ttu-id="0a6e0-119">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="0a6e0-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a6e0-121">Http</span><span class="sxs-lookup"><span data-stu-id="0a6e0-121">Http</span></span> 
- <span data-ttu-id="0a6e0-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="0a6e0-122">Https</span></span> 
- <span data-ttu-id="0a6e0-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="0a6e0-123">StorageQueue</span></span> 
- <span data-ttu-id="0a6e0-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0a6e0-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="0a6e0-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0a6e0-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="0a6e0-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="0a6e0-126">-ExecutionCount</span></span>
<span data-ttu-id="0a6e0-127">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="0a6e0-128">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="0a6e0-129">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="0a6e0-129">-Frequency</span></span>
<span data-ttu-id="0a6e0-130">Gibt die maximale Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="0a6e0-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a6e0-132">Minuten</span><span class="sxs-lookup"><span data-stu-id="0a6e0-132">Minute</span></span> 
- <span data-ttu-id="0a6e0-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="0a6e0-133">Hour</span></span> 
- <span data-ttu-id="0a6e0-134">Tag</span><span class="sxs-lookup"><span data-stu-id="0a6e0-134">Day</span></span> 
- <span data-ttu-id="0a6e0-135">Woche</span><span class="sxs-lookup"><span data-stu-id="0a6e0-135">Week</span></span> 
- <span data-ttu-id="0a6e0-136">Monat</span><span class="sxs-lookup"><span data-stu-id="0a6e0-136">Month</span></span>

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

### <span data-ttu-id="0a6e0-137">-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-137">-Headers</span></span>
<span data-ttu-id="0a6e0-138">Gibt eine Hashtabelle an, die Überschriften enthält.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e0-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0a6e0-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="0a6e0-140">Gibt den HTTP-Authentifizierungs an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="0a6e0-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a6e0-142">Keine</span><span class="sxs-lookup"><span data-stu-id="0a6e0-142">None</span></span> 
- <span data-ttu-id="0a6e0-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0a6e0-143">ClientCertificate</span></span> 
- <span data-ttu-id="0a6e0-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="0a6e0-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="0a6e0-145">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="0a6e0-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e0-146">-Intervall</span><span class="sxs-lookup"><span data-stu-id="0a6e0-146">-Interval</span></span>
<span data-ttu-id="0a6e0-147">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="0a6e0-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0a6e0-148">-JobCollectionName</span></span>
<span data-ttu-id="0a6e0-149">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="0a6e0-150">-Jobname</span><span class="sxs-lookup"><span data-stu-id="0a6e0-150">-JobName</span></span>
<span data-ttu-id="0a6e0-151">Gibt den Namen des Auftrags an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0a6e0-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="0a6e0-152">-JobState</span></span>
<span data-ttu-id="0a6e0-153">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-153">Specifies the state of the job.</span></span>
<span data-ttu-id="0a6e0-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a6e0-155">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0a6e0-155">Enabled</span></span> 
- <span data-ttu-id="0a6e0-156">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0a6e0-156">Disabled</span></span>

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

### <span data-ttu-id="0a6e0-157">-Methode</span><span class="sxs-lookup"><span data-stu-id="0a6e0-157">-Method</span></span>
<span data-ttu-id="0a6e0-158">Gibt die Methode für die Aktionstypen für diesen Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="0a6e0-159">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a6e0-160">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0a6e0-160">GET</span></span> 
- <span data-ttu-id="0a6e0-161">Setzen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-161">PUT</span></span> 
- <span data-ttu-id="0a6e0-162">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-162">POST</span></span> 
- <span data-ttu-id="0a6e0-163">Löschen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e0-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="0a6e0-164">-RequestBody</span></span>
<span data-ttu-id="0a6e0-165">Gibt den Wert des Texts für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-165">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e0-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6e0-166">-ResourceGroupName</span></span>
<span data-ttu-id="0a6e0-167">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="0a6e0-168">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0a6e0-168">-StartTime</span></span>
<span data-ttu-id="0a6e0-169">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="0a6e0-170">-URI</span><span class="sxs-lookup"><span data-stu-id="0a6e0-170">-Uri</span></span>
<span data-ttu-id="0a6e0-171">Gibt einen URI für die Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e0-172">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-172">-Confirm</span></span>
<span data-ttu-id="0a6e0-173">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6e0-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6e0-174">-WhatIf</span></span>
<span data-ttu-id="0a6e0-175">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6e0-176">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6e0-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6e0-177">CommonParameters</span></span>
<span data-ttu-id="0a6e0-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6e0-179">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6e0-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6e0-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a6e0-180">INPUTS</span></span>

### <span data-ttu-id="0a6e0-181">Keine</span><span class="sxs-lookup"><span data-stu-id="0a6e0-181">None</span></span>
<span data-ttu-id="0a6e0-182">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a6e0-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a6e0-183">OUTPUTS</span></span>

### <span data-ttu-id="0a6e0-184">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0a6e0-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="0a6e0-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a6e0-185">NOTES</span></span>

## <span data-ttu-id="0a6e0-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a6e0-186">RELATED LINKS</span></span>

[<span data-ttu-id="0a6e0-187">Neu – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0a6e0-188">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0a6e0-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0a6e0-189">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0a6e0-190">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0a6e0-191">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="0a6e0-192">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0a6e0-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0a6e0-193">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0a6e0-194">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0a6e0-195">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0a6e0-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


