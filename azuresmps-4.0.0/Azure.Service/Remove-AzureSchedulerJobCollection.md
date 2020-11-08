---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006334"
---
# <span data-ttu-id="31a9e-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31a9e-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="31a9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="31a9e-103">Löscht eine Scheduler-Auftrags Sammlung.</span><span class="sxs-lookup"><span data-stu-id="31a9e-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="31a9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a9e-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31a9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="31a9e-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="31a9e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="31a9e-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="31a9e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="31a9e-108">Das Cmdlet **Remove-AzureSchedulerJobCollection** löscht eine Scheduler-Auftrags Sammlung und alle Aufträge unter dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="31a9e-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="31a9e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31a9e-109">EXAMPLES</span></span>

### <span data-ttu-id="31a9e-110">Beispiel 1: Löschen einer Auftrags Sammlung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="31a9e-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="31a9e-111">Dieser Befehl löscht die Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 im Nord zentralen US-Standort.</span><span class="sxs-lookup"><span data-stu-id="31a9e-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="31a9e-112">Der Befehl löscht auch die Aufträge unter JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="31a9e-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="31a9e-113">Beispiel 2: Löschen eines Auftragsspeicher Orts</span><span class="sxs-lookup"><span data-stu-id="31a9e-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="31a9e-114">Dieser Befehl löscht die Scheduler-Auftrags Sammlung mit dem Namen JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="31a9e-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="31a9e-115">Der Befehl löscht auch die Aufträge unter JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="31a9e-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="31a9e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="31a9e-116">PARAMETERS</span></span>

### <span data-ttu-id="31a9e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31a9e-117">-Force</span></span>
<span data-ttu-id="31a9e-118">Gibt an, dass dieses Cmdlet die Scheduler-Auftrags Sammlung entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="31a9e-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="31a9e-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="31a9e-119">-JobCollectionName</span></span>
<span data-ttu-id="31a9e-120">Gibt den Namen der zu löschenden Scheduler-Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="31a9e-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="31a9e-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="31a9e-121">-Location</span></span>
<span data-ttu-id="31a9e-122">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="31a9e-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="31a9e-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="31a9e-123">Valid values are:</span></span> 

- <span data-ttu-id="31a9e-124">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="31a9e-124">Anywhere Asia</span></span>
- <span data-ttu-id="31a9e-125">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="31a9e-125">Anywhere Europe</span></span>
- <span data-ttu-id="31a9e-126">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="31a9e-126">Anywhere US</span></span>
- <span data-ttu-id="31a9e-127">Ostasien</span><span class="sxs-lookup"><span data-stu-id="31a9e-127">East Asia</span></span>
- <span data-ttu-id="31a9e-128">East US</span><span class="sxs-lookup"><span data-stu-id="31a9e-128">East US</span></span>
- <span data-ttu-id="31a9e-129">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="31a9e-129">North Central US</span></span>
- <span data-ttu-id="31a9e-130">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="31a9e-130">North Europe</span></span>
- <span data-ttu-id="31a9e-131">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="31a9e-131">South Central US</span></span>
- <span data-ttu-id="31a9e-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="31a9e-132">Southeast Asia</span></span>
- <span data-ttu-id="31a9e-133">West Europa</span><span class="sxs-lookup"><span data-stu-id="31a9e-133">West Europe</span></span>
- <span data-ttu-id="31a9e-134">West-US</span><span class="sxs-lookup"><span data-stu-id="31a9e-134">West US</span></span>

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

### <span data-ttu-id="31a9e-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="31a9e-135">-Profile</span></span>
<span data-ttu-id="31a9e-136">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="31a9e-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31a9e-137">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="31a9e-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31a9e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a9e-138">CommonParameters</span></span>
<span data-ttu-id="31a9e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a9e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a9e-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a9e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a9e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31a9e-141">INPUTS</span></span>

## <span data-ttu-id="31a9e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31a9e-142">OUTPUTS</span></span>

## <span data-ttu-id="31a9e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="31a9e-143">NOTES</span></span>

## <span data-ttu-id="31a9e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31a9e-144">RELATED LINKS</span></span>

[<span data-ttu-id="31a9e-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31a9e-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="31a9e-146">Neu – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31a9e-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="31a9e-147">Satz-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31a9e-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


