---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006005"
---
# <span data-ttu-id="2d0d0-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d0d0-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="2d0d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0d0-103">Aktualisiert einen Scheduler-Auftrag mit einer HTTP-Aktion.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="2d0d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d0d0-104">SYNTAX</span></span>

### <span data-ttu-id="2d0d0-105">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2d0d0-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d0d0-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="2d0d0-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2d0d0-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="2d0d0-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2d0d0-108">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="2d0d0-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d0d0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d0d0-109">DESCRIPTION</span></span>
<span data-ttu-id="2d0d0-110">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2d0d0-111">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2d0d0-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2d0d0-112">Das Cmdlet " **Satz-AzureSchedulerHttpJob** " aktualisiert einen Scheduler-Auftrag mit einer HTTP-Aktion.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="2d0d0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d0d0-113">EXAMPLES</span></span>

### <span data-ttu-id="2d0d0-114">Beispiel 1: Ändern des Status eines Auftrags in "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="2d0d0-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="2d0d0-115">Mit diesem Befehl wird der Status des Auftrags mit dem Namen Job01 in Disabled geändert.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="2d0d0-116">Dieser Auftrag ist Teil der Auftrags Sammlung mit dem Namen JobColleciton01 für den angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="2d0d0-117">Beispiel 2: Aktualisieren des URIs eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="2d0d0-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="2d0d0-118">Mit diesem Befehl wird der URI des Auftrags mit dem Namen Job01 aktualisiert http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="2d0d0-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="2d0d0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d0d0-119">PARAMETERS</span></span>

### <span data-ttu-id="2d0d0-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2d0d0-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="2d0d0-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="2d0d0-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="2d0d0-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2d0d0-122">-EndTime</span></span>
<span data-ttu-id="2d0d0-123">Gibt eine Uhrzeit als **DateTime** -Objekt an, damit der Planer das Initiieren von Aufträgen beendet.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="2d0d0-124">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="2d0d0-125">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2d0d0-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="2d0d0-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="2d0d0-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="2d0d0-127">Gibt Header als Hashtable an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="2d0d0-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="2d0d0-128">-ErrorActionMethod</span></span>
<span data-ttu-id="2d0d0-129">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="2d0d0-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2d0d0-130">Valid values are:</span></span> 

- <span data-ttu-id="2d0d0-131">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2d0d0-131">GET</span></span>
- <span data-ttu-id="2d0d0-132">Setzen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-132">PUT</span></span>
- <span data-ttu-id="2d0d0-133">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-133">POST</span></span>
- <span data-ttu-id="2d0d0-134">Kopf</span><span class="sxs-lookup"><span data-stu-id="2d0d0-134">HEAD</span></span>
- <span data-ttu-id="2d0d0-135">Löschen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-135">DELETE</span></span>

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

### <span data-ttu-id="2d0d0-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="2d0d0-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="2d0d0-137">Gibt den Text für die Speicher Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="2d0d0-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="2d0d0-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="2d0d0-139">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="2d0d0-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="2d0d0-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="2d0d0-141">Gibt das Shared Access-Signaturtoken (SAS) für die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="2d0d0-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d0d0-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="2d0d0-143">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="2d0d0-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d0d0-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="2d0d0-145">Gibt den Namen der Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="2d0d0-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="2d0d0-146">-ErrorActionURI</span></span>
<span data-ttu-id="2d0d0-147">Gibt den URI für die Fehler Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="2d0d0-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="2d0d0-148">-ExecutionCount</span></span>
<span data-ttu-id="2d0d0-149">Gibt die Anzahl der Vorkommen eines Auftrags an, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="2d0d0-150">Standardmäßig wird ein Auftrag auf unbestimmte Zeit wiederholt.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="2d0d0-151">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="2d0d0-151">-Frequency</span></span>
<span data-ttu-id="2d0d0-152">Gibt die maximale Häufigkeit für diesen Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="2d0d0-153">-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-153">-Headers</span></span>
<span data-ttu-id="2d0d0-154">Gibt die Kopfzeilen als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="2d0d0-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2d0d0-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="2d0d0-156">-Intervall</span><span class="sxs-lookup"><span data-stu-id="2d0d0-156">-Interval</span></span>
<span data-ttu-id="2d0d0-157">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="2d0d0-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2d0d0-158">-JobCollectionName</span></span>
<span data-ttu-id="2d0d0-159">Gibt den Namen der Sammlung an, die den zu ändernden Scheduler-Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="2d0d0-160">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2d0d0-160">-JobName</span></span>
<span data-ttu-id="2d0d0-161">Gibt den Namen des zu ändernden Scheduler-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="2d0d0-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="2d0d0-162">-JobState</span></span>
<span data-ttu-id="2d0d0-163">Gibt den Status für den Scheduler-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="2d0d0-164">-Standort</span><span class="sxs-lookup"><span data-stu-id="2d0d0-164">-Location</span></span>
<span data-ttu-id="2d0d0-165">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="2d0d0-166">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2d0d0-166">Valid values are:</span></span> 

