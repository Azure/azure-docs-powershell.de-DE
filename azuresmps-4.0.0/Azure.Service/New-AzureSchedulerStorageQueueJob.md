---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006108"
---
# <span data-ttu-id="26347-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="26347-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="26347-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26347-102">SYNOPSIS</span></span>
<span data-ttu-id="26347-103">Erstellt einen Scheduler-Auftrag mit einer Speicheraktion.</span><span class="sxs-lookup"><span data-stu-id="26347-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="26347-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26347-104">SYNTAX</span></span>

### <span data-ttu-id="26347-105">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="26347-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="26347-106">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="26347-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26347-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26347-107">DESCRIPTION</span></span>
<span data-ttu-id="26347-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="26347-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="26347-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="26347-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="26347-110">Das Cmdlet **New-AzureSchedulerStorageQueueJob** erstellt einen Scheduler-Auftrag mit einer Azure-Speicheraktion.</span><span class="sxs-lookup"><span data-stu-id="26347-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="26347-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26347-111">EXAMPLES</span></span>

### <span data-ttu-id="26347-112">Beispiel 1: Erstellen eines einmal ausgeführten Speicher Auftrags</span><span class="sxs-lookup"><span data-stu-id="26347-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="26347-113">Dieser Befehl erstellt einen Scheduler-Speicherauftrag als Teil der Sammlung mit dem Namen JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="26347-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="26347-114">Der Befehl gibt das Speicherkonto, den Warteschlangennamen und das SAS-Token an.</span><span class="sxs-lookup"><span data-stu-id="26347-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="26347-115">Der Auftrag wird sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26347-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="26347-116">Beispiel 2: Erstellen eines Speicher Auftrags, der eine bestimmte Anzahl von Zeiten ausführt</span><span class="sxs-lookup"><span data-stu-id="26347-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="26347-117">Dieser Befehl erstellt einen Scheduler-Speicherauftrag als Teil der Sammlung mit dem Namen JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="26347-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="26347-118">Der Befehl gibt das Speicherkonto, den Warteschlangennamen und das SAS-Token an.</span><span class="sxs-lookup"><span data-stu-id="26347-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="26347-119">Der Auftrag wird insgesamt 20 Mal pro Stunde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26347-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="26347-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="26347-120">PARAMETERS</span></span>

### <span data-ttu-id="26347-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="26347-121">-EndTime</span></span>
<span data-ttu-id="26347-122">Gibt eine Uhrzeit als **DateTime** -Objekt an, damit der Planer den Auftrag nicht mehr initiieren kann.</span><span class="sxs-lookup"><span data-stu-id="26347-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="26347-123">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="26347-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="26347-124">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="26347-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="26347-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="26347-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="26347-126">Gibt Header als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="26347-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="26347-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="26347-127">-ErrorActionMethod</span></span>
<span data-ttu-id="26347-128">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="26347-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="26347-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="26347-129">Valid values are:</span></span> 

