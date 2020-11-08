---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005818"
---
# <span data-ttu-id="444db-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="444db-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="444db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="444db-102">SYNOPSIS</span></span>
<span data-ttu-id="444db-103">Ruft Scheduler-Auftrags Auflistungen ab.</span><span class="sxs-lookup"><span data-stu-id="444db-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="444db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="444db-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="444db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="444db-105">DESCRIPTION</span></span>
<span data-ttu-id="444db-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="444db-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="444db-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="444db-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="444db-108">Das Cmdlet " **Get-AzureSchedulerJobCollection** " Ruft eine oder mehrere Scheduler-Auftrags Auflistungen ab.</span><span class="sxs-lookup"><span data-stu-id="444db-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="444db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="444db-109">EXAMPLES</span></span>

### <span data-ttu-id="444db-110">Beispiel 1: Abrufen aller Auflistungen</span><span class="sxs-lookup"><span data-stu-id="444db-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="444db-111">Dieser Befehl ruft alle Scheduler-Auftrags Auflistungen über alle Speicherorte des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="444db-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="444db-112">Beispiel 2: Abrufen aller Auflistungen für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="444db-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="444db-113">Dieser Befehl ruft alle Scheduler-Auftrags Auflistungen an dem Speicherort mit dem Namen North Central US ab.</span><span class="sxs-lookup"><span data-stu-id="444db-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="444db-114">Beispiel 3: Abrufen einer Sammlung mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="444db-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="444db-115">Dieser Befehl ruft die Scheduler-Auftrags Sammlung mit dem Namen JobCollection01 ab.</span><span class="sxs-lookup"><span data-stu-id="444db-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="444db-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="444db-116">PARAMETERS</span></span>

### <span data-ttu-id="444db-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="444db-117">-JobCollectionName</span></span>
<span data-ttu-id="444db-118">Gibt den Namen der abzurufenden Scheduler-Auftrags Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="444db-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="444db-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="444db-119">-Location</span></span>
<span data-ttu-id="444db-120">Gibt den Namen des Speicherorts an, der den clouddienst hostet.</span><span class="sxs-lookup"><span data-stu-id="444db-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="444db-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="444db-121">Valid values are:</span></span> 

- <span data-ttu-id="444db-122">Überall in Asien</span><span class="sxs-lookup"><span data-stu-id="444db-122">Anywhere Asia</span></span>
- <span data-ttu-id="444db-123">Überall in Europa</span><span class="sxs-lookup"><span data-stu-id="444db-123">Anywhere Europe</span></span>
- <span data-ttu-id="444db-124">Überall in den USA</span><span class="sxs-lookup"><span data-stu-id="444db-124">Anywhere US</span></span>
- <span data-ttu-id="444db-125">Ostasien</span><span class="sxs-lookup"><span data-stu-id="444db-125">East Asia</span></span>
- <span data-ttu-id="444db-126">East US</span><span class="sxs-lookup"><span data-stu-id="444db-126">East US</span></span>
- <span data-ttu-id="444db-127">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="444db-127">North Central US</span></span>
- <span data-ttu-id="444db-128">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="444db-128">North Europe</span></span>
- <span data-ttu-id="444db-129">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="444db-129">South Central US</span></span>
- <span data-ttu-id="444db-130">Südostasien</span><span class="sxs-lookup"><span data-stu-id="444db-130">Southeast Asia</span></span>
- <span data-ttu-id="444db-131">West Europa</span><span class="sxs-lookup"><span data-stu-id="444db-131">West Europe</span></span>
- <span data-ttu-id="444db-132">West-US</span><span class="sxs-lookup"><span data-stu-id="444db-132">West US</span></span>

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

### <span data-ttu-id="444db-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="444db-133">-Profile</span></span>
<span data-ttu-id="444db-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="444db-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="444db-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="444db-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="444db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444db-136">CommonParameters</span></span>
<span data-ttu-id="444db-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444db-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="444db-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444db-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="444db-139">INPUTS</span></span>

## <span data-ttu-id="444db-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="444db-140">OUTPUTS</span></span>

## <span data-ttu-id="444db-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="444db-141">NOTES</span></span>

## <span data-ttu-id="444db-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="444db-142">RELATED LINKS</span></span>

[<span data-ttu-id="444db-143">Neu – AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="444db-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="444db-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="444db-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="444db-145">Satz-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="444db-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


