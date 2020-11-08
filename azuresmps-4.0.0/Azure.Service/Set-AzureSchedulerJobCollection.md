---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005649"
---
# <span data-ttu-id="e3015-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e3015-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="e3015-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3015-102">SYNOPSIS</span></span>
<span data-ttu-id="e3015-103">Aktualisiert eine Scheduler-Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="e3015-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="e3015-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3015-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3015-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3015-105">DESCRIPTION</span></span>
<span data-ttu-id="e3015-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3015-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e3015-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e3015-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e3015-108">Das Cmdlet " **Satz-AzureSchedulerJobCollection** " aktualisiert eine Scheduler-Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="e3015-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="e3015-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3015-109">EXAMPLES</span></span>

### <span data-ttu-id="e3015-110">Beispiel 1: Ändern der maximalen Anzahl von Aufträgen für eine Sammlung</span><span class="sxs-lookup"><span data-stu-id="e3015-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="e3015-111">Mit diesem Befehl wird die maximale Anzahl von Aufträgen für die vorhandene Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 in 30 geändert.</span><span class="sxs-lookup"><span data-stu-id="e3015-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="e3015-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3015-112">PARAMETERS</span></span>

### <span data-ttu-id="e3015-113">-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="e3015-113">-Frequency</span></span>
<span data-ttu-id="e3015-114">Gibt die maximale Häufigkeit an, die für einen beliebigen Job in dieser Scheduler-Auftrags Sammlung angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3015-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="e3015-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3015-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3015-116">Minuten</span><span class="sxs-lookup"><span data-stu-id="e3015-116">Minute</span></span>
- <span data-ttu-id="e3015-117">Stunde</span><span class="sxs-lookup"><span data-stu-id="e3015-117">Hour</span></span>
- <span data-ttu-id="e3015-118">Tag</span><span class="sxs-lookup"><span data-stu-id="e3015-118">Day</span></span>
- <span data-ttu-id="e3015-119">Woche</span><span class="sxs-lookup"><span data-stu-id="e3015-119">Week</span></span>
- <span data-ttu-id="e3015-120">Monat</span><span class="sxs-lookup"><span data-stu-id="e3015-120">Month</span></span>
- <span data-ttu-id="e3015-121">Jahr</span><span class="sxs-lookup"><span data-stu-id="e3015-121">Year</span></span>

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

### <span data-ttu-id="e3015-122">-Intervall</span><span class="sxs-lookup"><span data-stu-id="e3015-122">-Interval</span></span>
<span data-ttu-id="e3015-123">Gibt das Intervall der Serie mit der Häufigkeit an, die mithilfe des *Frequency* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3015-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="e3015-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e3015-124">-JobCollectionName</span></span>
<span data-ttu-id="e3015-125">Gibt den Namen der Scheduler-Auftrags Sammlung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3015-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="e3015-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="e3015-126">-Location</span></span>
<span data-ttu-id="e3015-127">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="e3015-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="e3015-128">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e3015-128">Valid values are:</span></span> 

- <span data-ttu-id="e3015-129">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="e3015-129">Anywhere Asia</span></span>
- <span data-ttu-id="e3015-130">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="e3015-130">Anywhere Europe</span></span>
- <span data-ttu-id="e3015-131">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="e3015-131">Anywhere US</span></span>
- <span data-ttu-id="e3015-132">Ostasien</span><span class="sxs-lookup"><span data-stu-id="e3015-132">East Asia</span></span>
- <span data-ttu-id="e3015-133">East US</span><span class="sxs-lookup"><span data-stu-id="e3015-133">East US</span></span>
- <span data-ttu-id="e3015-134">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="e3015-134">North Central US</span></span>
- <span data-ttu-id="e3015-135">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="e3015-135">North Europe</span></span>
- <span data-ttu-id="e3015-136">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="e3015-136">South Central US</span></span>
- <span data-ttu-id="e3015-137">Südostasien</span><span class="sxs-lookup"><span data-stu-id="e3015-137">Southeast Asia</span></span>
- <span data-ttu-id="e3015-138">West Europa</span><span class="sxs-lookup"><span data-stu-id="e3015-138">West Europe</span></span>
- <span data-ttu-id="e3015-139">West-US</span><span class="sxs-lookup"><span data-stu-id="e3015-139">West US</span></span>

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

### <span data-ttu-id="e3015-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="e3015-140">-MaxJobCount</span></span>
<span data-ttu-id="e3015-141">Gibt die maximale Anzahl von Aufträgen an, die in der Scheduler-Auftrags Sammlung erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="e3015-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="e3015-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3015-142">-PassThru</span></span>
<span data-ttu-id="e3015-143">Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3015-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="e3015-144">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e3015-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3015-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="e3015-145">-Plan</span></span>
<span data-ttu-id="e3015-146">Gibt den Plan des Scheduler-Auftrags Sammlungs Plans an.</span><span class="sxs-lookup"><span data-stu-id="e3015-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="e3015-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3015-147">-Profile</span></span>
<span data-ttu-id="e3015-148">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e3015-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3015-149">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e3015-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3015-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3015-150">CommonParameters</span></span>
<span data-ttu-id="e3015-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3015-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3015-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3015-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3015-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3015-153">INPUTS</span></span>

## <span data-ttu-id="e3015-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3015-154">OUTPUTS</span></span>

## <span data-ttu-id="e3015-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3015-155">NOTES</span></span>

## <span data-ttu-id="e3015-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3015-156">RELATED LINKS</span></span>

[<span data-ttu-id="e3015-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e3015-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="e3015-158">Neu – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e3015-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="e3015-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e3015-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


