---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006110"
---
# <span data-ttu-id="7f804-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7f804-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="7f804-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f804-102">SYNOPSIS</span></span>
<span data-ttu-id="7f804-103">Erstellt einen Scheduler-Auftrag mit einer HTTP-Aktion.</span><span class="sxs-lookup"><span data-stu-id="7f804-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="7f804-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f804-104">SYNTAX</span></span>

### <span data-ttu-id="7f804-105">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f804-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f804-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="7f804-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7f804-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="7f804-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7f804-108">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7f804-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f804-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f804-109">DESCRIPTION</span></span>
<span data-ttu-id="7f804-110">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f804-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7f804-111">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7f804-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7f804-112">Das Cmdlet **New-AzureSchedulerHttpJob** erstellt einen Scheduler-Auftrag mit einer HTTP-Aktion.</span><span class="sxs-lookup"><span data-stu-id="7f804-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="7f804-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f804-113">EXAMPLES</span></span>

### <span data-ttu-id="7f804-114">Beispiel 1: Erstellen eines HTTP-Auftrags</span><span class="sxs-lookup"><span data-stu-id="7f804-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="7f804-115">Dieser Befehl erstellt einen Scheduler-http-Auftrag in der Auftrags Sammlung mit dem Namen JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="7f804-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="7f804-116">Der Befehl gibt einen URI an und gibt Get als Methode an.</span><span class="sxs-lookup"><span data-stu-id="7f804-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="7f804-117">Beispiel 2: Erstellen eines HTTP-Auftrags für eine bestimmte Ausführungsanzahl</span><span class="sxs-lookup"><span data-stu-id="7f804-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="7f804-118">Dieser Befehl erstellt den Scheduler http-Job in der Job-Sammlung mit dem Namen JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="7f804-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="7f804-119">Der Befehl gibt einen URI an und gibt Get als Methode an.</span><span class="sxs-lookup"><span data-stu-id="7f804-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="7f804-120">Dieser Befehl bewirkt, dass der Auftrag 20 Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f804-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="7f804-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f804-121">PARAMETERS</span></span>

### <span data-ttu-id="7f804-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7f804-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="7f804-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7f804-124">-EndTime</span></span>
<span data-ttu-id="7f804-125">Gibt eine Uhrzeit als **DateTime** -Objekt an, damit der Planer das Initiieren von Aufträgen beendet.</span><span class="sxs-lookup"><span data-stu-id="7f804-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="7f804-126">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f804-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7f804-127">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7f804-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="7f804-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="7f804-129">Gibt Header als Hashtable an.</span><span class="sxs-lookup"><span data-stu-id="7f804-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="7f804-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="7f804-130">-ErrorActionMethod</span></span>
<span data-ttu-id="7f804-131">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="7f804-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="7f804-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7f804-132">Valid values are:</span></span> 

- <span data-ttu-id="7f804-133">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7f804-133">GET</span></span>
- <span data-ttu-id="7f804-134">Setzen</span><span class="sxs-lookup"><span data-stu-id="7f804-134">PUT</span></span>
- <span data-ttu-id="7f804-135">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="7f804-135">POST</span></span>
- <span data-ttu-id="7f804-136">Kopf</span><span class="sxs-lookup"><span data-stu-id="7f804-136">HEAD</span></span>
- <span data-ttu-id="7f804-137">Löschen</span><span class="sxs-lookup"><span data-stu-id="7f804-137">DELETE</span></span>

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

### <span data-ttu-id="7f804-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="7f804-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="7f804-139">Gibt den Text für die Speicher Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="7f804-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="7f804-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="7f804-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="7f804-141">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="7f804-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="7f804-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="7f804-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="7f804-143">Gibt das Shared Access-Signaturtoken (SAS) für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="7f804-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="7f804-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7f804-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="7f804-145">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="7f804-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="7f804-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7f804-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="7f804-147">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="7f804-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="7f804-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="7f804-148">-ErrorActionURI</span></span>
<span data-ttu-id="7f804-149">Gibt den URI für die Fehler Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="7f804-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="7f804-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="7f804-150">-ExecutionCount</span></span>
<span data-ttu-id="7f804-151">Gibt die Anzahl der Vorkommen eines Auftrags an, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7f804-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="7f804-152">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="7f804-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-153">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="7f804-153">-Frequency</span></span>
<span data-ttu-id="7f804-154">Gibt die maximale Häufigkeit für diesen Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="7f804-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-155">-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="7f804-155">-Headers</span></span>
<span data-ttu-id="7f804-156">Gibt die Kopfzeilen als Hashtable an.</span><span class="sxs-lookup"><span data-stu-id="7f804-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="7f804-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="7f804-157">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-158">-Intervall</span><span class="sxs-lookup"><span data-stu-id="7f804-158">-Interval</span></span>
<span data-ttu-id="7f804-159">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f804-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7f804-160">-JobCollectionName</span></span>
<span data-ttu-id="7f804-161">Gibt den Namen der Sammlung an, die den Scheduler-Job enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7f804-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="7f804-162">-Jobname</span><span class="sxs-lookup"><span data-stu-id="7f804-162">-JobName</span></span>
<span data-ttu-id="7f804-163">Gibt den Namen für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="7f804-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="7f804-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="7f804-164">-JobState</span></span>
<span data-ttu-id="7f804-165">Gibt den Status für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="7f804-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="7f804-166">-Standort</span><span class="sxs-lookup"><span data-stu-id="7f804-166">-Location</span></span>
<span data-ttu-id="7f804-167">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="7f804-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="7f804-168">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7f804-168">Valid values are:</span></span> 