- <span data-ttu-id="2d0d0-167">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="2d0d0-167">Anywhere Asia</span></span>
- <span data-ttu-id="2d0d0-168">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="2d0d0-168">Anywhere Europe</span></span>
- <span data-ttu-id="2d0d0-169">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="2d0d0-169">Anywhere US</span></span>
- <span data-ttu-id="2d0d0-170">Ostasien</span><span class="sxs-lookup"><span data-stu-id="2d0d0-170">East Asia</span></span>
- <span data-ttu-id="2d0d0-171">East US</span><span class="sxs-lookup"><span data-stu-id="2d0d0-171">East US</span></span>
- <span data-ttu-id="2d0d0-172">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="2d0d0-172">North Central US</span></span>
- <span data-ttu-id="2d0d0-173">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="2d0d0-173">North Europe</span></span>
- <span data-ttu-id="2d0d0-174">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="2d0d0-174">South Central US</span></span>
- <span data-ttu-id="2d0d0-175">Südostasien</span><span class="sxs-lookup"><span data-stu-id="2d0d0-175">Southeast Asia</span></span>
- <span data-ttu-id="2d0d0-176">West Europa</span><span class="sxs-lookup"><span data-stu-id="2d0d0-176">West Europe</span></span>
- <span data-ttu-id="2d0d0-177">West-US</span><span class="sxs-lookup"><span data-stu-id="2d0d0-177">West US</span></span>

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

### <span data-ttu-id="2d0d0-178">-Methode</span><span class="sxs-lookup"><span data-stu-id="2d0d0-178">-Method</span></span>
<span data-ttu-id="2d0d0-179">Gibt die Methode für http-und HTTPS-Aktionstypen an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="2d0d0-180">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2d0d0-180">Valid values are:</span></span> 

- <span data-ttu-id="2d0d0-181">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2d0d0-181">GET</span></span>
- <span data-ttu-id="2d0d0-182">Setzen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-182">PUT</span></span>
- <span data-ttu-id="2d0d0-183">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-183">POST</span></span>
- <span data-ttu-id="2d0d0-184">Kopf</span><span class="sxs-lookup"><span data-stu-id="2d0d0-184">HEAD</span></span>
- <span data-ttu-id="2d0d0-185">Löschen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-185">DELETE</span></span>

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

### <span data-ttu-id="2d0d0-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d0d0-186">-PassThru</span></span>
<span data-ttu-id="2d0d0-187">Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="2d0d0-188">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d0d0-189">-Profil</span><span class="sxs-lookup"><span data-stu-id="2d0d0-189">-Profile</span></span>
<span data-ttu-id="2d0d0-190">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d0d0-191">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d0d0-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="2d0d0-192">-RequestBody</span></span>
<span data-ttu-id="2d0d0-193">Gibt den Textkörper für Put-und Post-Auftragsaktionen an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="2d0d0-194">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="2d0d0-194">-StartTime</span></span>
<span data-ttu-id="2d0d0-195">Gibt eine Uhrzeit als **DateTime** -Objekt für den Start des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="2d0d0-196">-URI</span><span class="sxs-lookup"><span data-stu-id="2d0d0-196">-URI</span></span>
<span data-ttu-id="2d0d0-197">Gibt einen URI für eine Auftragsaktion an.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="2d0d0-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0d0-198">CommonParameters</span></span>
<span data-ttu-id="2d0d0-199">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d0d0-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0d0-200">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d0d0-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0d0-201">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d0d0-201">INPUTS</span></span>

## <span data-ttu-id="2d0d0-202">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d0d0-202">OUTPUTS</span></span>

## <span data-ttu-id="2d0d0-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d0d0-203">NOTES</span></span>

## <span data-ttu-id="2d0d0-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d0d0-204">RELATED LINKS</span></span>

[<span data-ttu-id="2d0d0-205">Neu – AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d0d0-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


