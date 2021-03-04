---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d8928aea539910751c61ad03f5e5a4d67188e371
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922848"
---
# <span data-ttu-id="1bebc-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1bebc-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="1bebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bebc-102">SYNOPSIS</span></span>
<span data-ttu-id="1bebc-103">Überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1bebc-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="1bebc-104">Mediendienstnamen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1bebc-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="1bebc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bebc-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="1bebc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bebc-106">DESCRIPTION</span></span>
<span data-ttu-id="1bebc-107">Das **Cmdlet Get-AzMediaServiceNameAvailability** überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1bebc-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="1bebc-108">Mediendienstnamen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1bebc-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="1bebc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1bebc-109">EXAMPLES</span></span>

### <span data-ttu-id="1bebc-110">Beispiel 1: Überprüfen, ob ein Mediendienstname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="1bebc-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="1bebc-111">Mit diesem Befehl wird überprüft, ob der Name MediaService1 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1bebc-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="1bebc-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1bebc-112">PARAMETERS</span></span>

### <span data-ttu-id="1bebc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1bebc-113">-AccountName</span></span>
<span data-ttu-id="1bebc-114">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1bebc-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bebc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bebc-115">-DefaultProfile</span></span>
<span data-ttu-id="1bebc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1bebc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bebc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bebc-117">CommonParameters</span></span>
<span data-ttu-id="1bebc-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bebc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bebc-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bebc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bebc-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1bebc-120">INPUTS</span></span>

### <span data-ttu-id="1bebc-121">Keine</span><span class="sxs-lookup"><span data-stu-id="1bebc-121">None</span></span>

## <span data-ttu-id="1bebc-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1bebc-122">OUTPUTS</span></span>

### <span data-ttu-id="1bebc-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="1bebc-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="1bebc-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1bebc-124">NOTES</span></span>

## <span data-ttu-id="1bebc-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1bebc-125">RELATED LINKS</span></span>

[<span data-ttu-id="1bebc-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1bebc-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="1bebc-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1bebc-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="1bebc-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1bebc-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="1bebc-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1bebc-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