- <span data-ttu-id="7f804-169">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="7f804-169">Anywhere Asia</span></span>
- <span data-ttu-id="7f804-170">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="7f804-170">Anywhere Europe</span></span>
- <span data-ttu-id="7f804-171">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="7f804-171">Anywhere US</span></span>
- <span data-ttu-id="7f804-172">Ostasien</span><span class="sxs-lookup"><span data-stu-id="7f804-172">East Asia</span></span>
- <span data-ttu-id="7f804-173">East US</span><span class="sxs-lookup"><span data-stu-id="7f804-173">East US</span></span>
- <span data-ttu-id="7f804-174">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="7f804-174">North Central US</span></span>
- <span data-ttu-id="7f804-175">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="7f804-175">North Europe</span></span>
- <span data-ttu-id="7f804-176">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="7f804-176">South Central US</span></span>
- <span data-ttu-id="7f804-177">Südostasien</span><span class="sxs-lookup"><span data-stu-id="7f804-177">Southeast Asia</span></span>
- <span data-ttu-id="7f804-178">West Europa</span><span class="sxs-lookup"><span data-stu-id="7f804-178">West Europe</span></span>
- <span data-ttu-id="7f804-179">West-US</span><span class="sxs-lookup"><span data-stu-id="7f804-179">West US</span></span>

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

### <span data-ttu-id="7f804-180">-Methode</span><span class="sxs-lookup"><span data-stu-id="7f804-180">-Method</span></span>
<span data-ttu-id="7f804-181">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="7f804-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="7f804-182">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7f804-182">Valid values are:</span></span> 

- <span data-ttu-id="7f804-183">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7f804-183">GET</span></span>
- <span data-ttu-id="7f804-184">Setzen</span><span class="sxs-lookup"><span data-stu-id="7f804-184">PUT</span></span>
- <span data-ttu-id="7f804-185">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="7f804-185">POST</span></span>
- <span data-ttu-id="7f804-186">Kopf</span><span class="sxs-lookup"><span data-stu-id="7f804-186">HEAD</span></span>
- <span data-ttu-id="7f804-187">Löschen</span><span class="sxs-lookup"><span data-stu-id="7f804-187">DELETE</span></span>

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

### <span data-ttu-id="7f804-188">-Profil</span><span class="sxs-lookup"><span data-stu-id="7f804-188">-Profile</span></span>
<span data-ttu-id="7f804-189">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7f804-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f804-190">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7f804-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f804-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="7f804-191">-RequestBody</span></span>
<span data-ttu-id="7f804-192">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="7f804-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-193">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="7f804-193">-StartTime</span></span>
<span data-ttu-id="7f804-194">Gibt eine Uhrzeit als **DateTime** -Objekt für den Start des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="7f804-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="7f804-195">-URI</span><span class="sxs-lookup"><span data-stu-id="7f804-195">-URI</span></span>
<span data-ttu-id="7f804-196">Gibt einen URI für eine Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="7f804-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f804-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f804-197">CommonParameters</span></span>
<span data-ttu-id="7f804-198">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f804-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f804-199">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f804-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f804-200">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f804-200">INPUTS</span></span>

## <span data-ttu-id="7f804-201">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f804-201">OUTPUTS</span></span>

## <span data-ttu-id="7f804-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f804-202">NOTES</span></span>

## <span data-ttu-id="7f804-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f804-203">RELATED LINKS</span></span>

[<span data-ttu-id="7f804-204">Satz-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7f804-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


