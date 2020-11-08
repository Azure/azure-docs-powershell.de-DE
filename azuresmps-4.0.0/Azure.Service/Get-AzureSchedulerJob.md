---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006517"
---
# <span data-ttu-id="616fc-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="616fc-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="616fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="616fc-102">SYNOPSIS</span></span>
<span data-ttu-id="616fc-103">Ruft eine Liste der Scheduler-Aufträge oder eines bestimmten Scheduler-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="616fc-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="616fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="616fc-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="616fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="616fc-105">DESCRIPTION</span></span>
<span data-ttu-id="616fc-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="616fc-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="616fc-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="616fc-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="616fc-108">Das Cmdlet " **Get-AzureSchedulerJobCollection** " Ruft eine Liste der Scheduler-Aufträge oder eines bestimmten Scheduler-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="616fc-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="616fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="616fc-109">EXAMPLES</span></span>

### <span data-ttu-id="616fc-110">Beispiel 1: Abrufen aller Aufträge in einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="616fc-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="616fc-111">Dieser Befehl ruft Scheduler-Aufträge ab, die Teil der Auftrags Sammlung mit dem Namen JobCollection01 sind.</span><span class="sxs-lookup"><span data-stu-id="616fc-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="616fc-112">Beispiel 2: Abrufen eines benannten Auftrags</span><span class="sxs-lookup"><span data-stu-id="616fc-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="616fc-113">Dieser Befehl ruft den Auftrag mit dem Namen Job01 aus der Sammlung mit dem Namen JobCollection01 an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="616fc-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="616fc-114">Beispiel 3: Abrufen von deaktivierten Aufträgen in einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="616fc-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="616fc-115">Dieser Befehl ruft alle deaktivierten Scheduler-Aufträge ab, die Teil von JobCollection01 an der angegebenen Position sind.</span><span class="sxs-lookup"><span data-stu-id="616fc-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="616fc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="616fc-116">PARAMETERS</span></span>

### <span data-ttu-id="616fc-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="616fc-117">-JobCollectionName</span></span>
<span data-ttu-id="616fc-118">Gibt den Namen der Sammlung an, die den abzurufenden Scheduler-Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="616fc-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="616fc-119">-Jobname</span><span class="sxs-lookup"><span data-stu-id="616fc-119">-JobName</span></span>
<span data-ttu-id="616fc-120">Gibt den Namen des abzurufenden Scheduler-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="616fc-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="616fc-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="616fc-121">-JobState</span></span>
<span data-ttu-id="616fc-122">Gibt den Zustand der abzurufenden Scheduler-Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="616fc-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="616fc-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="616fc-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="616fc-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="616fc-124">Enabled</span></span>
- <span data-ttu-id="616fc-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="616fc-125">Disabled</span></span>
- <span data-ttu-id="616fc-126">Faulted</span><span class="sxs-lookup"><span data-stu-id="616fc-126">Faulted</span></span>
- <span data-ttu-id="616fc-127">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="616fc-127">Completed</span></span>

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

### <span data-ttu-id="616fc-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="616fc-128">-Location</span></span>
<span data-ttu-id="616fc-129">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="616fc-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="616fc-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="616fc-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="616fc-131">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="616fc-131">Anywhere Asia</span></span>
- <span data-ttu-id="616fc-132">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="616fc-132">Anywhere Europe</span></span>
- <span data-ttu-id="616fc-133">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="616fc-133">Anywhere US</span></span>
- <span data-ttu-id="616fc-134">Ostasien</span><span class="sxs-lookup"><span data-stu-id="616fc-134">East Asia</span></span>
- <span data-ttu-id="616fc-135">East US</span><span class="sxs-lookup"><span data-stu-id="616fc-135">East US</span></span>
- <span data-ttu-id="616fc-136">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="616fc-136">North Central US</span></span>
- <span data-ttu-id="616fc-137">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="616fc-137">North Europe</span></span>
- <span data-ttu-id="616fc-138">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="616fc-138">South Central US</span></span>
- <span data-ttu-id="616fc-139">Südostasien</span><span class="sxs-lookup"><span data-stu-id="616fc-139">Southeast Asia</span></span>
- <span data-ttu-id="616fc-140">West Europa</span><span class="sxs-lookup"><span data-stu-id="616fc-140">West Europe</span></span>
- <span data-ttu-id="616fc-141">West-US</span><span class="sxs-lookup"><span data-stu-id="616fc-141">West US</span></span>

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

### <span data-ttu-id="616fc-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="616fc-142">-Profile</span></span>
<span data-ttu-id="616fc-143">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="616fc-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="616fc-144">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="616fc-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="616fc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616fc-145">CommonParameters</span></span>
<span data-ttu-id="616fc-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616fc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616fc-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616fc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616fc-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="616fc-148">INPUTS</span></span>

## <span data-ttu-id="616fc-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="616fc-149">OUTPUTS</span></span>

## <span data-ttu-id="616fc-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="616fc-150">NOTES</span></span>

## <span data-ttu-id="616fc-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="616fc-151">RELATED LINKS</span></span>

[<span data-ttu-id="616fc-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="616fc-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


