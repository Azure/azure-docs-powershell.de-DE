---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005897"
---
# <span data-ttu-id="6cff5-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="6cff5-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="6cff5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cff5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cff5-103">Deaktiviert das Debuggen der Website.</span><span class="sxs-lookup"><span data-stu-id="6cff5-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="6cff5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cff5-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cff5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cff5-105">DESCRIPTION</span></span>
<span data-ttu-id="6cff5-106">Deaktiviert das Debuggen der Website in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6cff5-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="6cff5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cff5-107">EXAMPLES</span></span>

### <span data-ttu-id="6cff5-108">--------------Deaktivieren des Website Debuggens--------------</span><span class="sxs-lookup"><span data-stu-id="6cff5-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="6cff5-109">Deaktiviert das Debuggen von Websites auf der Website mywebsite</span><span class="sxs-lookup"><span data-stu-id="6cff5-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="6cff5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cff5-110">PARAMETERS</span></span>

### <span data-ttu-id="6cff5-111">-Name</span><span class="sxs-lookup"><span data-stu-id="6cff5-111">-Name</span></span>
<span data-ttu-id="6cff5-112">Der Name der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="6cff5-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="6cff5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cff5-113">-PassThru</span></span>
<span data-ttu-id="6cff5-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6cff5-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cff5-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6cff5-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6cff5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="6cff5-116">-Profile</span></span>
<span data-ttu-id="6cff5-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6cff5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6cff5-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6cff5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6cff5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6cff5-119">-Slot</span></span>
<span data-ttu-id="6cff5-120">Der Steckplatzname der Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="6cff5-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="6cff5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cff5-121">CommonParameters</span></span>
<span data-ttu-id="6cff5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cff5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cff5-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cff5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cff5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cff5-124">INPUTS</span></span>

## <span data-ttu-id="6cff5-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cff5-125">OUTPUTS</span></span>

## <span data-ttu-id="6cff5-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cff5-126">NOTES</span></span>

## <span data-ttu-id="6cff5-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cff5-127">RELATED LINKS</span></span>

[<span data-ttu-id="6cff5-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="6cff5-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="6cff5-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cff5-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6cff5-130">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cff5-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6cff5-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cff5-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6cff5-132">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6cff5-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


