---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006256"
---
# <span data-ttu-id="9df0d-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9df0d-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="9df0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9df0d-102">SYNOPSIS</span></span>
<span data-ttu-id="9df0d-103">Aktualisiert einen Scheduler-Auftrag mit einer Speicheraktion.</span><span class="sxs-lookup"><span data-stu-id="9df0d-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="9df0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9df0d-104">SYNTAX</span></span>

### <span data-ttu-id="9df0d-105">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9df0d-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9df0d-106">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="9df0d-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9df0d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9df0d-107">DESCRIPTION</span></span>
<span data-ttu-id="9df0d-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9df0d-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9df0d-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9df0d-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9df0d-110">Das Cmdlet " **Satz-AzureSchedulerStorageQueueJob** " aktualisiert einen Scheduler-Auftrag mit einer Azure-Speicheraktion.</span><span class="sxs-lookup"><span data-stu-id="9df0d-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="9df0d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9df0d-111">EXAMPLES</span></span>

### <span data-ttu-id="9df0d-112">Beispiel 1: Aktualisieren einer Speicher Warteschlangen Nachricht</span><span class="sxs-lookup"><span data-stu-id="9df0d-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="9df0d-113">Mit diesem Befehl wird die Warteschlangen Meldung für den Speicherauftrag mit dem Namen Job12 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9df0d-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="9df0d-114">Der Befehl gibt den Namen der Auftrags Sammlung und den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="9df0d-115">Beispiel 2: Aktivieren eines Speicher Warteschlangenauftrags</span><span class="sxs-lookup"><span data-stu-id="9df0d-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="9df0d-116">Mit diesem Befehl wird der Auftrag mit dem Namen Job16 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9df0d-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="9df0d-117">Der Befehl ändert den Zustand des Auftrags in enabled, indem dieser Wert für den *JobState* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9df0d-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="9df0d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9df0d-118">PARAMETERS</span></span>

### <span data-ttu-id="9df0d-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9df0d-119">-EndTime</span></span>
<span data-ttu-id="9df0d-120">Gibt eine Uhrzeit als **DateTime** -Objekt an, damit der Planer den Auftrag nicht mehr initiieren kann.</span><span class="sxs-lookup"><span data-stu-id="9df0d-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="9df0d-121">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9df0d-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="9df0d-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9df0d-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="9df0d-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="9df0d-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="9df0d-124">Gibt Header als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="9df0d-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="9df0d-125">-ErrorActionMethod</span></span>
<span data-ttu-id="9df0d-126">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="9df0d-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9df0d-127">Valid values are:</span></span> 

- <span data-ttu-id="9df0d-128">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9df0d-128">GET</span></span>
- <span data-ttu-id="9df0d-129">Setzen</span><span class="sxs-lookup"><span data-stu-id="9df0d-129">PUT</span></span>
- <span data-ttu-id="9df0d-130">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="9df0d-130">POST</span></span>
- <span data-ttu-id="9df0d-131">Kopf</span><span class="sxs-lookup"><span data-stu-id="9df0d-131">HEAD</span></span>
- <span data-ttu-id="9df0d-132">Löschen</span><span class="sxs-lookup"><span data-stu-id="9df0d-132">DELETE</span></span>

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

