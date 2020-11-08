---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005688"
---
# <span data-ttu-id="05c77-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="05c77-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="05c77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05c77-102">SYNOPSIS</span></span>
<span data-ttu-id="05c77-103">Entfernt einen vorhandenen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="05c77-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="05c77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c77-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05c77-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05c77-105">DESCRIPTION</span></span>
<span data-ttu-id="05c77-106">Entfernt einen vorhandenen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="05c77-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="05c77-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05c77-107">EXAMPLES</span></span>

### <span data-ttu-id="05c77-108">Beispiel 1: Entfernen eines vorhandenen Web-Auftrags für eine Website</span><span class="sxs-lookup"><span data-stu-id="05c77-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="05c77-109">Entfernt einen Web-Job namens "MyWebJob" für "Meine Website".</span><span class="sxs-lookup"><span data-stu-id="05c77-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="05c77-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05c77-110">PARAMETERS</span></span>

### <span data-ttu-id="05c77-111">-Force</span><span class="sxs-lookup"><span data-stu-id="05c77-111">-Force</span></span>
<span data-ttu-id="05c77-112">Gibt an, dass das Cmdlet den Web-Job entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="05c77-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="05c77-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="05c77-113">-JobName</span></span>
<span data-ttu-id="05c77-114">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="05c77-114">The web job name.</span></span>

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

### <span data-ttu-id="05c77-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="05c77-115">-JobType</span></span>
<span data-ttu-id="05c77-116">Der Web-Auftragstyp.</span><span class="sxs-lookup"><span data-stu-id="05c77-116">The web job type.</span></span>
<span data-ttu-id="05c77-117">Kann ausgelöst oder kontinuierlich sein.</span><span class="sxs-lookup"><span data-stu-id="05c77-117">Can be triggered or continuous.</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c77-118">-Name</span><span class="sxs-lookup"><span data-stu-id="05c77-118">-Name</span></span>
<span data-ttu-id="05c77-119">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="05c77-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="05c77-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="05c77-120">-Profile</span></span>
<span data-ttu-id="05c77-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="05c77-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05c77-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="05c77-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05c77-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="05c77-123">-Slot</span></span>
<span data-ttu-id="05c77-124">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="05c77-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="05c77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c77-125">CommonParameters</span></span>
<span data-ttu-id="05c77-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c77-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c77-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c77-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05c77-128">INPUTS</span></span>

## <span data-ttu-id="05c77-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05c77-129">OUTPUTS</span></span>

## <span data-ttu-id="05c77-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="05c77-130">NOTES</span></span>

## <span data-ttu-id="05c77-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05c77-131">RELATED LINKS</span></span>

[<span data-ttu-id="05c77-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="05c77-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="05c77-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="05c77-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="05c77-134">Neu – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="05c77-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="05c77-135">Anfang-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="05c77-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="05c77-136">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="05c77-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


