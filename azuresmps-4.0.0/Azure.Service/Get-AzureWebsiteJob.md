---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006479"
---
# <span data-ttu-id="ba5bd-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ba5bd-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="ba5bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5bd-103">Ruft die Web-Aufträge ab, die einer Website zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="ba5bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba5bd-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba5bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba5bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5bd-106">Ruft die Web-Aufträge ab, die einer Website zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="ba5bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba5bd-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5bd-108">Beispiel 1: Abrufen bestimmter Informationen zum Web-Job</span><span class="sxs-lookup"><span data-stu-id="ba5bd-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="ba5bd-109">Ruft einen Webauftrag mit dem Namen "MyWebJob" aus dem Produktions Steckplatz der Website ab.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="ba5bd-110">Beispiel 2: Abrufen aller Web-Aufträge für eine Website</span><span class="sxs-lookup"><span data-stu-id="ba5bd-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="ba5bd-111">Ruft alle Web-Jobs ab, die dem Produktions Steckplatz von mywebsite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="ba5bd-112">Beispiel 3: Abrufen aller ausgelösten Web-Aufträge</span><span class="sxs-lookup"><span data-stu-id="ba5bd-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="ba5bd-113">Ruft alle ausgelösten Webaufträge aus dem Staging-Slot der mywebsite ab.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="ba5bd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba5bd-114">PARAMETERS</span></span>

### <span data-ttu-id="ba5bd-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="ba5bd-115">-JobName</span></span>
<span data-ttu-id="ba5bd-116">Der Name des Webdiensts</span><span class="sxs-lookup"><span data-stu-id="ba5bd-116">The web job name</span></span>

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

### <span data-ttu-id="ba5bd-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="ba5bd-117">-JobType</span></span>
<span data-ttu-id="ba5bd-118">Der Web-Auftragstyp.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-118">The web job type.</span></span>
<span data-ttu-id="ba5bd-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba5bd-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba5bd-120">Ausgelöst</span><span class="sxs-lookup"><span data-stu-id="ba5bd-120">Triggered</span></span>
- <span data-ttu-id="ba5bd-121">Fortlaufender</span><span class="sxs-lookup"><span data-stu-id="ba5bd-121">Continuous</span></span>

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

### <span data-ttu-id="ba5bd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ba5bd-122">-Name</span></span>
<span data-ttu-id="ba5bd-123">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="ba5bd-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba5bd-124">-Profile</span></span>
<span data-ttu-id="ba5bd-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba5bd-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba5bd-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="ba5bd-127">-Slot</span></span>
<span data-ttu-id="ba5bd-128">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="ba5bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5bd-129">CommonParameters</span></span>
<span data-ttu-id="ba5bd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5bd-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5bd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5bd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba5bd-132">INPUTS</span></span>

## <span data-ttu-id="ba5bd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba5bd-133">OUTPUTS</span></span>

## <span data-ttu-id="ba5bd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba5bd-134">NOTES</span></span>

## <span data-ttu-id="ba5bd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba5bd-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba5bd-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba5bd-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ba5bd-137">Neu – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ba5bd-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="ba5bd-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ba5bd-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="ba5bd-139">Anfang-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ba5bd-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="ba5bd-140">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ba5bd-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