### <span data-ttu-id="9df0d-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="9df0d-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="9df0d-134">Gibt den Text für die Speicher Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="9df0d-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="9df0d-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="9df0d-136">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="9df0d-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="9df0d-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="9df0d-138">Gibt das Shared Access-Signaturtoken (SAS) für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="9df0d-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9df0d-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="9df0d-140">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9df0d-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9df0d-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="9df0d-142">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="9df0d-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="9df0d-143">-ErrorActionURI</span></span>
<span data-ttu-id="9df0d-144">Gibt den URI für die Fehler Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="9df0d-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="9df0d-145">-ExecutionCount</span></span>
<span data-ttu-id="9df0d-146">Gibt die Anzahl der Vorkommen eines Auftrags an, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9df0d-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="9df0d-147">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="9df0d-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="9df0d-148">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="9df0d-148">-Frequency</span></span>
<span data-ttu-id="9df0d-149">Gibt die maximale Häufigkeit für diesen Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="9df0d-150">-Intervall</span><span class="sxs-lookup"><span data-stu-id="9df0d-150">-Interval</span></span>
<span data-ttu-id="9df0d-151">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9df0d-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="9df0d-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9df0d-152">-JobCollectionName</span></span>
<span data-ttu-id="9df0d-153">Gibt den Namen der Sammlung an, die den Scheduler-Job enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="9df0d-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="9df0d-154">-Jobname</span><span class="sxs-lookup"><span data-stu-id="9df0d-154">-JobName</span></span>
<span data-ttu-id="9df0d-155">Gibt den Namen des Scheduler-Auftrags an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9df0d-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="9df0d-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="9df0d-156">-JobState</span></span>
<span data-ttu-id="9df0d-157">Gibt den Status für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="9df0d-158">-Standort</span><span class="sxs-lookup"><span data-stu-id="9df0d-158">-Location</span></span>
<span data-ttu-id="9df0d-159">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="9df0d-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="9df0d-160">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9df0d-160">Valid values are:</span></span> 

- <span data-ttu-id="9df0d-161">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="9df0d-161">Anywhere Asia</span></span>
- <span data-ttu-id="9df0d-162">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="9df0d-162">Anywhere Europe</span></span>
- <span data-ttu-id="9df0d-163">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="9df0d-163">Anywhere US</span></span>
- <span data-ttu-id="9df0d-164">Ostasien</span><span class="sxs-lookup"><span data-stu-id="9df0d-164">East Asia</span></span>
- <span data-ttu-id="9df0d-165">East US</span><span class="sxs-lookup"><span data-stu-id="9df0d-165">East US</span></span>
- <span data-ttu-id="9df0d-166">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="9df0d-166">North Central US</span></span>
- <span data-ttu-id="9df0d-167">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="9df0d-167">North Europe</span></span>
- <span data-ttu-id="9df0d-168">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="9df0d-168">South Central US</span></span>
- <span data-ttu-id="9df0d-169">Südostasien</span><span class="sxs-lookup"><span data-stu-id="9df0d-169">Southeast Asia</span></span>
- <span data-ttu-id="9df0d-170">West Europa</span><span class="sxs-lookup"><span data-stu-id="9df0d-170">West Europe</span></span>
- <span data-ttu-id="9df0d-171">West-US</span><span class="sxs-lookup"><span data-stu-id="9df0d-171">West US</span></span>

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

### <span data-ttu-id="9df0d-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9df0d-172">-PassThru</span></span>
<span data-ttu-id="9df0d-173">Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9df0d-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="9df0d-174">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9df0d-174">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df0d-175">-Profil</span><span class="sxs-lookup"><span data-stu-id="9df0d-175">-Profile</span></span>
<span data-ttu-id="9df0d-176">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9df0d-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9df0d-177">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9df0d-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9df0d-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="9df0d-178">-SASToken</span></span>
<span data-ttu-id="9df0d-179">Gibt das SAS-Token für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="9df0d-180">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="9df0d-180">-StartTime</span></span>
<span data-ttu-id="9df0d-181">Gibt eine Uhrzeit als **DateTime** -Objekt für den Start des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="9df0d-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="9df0d-182">-StorageQueueAccount</span></span>
<span data-ttu-id="9df0d-183">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="9df0d-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="9df0d-184">-StorageQueueMessage</span></span>
<span data-ttu-id="9df0d-185">Gibt die Warteschlangen Meldung für den Speicherauftrag an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="9df0d-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="9df0d-186">-StorageQueueName</span></span>
<span data-ttu-id="9df0d-187">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="9df0d-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="9df0d-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df0d-188">CommonParameters</span></span>
<span data-ttu-id="9df0d-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df0d-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df0d-190">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df0d-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df0d-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9df0d-191">INPUTS</span></span>

## <span data-ttu-id="9df0d-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9df0d-192">OUTPUTS</span></span>

## <span data-ttu-id="9df0d-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="9df0d-193">NOTES</span></span>

## <span data-ttu-id="9df0d-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9df0d-194">RELATED LINKS</span></span>

[<span data-ttu-id="9df0d-195">Neu – AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9df0d-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


