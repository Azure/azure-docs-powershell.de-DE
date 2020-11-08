---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006186"
---
# <span data-ttu-id="9096e-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9096e-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="9096e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9096e-102">SYNOPSIS</span></span>
<span data-ttu-id="9096e-103">Erstellt eine Scheduler-Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="9096e-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="9096e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9096e-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9096e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9096e-105">DESCRIPTION</span></span>
<span data-ttu-id="9096e-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9096e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9096e-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9096e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9096e-108">Das Cmdlet **New-AzureSchedulerJobCollection** erstellt eine Scheduler-Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="9096e-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="9096e-109">Wenn Sie keinen Wert für den *Plan* -Parameter angeben, erstellt das Cmdlet eine Standardauftrags Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9096e-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="9096e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9096e-110">EXAMPLES</span></span>

### <span data-ttu-id="9096e-111">Beispiel 1: Erstellen einer Scheduler-Auftrags Sammlung mit Standardwerten</span><span class="sxs-lookup"><span data-stu-id="9096e-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="9096e-112">Dieser Befehl erstellt eine standardmäßige Scheduler-Auftrags Sammlung mit dem Namen JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="9096e-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="9096e-113">Die neue Sammlung verfügt über eine Standardauftrags Anzahl und maximale Serienwerte für eine standardmäßige Aufgabenauflistung des Schedulers.</span><span class="sxs-lookup"><span data-stu-id="9096e-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="9096e-114">Beispiel 2: Erstellen einer Scheduler-Auftrags Sammlung mit angegebenen Werten</span><span class="sxs-lookup"><span data-stu-id="9096e-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="9096e-115">Dieser Befehl erstellt eine standardmäßige Scheduler-Auftrags Sammlung mit dem Namen JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="9096e-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="9096e-116">Die neue Sammlung hat eine maximale Auftragsanzahl von 30 und ein maximales wieder auftreten von 12 pro Stunde.</span><span class="sxs-lookup"><span data-stu-id="9096e-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="9096e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9096e-117">PARAMETERS</span></span>

### <span data-ttu-id="9096e-118">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="9096e-118">-Frequency</span></span>
<span data-ttu-id="9096e-119">Gibt die maximale Häufigkeit an, die für einen beliebigen Job in dieser Scheduler-Auftrags Sammlung angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9096e-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

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

### <span data-ttu-id="9096e-120">-Intervall</span><span class="sxs-lookup"><span data-stu-id="9096e-120">-Interval</span></span>
<span data-ttu-id="9096e-121">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9096e-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="9096e-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9096e-122">-JobCollectionName</span></span>
<span data-ttu-id="9096e-123">Gibt den Namen der neuen Scheduler-Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="9096e-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="9096e-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="9096e-124">-Location</span></span>
<span data-ttu-id="9096e-125">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="9096e-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="9096e-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9096e-126">Valid values are:</span></span> 

- <span data-ttu-id="9096e-127">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="9096e-127">Anywhere Asia</span></span>
- <span data-ttu-id="9096e-128">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="9096e-128">Anywhere Europe</span></span>
- <span data-ttu-id="9096e-129">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="9096e-129">Anywhere US</span></span>
- <span data-ttu-id="9096e-130">Ostasien</span><span class="sxs-lookup"><span data-stu-id="9096e-130">East Asia</span></span>
- <span data-ttu-id="9096e-131">East US</span><span class="sxs-lookup"><span data-stu-id="9096e-131">East US</span></span>
- <span data-ttu-id="9096e-132">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="9096e-132">North Central US</span></span>
- <span data-ttu-id="9096e-133">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="9096e-133">North Europe</span></span>
- <span data-ttu-id="9096e-134">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="9096e-134">South Central US</span></span>
- <span data-ttu-id="9096e-135">Südostasien</span><span class="sxs-lookup"><span data-stu-id="9096e-135">Southeast Asia</span></span>
- <span data-ttu-id="9096e-136">West Europa</span><span class="sxs-lookup"><span data-stu-id="9096e-136">West Europe</span></span>
- <span data-ttu-id="9096e-137">West-US</span><span class="sxs-lookup"><span data-stu-id="9096e-137">West US</span></span>

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

### <span data-ttu-id="9096e-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="9096e-138">-MaxJobCount</span></span>
<span data-ttu-id="9096e-139">Gibt die maximale Anzahl von Aufträgen an, die in der Scheduler-Auftrags Sammlung erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="9096e-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="9096e-140">-Plan</span><span class="sxs-lookup"><span data-stu-id="9096e-140">-Plan</span></span>
<span data-ttu-id="9096e-141">Gibt den Plan des Scheduler-Auftrags Sammlungs Plans an.</span><span class="sxs-lookup"><span data-stu-id="9096e-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="9096e-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="9096e-142">-Profile</span></span>
<span data-ttu-id="9096e-143">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9096e-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9096e-144">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9096e-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9096e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9096e-145">CommonParameters</span></span>
<span data-ttu-id="9096e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9096e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9096e-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9096e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9096e-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9096e-148">INPUTS</span></span>

## <span data-ttu-id="9096e-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9096e-149">OUTPUTS</span></span>

## <span data-ttu-id="9096e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="9096e-150">NOTES</span></span>

## <span data-ttu-id="9096e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9096e-151">RELATED LINKS</span></span>

[<span data-ttu-id="9096e-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9096e-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="9096e-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9096e-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="9096e-154">Satz-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9096e-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


