---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005991"
---
# <span data-ttu-id="bd05f-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="bd05f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd05f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd05f-103">Öffnet einen Browser auf einer bestimmten Website.</span><span class="sxs-lookup"><span data-stu-id="bd05f-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="bd05f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd05f-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bd05f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd05f-105">DESCRIPTION</span></span>
<span data-ttu-id="bd05f-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd05f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bd05f-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bd05f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bd05f-108">Mit dem Cmdlet " **anzeigen-AzureWebsite** " wird ein Browser auf einer bestimmten Website geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bd05f-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="bd05f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd05f-109">EXAMPLES</span></span>

## <span data-ttu-id="bd05f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd05f-110">PARAMETERS</span></span>

### <span data-ttu-id="bd05f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="bd05f-111">-Name</span></span>
<span data-ttu-id="bd05f-112">Gibt den Namen der Website an, die im Browser geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd05f-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="bd05f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="bd05f-113">-Profile</span></span>
<span data-ttu-id="bd05f-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bd05f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bd05f-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bd05f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd05f-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="bd05f-116">-Slot</span></span>
<span data-ttu-id="bd05f-117">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="bd05f-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="bd05f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd05f-118">CommonParameters</span></span>
<span data-ttu-id="bd05f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd05f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd05f-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd05f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd05f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd05f-121">INPUTS</span></span>

## <span data-ttu-id="bd05f-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd05f-122">OUTPUTS</span></span>

## <span data-ttu-id="bd05f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd05f-123">NOTES</span></span>

## <span data-ttu-id="bd05f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd05f-124">RELATED LINKS</span></span>

[<span data-ttu-id="bd05f-125">Anzeigen-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="bd05f-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="bd05f-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="bd05f-127">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="bd05f-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="bd05f-129">Neustart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="bd05f-130">Satz-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bd05f-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


