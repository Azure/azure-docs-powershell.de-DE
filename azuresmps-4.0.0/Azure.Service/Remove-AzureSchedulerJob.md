---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006335"
---
# <span data-ttu-id="899f4-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="899f4-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="899f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="899f4-102">SYNOPSIS</span></span>
<span data-ttu-id="899f4-103">Löscht einen Scheduler-Job.</span><span class="sxs-lookup"><span data-stu-id="899f4-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="899f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="899f4-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="899f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="899f4-105">DESCRIPTION</span></span>
<span data-ttu-id="899f4-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="899f4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="899f4-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="899f4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="899f4-108">Das Cmdlet **Remove-AzureSchedulerJob** löscht einen Scheduler-Job.</span><span class="sxs-lookup"><span data-stu-id="899f4-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="899f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="899f4-109">EXAMPLES</span></span>

### <span data-ttu-id="899f4-110">Beispiel 1: Löschen eines Scheduler-Auftrags</span><span class="sxs-lookup"><span data-stu-id="899f4-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="899f4-111">Mit diesem Befehl wird der Auftrag mit dem Namen Job17 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="899f4-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="899f4-112">Dieser Auftrag ist Teil der Auftrags Sammlung mit dem Namen JobCollection01 und befindet sich am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="899f4-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="899f4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="899f4-113">PARAMETERS</span></span>

### <span data-ttu-id="899f4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="899f4-114">-Force</span></span>
<span data-ttu-id="899f4-115">Gibt an, dass das Cmdlet den Scheduler-Auftrag entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="899f4-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="899f4-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="899f4-116">-JobCollectionName</span></span>
<span data-ttu-id="899f4-117">Gibt den Namen der Sammlung an, die den zu löschenden Scheduler-Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="899f4-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="899f4-118">-Jobname</span><span class="sxs-lookup"><span data-stu-id="899f4-118">-JobName</span></span>
<span data-ttu-id="899f4-119">Gibt den Namen eines Scheduler-Auftrags an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="899f4-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="899f4-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="899f4-120">-Location</span></span>
<span data-ttu-id="899f4-121">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="899f4-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="899f4-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="899f4-122">Valid values are:</span></span> 

- <span data-ttu-id="899f4-123">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="899f4-123">Anywhere Asia</span></span>
- <span data-ttu-id="899f4-124">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="899f4-124">Anywhere Europe</span></span>
- <span data-ttu-id="899f4-125">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="899f4-125">Anywhere US</span></span>
- <span data-ttu-id="899f4-126">Ostasien</span><span class="sxs-lookup"><span data-stu-id="899f4-126">East Asia</span></span>
- <span data-ttu-id="899f4-127">East US</span><span class="sxs-lookup"><span data-stu-id="899f4-127">East US</span></span>
- <span data-ttu-id="899f4-128">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="899f4-128">North Central US</span></span>
- <span data-ttu-id="899f4-129">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="899f4-129">North Europe</span></span>
- <span data-ttu-id="899f4-130">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="899f4-130">South Central US</span></span>
- <span data-ttu-id="899f4-131">Südostasien</span><span class="sxs-lookup"><span data-stu-id="899f4-131">Southeast Asia</span></span>
- <span data-ttu-id="899f4-132">West Europa</span><span class="sxs-lookup"><span data-stu-id="899f4-132">West Europe</span></span>
- <span data-ttu-id="899f4-133">West-US</span><span class="sxs-lookup"><span data-stu-id="899f4-133">West US</span></span>

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

### <span data-ttu-id="899f4-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="899f4-134">-Profile</span></span>
<span data-ttu-id="899f4-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="899f4-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="899f4-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="899f4-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="899f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899f4-137">CommonParameters</span></span>
<span data-ttu-id="899f4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899f4-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899f4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899f4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="899f4-140">INPUTS</span></span>

## <span data-ttu-id="899f4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="899f4-141">OUTPUTS</span></span>

## <span data-ttu-id="899f4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="899f4-142">NOTES</span></span>

## <span data-ttu-id="899f4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="899f4-143">RELATED LINKS</span></span>

[<span data-ttu-id="899f4-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="899f4-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


