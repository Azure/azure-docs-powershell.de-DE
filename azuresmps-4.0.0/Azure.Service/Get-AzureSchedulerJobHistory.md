---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006516"
---
# <span data-ttu-id="97505-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="97505-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="97505-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97505-102">SYNOPSIS</span></span>
<span data-ttu-id="97505-103">Ruft den Verlauf eines Scheduler-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="97505-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="97505-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97505-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="97505-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97505-105">DESCRIPTION</span></span>
<span data-ttu-id="97505-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="97505-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="97505-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="97505-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="97505-108">Das Cmdlet " **Get-AzureSchedulerJobHistory** " Ruft das Protokoll für einen Scheduler-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="97505-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="97505-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97505-109">EXAMPLES</span></span>

### <span data-ttu-id="97505-110">Beispiel 1: Abrufen des Verlaufs für einen Auftrag mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="97505-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="97505-111">Mit diesem Befehl wird der Verlauf des Auftrags mit dem Namen Job01 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="97505-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="97505-112">Dieser Auftrag gehört zur Auftrags Sammlung mit dem Namen JobCollection01 an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="97505-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="97505-113">Beispiel 2: Abrufen des Verlaufs für einen fehlerhaften Auftrag mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="97505-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="97505-114">Dieser Befehl ruft den Verlauf des Auftrags mit dem Namen Job12 ab, der den Status Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="97505-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="97505-115">Dieser Auftrag gehört zur Auftrags Sammlung mit dem Namen JobCollection01 an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="97505-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="97505-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="97505-116">PARAMETERS</span></span>

### <span data-ttu-id="97505-117">-First</span><span class="sxs-lookup"><span data-stu-id="97505-117">-First</span></span>
<span data-ttu-id="97505-118">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="97505-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="97505-119">Geben Sie die Anzahl der abzurufenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="97505-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97505-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="97505-120">-IncludeTotalCount</span></span>
<span data-ttu-id="97505-121">Gibt die Gesamtzahl der Objekte in der Datengruppe (einer ganzen Zahl) an, gefolgt von den ausgewählten Objekten.</span><span class="sxs-lookup"><span data-stu-id="97505-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="97505-122">Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "unbekannte Gesamtanzahl" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="97505-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="97505-123">Die ganze Zahl verfügt über eine Genauigkeits Eigenschaft, die die Zuverlässigkeit des Gesamtanzahl Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="97505-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="97505-124">Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 eine zunehmend zuverlässige Schätzung angibt.</span><span class="sxs-lookup"><span data-stu-id="97505-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97505-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="97505-125">-JobCollectionName</span></span>
<span data-ttu-id="97505-126">Gibt den Namen einer Scheduler-Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="97505-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="97505-127">Dieses Cmdlet ruft das Protokoll für einen Auftrag ab, der zu der Sammlung gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="97505-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="97505-128">-Jobname</span><span class="sxs-lookup"><span data-stu-id="97505-128">-JobName</span></span>
<span data-ttu-id="97505-129">Gibt den Namen eines Scheduler-Auftrags an, für den der Verlauf abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="97505-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="97505-130">-Jobstatus</span><span class="sxs-lookup"><span data-stu-id="97505-130">-JobStatus</span></span>
<span data-ttu-id="97505-131">Gibt den Status des Scheduler-Auftrags an, für den der Verlauf abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="97505-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="97505-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="97505-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97505-133">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="97505-133">Completed</span></span>
- <span data-ttu-id="97505-134">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="97505-134">Failed</span></span>

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

### <span data-ttu-id="97505-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="97505-135">-Location</span></span>
<span data-ttu-id="97505-136">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="97505-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="97505-137">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="97505-137">Valid values are:</span></span> 

- <span data-ttu-id="97505-138">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="97505-138">Anywhere Asia</span></span>
- <span data-ttu-id="97505-139">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="97505-139">Anywhere Europe</span></span>
- <span data-ttu-id="97505-140">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="97505-140">Anywhere US</span></span>
- <span data-ttu-id="97505-141">Ostasien</span><span class="sxs-lookup"><span data-stu-id="97505-141">East Asia</span></span>
- <span data-ttu-id="97505-142">East US</span><span class="sxs-lookup"><span data-stu-id="97505-142">East US</span></span>
- <span data-ttu-id="97505-143">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="97505-143">North Central US</span></span>
- <span data-ttu-id="97505-144">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="97505-144">North Europe</span></span>
- <span data-ttu-id="97505-145">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="97505-145">South Central US</span></span>
- <span data-ttu-id="97505-146">Südostasien</span><span class="sxs-lookup"><span data-stu-id="97505-146">Southeast Asia</span></span>
- <span data-ttu-id="97505-147">West Europa</span><span class="sxs-lookup"><span data-stu-id="97505-147">West Europe</span></span>
- <span data-ttu-id="97505-148">West-US</span><span class="sxs-lookup"><span data-stu-id="97505-148">West US</span></span>

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

### <span data-ttu-id="97505-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="97505-149">-Profile</span></span>
<span data-ttu-id="97505-150">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="97505-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97505-151">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="97505-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97505-152">-Skip</span><span class="sxs-lookup"><span data-stu-id="97505-152">-Skip</span></span>
<span data-ttu-id="97505-153">Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="97505-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="97505-154">Geben Sie die Anzahl der zu überspringenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="97505-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97505-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97505-155">CommonParameters</span></span>
<span data-ttu-id="97505-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97505-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97505-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97505-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97505-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97505-158">INPUTS</span></span>

## <span data-ttu-id="97505-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97505-159">OUTPUTS</span></span>

## <span data-ttu-id="97505-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="97505-160">NOTES</span></span>

## <span data-ttu-id="97505-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97505-161">RELATED LINKS</span></span>

[<span data-ttu-id="97505-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="97505-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="97505-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="97505-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


