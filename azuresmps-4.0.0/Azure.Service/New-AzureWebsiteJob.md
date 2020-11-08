---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006389"
---
# <span data-ttu-id="66aaa-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="66aaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="66aaa-103">Erstellt einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="66aaa-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="66aaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66aaa-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66aaa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="66aaa-106">Das Cmdlet **New-AzureWebsiteJob** erstellt einen Web-Job für eine Website.</span><span class="sxs-lookup"><span data-stu-id="66aaa-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="66aaa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66aaa-107">EXAMPLES</span></span>

### <span data-ttu-id="66aaa-108">Beispiel 1: Erstellen eines neuen Webauftrags für eine Website</span><span class="sxs-lookup"><span data-stu-id="66aaa-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="66aaa-109">Erstellt einen fortlaufenden Job, um job.bat auf der Website mywebsite anzurufen.</span><span class="sxs-lookup"><span data-stu-id="66aaa-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="66aaa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66aaa-110">PARAMETERS</span></span>

### <span data-ttu-id="66aaa-111">-Jobfile</span><span class="sxs-lookup"><span data-stu-id="66aaa-111">-JobFile</span></span>
<span data-ttu-id="66aaa-112">Die Web-Job-Datei.</span><span class="sxs-lookup"><span data-stu-id="66aaa-112">The web job file.</span></span>

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

### <span data-ttu-id="66aaa-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="66aaa-113">-JobName</span></span>
<span data-ttu-id="66aaa-114">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="66aaa-114">The web job name.</span></span>

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

### <span data-ttu-id="66aaa-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="66aaa-115">-JobType</span></span>
<span data-ttu-id="66aaa-116">Der Web-Auftragstyp.</span><span class="sxs-lookup"><span data-stu-id="66aaa-116">The web job type.</span></span>
<span data-ttu-id="66aaa-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="66aaa-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66aaa-118">Ausgelöst</span><span class="sxs-lookup"><span data-stu-id="66aaa-118">Triggered</span></span> 
- <span data-ttu-id="66aaa-119">Fortlaufender</span><span class="sxs-lookup"><span data-stu-id="66aaa-119">Continuous</span></span>

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

### <span data-ttu-id="66aaa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66aaa-120">-Name</span></span>
<span data-ttu-id="66aaa-121">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="66aaa-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="66aaa-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="66aaa-122">-Profile</span></span>
<span data-ttu-id="66aaa-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="66aaa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66aaa-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="66aaa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66aaa-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="66aaa-125">-Slot</span></span>
<span data-ttu-id="66aaa-126">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="66aaa-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="66aaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66aaa-127">CommonParameters</span></span>
<span data-ttu-id="66aaa-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66aaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66aaa-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66aaa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66aaa-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66aaa-130">INPUTS</span></span>

## <span data-ttu-id="66aaa-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66aaa-131">OUTPUTS</span></span>

## <span data-ttu-id="66aaa-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="66aaa-132">NOTES</span></span>

## <span data-ttu-id="66aaa-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66aaa-133">RELATED LINKS</span></span>

[<span data-ttu-id="66aaa-134">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="66aaa-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="66aaa-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="66aaa-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="66aaa-137">Anfang-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="66aaa-138">Stopp-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