- <span data-ttu-id="26347-130">Erhalten</span><span class="sxs-lookup"><span data-stu-id="26347-130">GET</span></span>
- <span data-ttu-id="26347-131">Setzen</span><span class="sxs-lookup"><span data-stu-id="26347-131">PUT</span></span>
- <span data-ttu-id="26347-132">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="26347-132">POST</span></span>
- <span data-ttu-id="26347-133">Kopf</span><span class="sxs-lookup"><span data-stu-id="26347-133">HEAD</span></span>
- <span data-ttu-id="26347-134">Löschen</span><span class="sxs-lookup"><span data-stu-id="26347-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="26347-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="26347-136">Gibt den Text für die Speicher Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="26347-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="26347-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="26347-138">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="26347-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="26347-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="26347-140">Gibt das Shared Access-Signaturtoken (SAS) für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="26347-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26347-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="26347-142">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="26347-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="26347-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="26347-144">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="26347-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="26347-145">-ErrorActionURI</span></span>
<span data-ttu-id="26347-146">Gibt den URI für die Fehler Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="26347-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="26347-147">-ExecutionCount</span></span>
<span data-ttu-id="26347-148">Gibt die Anzahl der Vorkommen eines Auftrags an, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="26347-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="26347-149">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="26347-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="26347-150">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="26347-150">-Frequency</span></span>
<span data-ttu-id="26347-151">Gibt die maximale Häufigkeit für diesen Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="26347-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="26347-152">-Intervall</span><span class="sxs-lookup"><span data-stu-id="26347-152">-Interval</span></span>
<span data-ttu-id="26347-153">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="26347-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="26347-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="26347-154">-JobCollectionName</span></span>
<span data-ttu-id="26347-155">Gibt den Namen der Sammlung an, die den Scheduler-Job enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="26347-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-156">-Jobname</span><span class="sxs-lookup"><span data-stu-id="26347-156">-JobName</span></span>
<span data-ttu-id="26347-157">Gibt den Namen für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="26347-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="26347-158">-JobState</span></span>
<span data-ttu-id="26347-159">Gibt den Status für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="26347-159">Specifies the state for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-160">-Standort</span><span class="sxs-lookup"><span data-stu-id="26347-160">-Location</span></span>
<span data-ttu-id="26347-161">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="26347-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="26347-162">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="26347-162">Valid values are:</span></span> 

- <span data-ttu-id="26347-163">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="26347-163">Anywhere Asia</span></span>
- <span data-ttu-id="26347-164">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="26347-164">Anywhere Europe</span></span>
- <span data-ttu-id="26347-165">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="26347-165">Anywhere US</span></span>
- <span data-ttu-id="26347-166">Ostasien</span><span class="sxs-lookup"><span data-stu-id="26347-166">East Asia</span></span>
- <span data-ttu-id="26347-167">East US</span><span class="sxs-lookup"><span data-stu-id="26347-167">East US</span></span>
- <span data-ttu-id="26347-168">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="26347-168">North Central US</span></span>
- <span data-ttu-id="26347-169">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="26347-169">North Europe</span></span>
- <span data-ttu-id="26347-170">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="26347-170">South Central US</span></span>
- <span data-ttu-id="26347-171">Südostasien</span><span class="sxs-lookup"><span data-stu-id="26347-171">Southeast Asia</span></span>
- <span data-ttu-id="26347-172">West Europa</span><span class="sxs-lookup"><span data-stu-id="26347-172">West Europe</span></span>
- <span data-ttu-id="26347-173">West-US</span><span class="sxs-lookup"><span data-stu-id="26347-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-174">-Profil</span><span class="sxs-lookup"><span data-stu-id="26347-174">-Profile</span></span>
<span data-ttu-id="26347-175">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="26347-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26347-176">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="26347-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="26347-177">-SASToken</span></span>
<span data-ttu-id="26347-178">Gibt das SAS-Token für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="26347-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-179">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="26347-179">-StartTime</span></span>
<span data-ttu-id="26347-180">Gibt eine Uhrzeit als **DateTime** -Objekt für den Start des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="26347-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26347-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="26347-181">-StorageQueueAccount</span></span>
<span data-ttu-id="26347-182">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="26347-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="26347-183">-StorageQueueMessage</span></span>
<span data-ttu-id="26347-184">Gibt die Warteschlangen Meldung für den Speicherauftrag an.</span><span class="sxs-lookup"><span data-stu-id="26347-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="26347-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="26347-185">-StorageQueueName</span></span>
<span data-ttu-id="26347-186">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="26347-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26347-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26347-187">CommonParameters</span></span>
<span data-ttu-id="26347-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26347-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26347-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26347-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26347-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26347-190">INPUTS</span></span>

## <span data-ttu-id="26347-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26347-191">OUTPUTS</span></span>

## <span data-ttu-id="26347-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="26347-192">NOTES</span></span>

## <span data-ttu-id="26347-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26347-193">RELATED LINKS</span></span>

[<span data-ttu-id="26347-194">Satz-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="26347-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


