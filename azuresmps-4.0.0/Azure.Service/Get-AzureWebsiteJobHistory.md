---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006713"
---
# <span data-ttu-id="849e6-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="849e6-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="849e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="849e6-102">SYNOPSIS</span></span>
<span data-ttu-id="849e6-103">Ruft einen Web-Auftragsverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="849e6-103">Gets a web job history.</span></span>

## <span data-ttu-id="849e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="849e6-104">SYNTAX</span></span>

### <span data-ttu-id="849e6-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="849e6-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="849e6-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="849e6-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="849e6-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="849e6-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="849e6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="849e6-108">DESCRIPTION</span></span>
<span data-ttu-id="849e6-109">Ruft einen Web-Auftragsverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="849e6-109">Gets a web job history.</span></span>

## <span data-ttu-id="849e6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="849e6-110">EXAMPLES</span></span>

### <span data-ttu-id="849e6-111">Beispiel 1: Abrufen des vollständigen Verlaufs für einen Web-Job</span><span class="sxs-lookup"><span data-stu-id="849e6-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="849e6-112">Ruft den vollständigen Verlauf für MyWebJob ab.</span><span class="sxs-lookup"><span data-stu-id="849e6-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="849e6-113">Beispiel 2: Abrufen der letzten Ausführung für einen Web-Job</span><span class="sxs-lookup"><span data-stu-id="849e6-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="849e6-114">Ruft die neuesten Ausführungsinformationen für MyWebJob ab.</span><span class="sxs-lookup"><span data-stu-id="849e6-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="849e6-115">Beispiel 3: Abrufen einer bestimmten Ausführung für einen Web-Job</span><span class="sxs-lookup"><span data-stu-id="849e6-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="849e6-116">Ruft alle Informationen zum Ausführen mit ID 10 für MyWebJob ab.</span><span class="sxs-lookup"><span data-stu-id="849e6-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="849e6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="849e6-117">PARAMETERS</span></span>

### <span data-ttu-id="849e6-118">-Jobname</span><span class="sxs-lookup"><span data-stu-id="849e6-118">-JobName</span></span>
<span data-ttu-id="849e6-119">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="849e6-119">The web job name.</span></span>

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

### <span data-ttu-id="849e6-120">-Neueste</span><span class="sxs-lookup"><span data-stu-id="849e6-120">-Latest</span></span>
<span data-ttu-id="849e6-121">Wenn angegeben, geben Sie den neuesten Ausführungsverlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="849e6-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="849e6-122">-Name</span></span>
<span data-ttu-id="849e6-123">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="849e6-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="849e6-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="849e6-124">-Profile</span></span>
<span data-ttu-id="849e6-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="849e6-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="849e6-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="849e6-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="849e6-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="849e6-127">-RunId</span></span>
<span data-ttu-id="849e6-128">Gibt die ID des Ausführungsverlaufs an, den Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="849e6-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="849e6-129">-Slot</span></span>
<span data-ttu-id="849e6-130">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="849e6-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="849e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849e6-131">CommonParameters</span></span>
<span data-ttu-id="849e6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849e6-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849e6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="849e6-134">INPUTS</span></span>

## <span data-ttu-id="849e6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="849e6-135">OUTPUTS</span></span>

## <span data-ttu-id="849e6-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="849e6-136">NOTES</span></span>

## <span data-ttu-id="849e6-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="849e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="849e6-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="849e6-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="849e6-139">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="849e6-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="849e6-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="849e6-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="849e6-141">Neu – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="849e6-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="849e6-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="849e6-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


