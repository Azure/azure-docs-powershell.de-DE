---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005973"
---
# <span data-ttu-id="46bc1-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="46bc1-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="46bc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="46bc1-103">Startet einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="46bc1-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="46bc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46bc1-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46bc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="46bc1-106">Das Cmdlet **Start-AzureWebsiteJob** startet einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="46bc1-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="46bc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46bc1-107">EXAMPLES</span></span>

### <span data-ttu-id="46bc1-108">Beispiel 1: Starten eines Web-Auftrags für eine Website</span><span class="sxs-lookup"><span data-stu-id="46bc1-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="46bc1-109">Startet einen Web-Job namens MyWebJob für mywebsite.</span><span class="sxs-lookup"><span data-stu-id="46bc1-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="46bc1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46bc1-110">PARAMETERS</span></span>

### <span data-ttu-id="46bc1-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="46bc1-111">-JobName</span></span>
<span data-ttu-id="46bc1-112">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="46bc1-112">The web job name.</span></span>

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

### <span data-ttu-id="46bc1-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="46bc1-113">-JobType</span></span>
<span data-ttu-id="46bc1-114">Der Web-Auftragstyp.</span><span class="sxs-lookup"><span data-stu-id="46bc1-114">The web job type.</span></span>
<span data-ttu-id="46bc1-115">Kann ausgelöst oder kontinuierlich sein.</span><span class="sxs-lookup"><span data-stu-id="46bc1-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="46bc1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="46bc1-116">-Name</span></span>
<span data-ttu-id="46bc1-117">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="46bc1-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="46bc1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46bc1-118">-PassThru</span></span>
<span data-ttu-id="46bc1-119">Gibt einen booleschen Wert zurück, der angibt, dass der Auftrag erfolgreich gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="46bc1-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="46bc1-120">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="46bc1-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="46bc1-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="46bc1-121">-Profile</span></span>
<span data-ttu-id="46bc1-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="46bc1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46bc1-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="46bc1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46bc1-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="46bc1-124">-Slot</span></span>
<span data-ttu-id="46bc1-125">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="46bc1-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="46bc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bc1-126">CommonParameters</span></span>
<span data-ttu-id="46bc1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bc1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46bc1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bc1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46bc1-129">INPUTS</span></span>

## <span data-ttu-id="46bc1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46bc1-130">OUTPUTS</span></span>

## <span data-ttu-id="46bc1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="46bc1-131">NOTES</span></span>

## <span data-ttu-id="46bc1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46bc1-132">RELATED LINKS</span></span>

[<span data-ttu-id="46bc1-133">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="46bc1-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="46bc1-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="46bc1-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="46bc1-135">Neu – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="46bc1-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="46bc1-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="46bc1-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="46bc1-137">Anfang-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="46bc1-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


