---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663831"
---
# <span data-ttu-id="8a1b8-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="8a1b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1b8-103">Erstellt einen HTTP-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a1b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a1b8-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a1b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a1b8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1b8-106">Das Cmdlet **New-AzureRmSchedulerHttpJob** erstellt einen HTTP-Auftrag in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="8a1b8-107">Dieses Cmdlet unterstützt dynamische Parameter basierend auf den Parametern *ErrorActionType* und *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="8a1b8-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="8a1b8-108">Dynamische Parameter werden auf Grundlage anderer Parameterwerte zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="8a1b8-109">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, nachdem Sie die anderen Parameter angegeben haben, geben Sie einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8a1b8-110">Wenn Sie keinen erforderlichen Parameter angeben, werden Sie vom Cmdlet aufgefordert, den Wert zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8a1b8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a1b8-111">EXAMPLES</span></span>

## <span data-ttu-id="8a1b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a1b8-112">PARAMETERS</span></span>

### <span data-ttu-id="8a1b8-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8a1b8-113">-EndTime</span></span>
<span data-ttu-id="8a1b8-114">Gibt eine Endzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="8a1b8-115">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="8a1b8-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="8a1b8-116">-ErrorActionType</span></span>
<span data-ttu-id="8a1b8-117">Gibt eine Fehler Aktionseinstellung für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="8a1b8-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a1b8-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a1b8-119">Http</span><span class="sxs-lookup"><span data-stu-id="8a1b8-119">Http</span></span> 
- <span data-ttu-id="8a1b8-120">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8a1b8-120">Https</span></span> 
- <span data-ttu-id="8a1b8-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="8a1b8-121">StorageQueue</span></span> 
- <span data-ttu-id="8a1b8-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8a1b8-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="8a1b8-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8a1b8-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="8a1b8-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="8a1b8-124">-ExecutionCount</span></span>
<span data-ttu-id="8a1b8-125">Gibt an, wie oft der Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="8a1b8-126">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="8a1b8-127">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="8a1b8-127">-Frequency</span></span>
<span data-ttu-id="8a1b8-128">Gibt die maximale Häufigkeit für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="8a1b8-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a1b8-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a1b8-130">Minuten</span><span class="sxs-lookup"><span data-stu-id="8a1b8-130">Minute</span></span> 
- <span data-ttu-id="8a1b8-131">Stunde</span><span class="sxs-lookup"><span data-stu-id="8a1b8-131">Hour</span></span> 
- <span data-ttu-id="8a1b8-132">Tag</span><span class="sxs-lookup"><span data-stu-id="8a1b8-132">Day</span></span> 
- <span data-ttu-id="8a1b8-133">Woche</span><span class="sxs-lookup"><span data-stu-id="8a1b8-133">Week</span></span> 
- <span data-ttu-id="8a1b8-134">Monat</span><span class="sxs-lookup"><span data-stu-id="8a1b8-134">Month</span></span>

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

### <span data-ttu-id="8a1b8-135">-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-135">-Headers</span></span>
<span data-ttu-id="8a1b8-136">Gibt eine Hashtabelle an, die Überschriften enthält.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-136">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8a1b8-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="8a1b8-138">Gibt den HTTP-Authentifizierungs an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="8a1b8-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a1b8-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a1b8-140">Keine</span><span class="sxs-lookup"><span data-stu-id="8a1b8-140">None</span></span> 
- <span data-ttu-id="8a1b8-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a1b8-141">ClientCertificate</span></span> 
- <span data-ttu-id="8a1b8-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="8a1b8-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="8a1b8-143">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="8a1b8-143">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-144">-Intervall</span><span class="sxs-lookup"><span data-stu-id="8a1b8-144">-Interval</span></span>
<span data-ttu-id="8a1b8-145">Gibt ein Wiederholungsintervall für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="8a1b8-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8a1b8-146">-JobCollectionName</span></span>
<span data-ttu-id="8a1b8-147">Gibt den Namen der Auftrags Sammlung an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="8a1b8-148">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8a1b8-148">-JobName</span></span>
<span data-ttu-id="8a1b8-149">Gibt einen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="8a1b8-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="8a1b8-150">-JobState</span></span>
<span data-ttu-id="8a1b8-151">Gibt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-151">Specifies the state of the job.</span></span>
<span data-ttu-id="8a1b8-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a1b8-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a1b8-153">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="8a1b8-153">Enabled</span></span> 
- <span data-ttu-id="8a1b8-154">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="8a1b8-154">Disabled</span></span>

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

### <span data-ttu-id="8a1b8-155">-Methode</span><span class="sxs-lookup"><span data-stu-id="8a1b8-155">-Method</span></span>
<span data-ttu-id="8a1b8-156">Gibt die Methode für die Aktionstypen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="8a1b8-157">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a1b8-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a1b8-158">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8a1b8-158">GET</span></span> 
- <span data-ttu-id="8a1b8-159">Setzen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-159">PUT</span></span> 
- <span data-ttu-id="8a1b8-160">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-160">POST</span></span> 
- <span data-ttu-id="8a1b8-161">Löschen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="8a1b8-162">-RequestBody</span></span>
<span data-ttu-id="8a1b8-163">Gibt den Wert des Texts für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-163">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a1b8-164">-ResourceGroupName</span></span>
<span data-ttu-id="8a1b8-165">Gibt die Ressourcengruppe an, zu der der Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="8a1b8-166">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="8a1b8-166">-StartTime</span></span>
<span data-ttu-id="8a1b8-167">Gibt die Startzeit als **DateTime** -Objekt für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="8a1b8-168">-URI</span><span class="sxs-lookup"><span data-stu-id="8a1b8-168">-Uri</span></span>
<span data-ttu-id="8a1b8-169">Gibt einen URI für die Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-170">-Confirm</span></span>
<span data-ttu-id="8a1b8-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a1b8-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a1b8-172">-WhatIf</span></span>
<span data-ttu-id="8a1b8-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a1b8-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a1b8-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1b8-175">-DefaultProfile</span></span>
<span data-ttu-id="8a1b8-176">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a1b8-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1b8-177">CommonParameters</span></span>
<span data-ttu-id="8a1b8-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1b8-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1b8-179">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a1b8-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1b8-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a1b8-180">INPUTS</span></span>

## <span data-ttu-id="8a1b8-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a1b8-181">OUTPUTS</span></span>

### <span data-ttu-id="8a1b8-182">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8a1b8-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="8a1b8-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a1b8-183">NOTES</span></span>

## <span data-ttu-id="8a1b8-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a1b8-184">RELATED LINKS</span></span>

[<span data-ttu-id="8a1b8-185">Neu – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8a1b8-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8a1b8-186">Neu – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8a1b8-187">Neu – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8a1b8-188">Neu – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="8a1b8-189">Satz-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="8a1b8-190">Satz-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8a1b8-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8a1b8-191">Satz-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8a1b8-192">Satz-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8a1b8-193">Satz-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


