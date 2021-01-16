---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301048"
---
# <span data-ttu-id="028c6-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="028c6-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="028c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="028c6-102">SYNOPSIS</span></span>
<span data-ttu-id="028c6-103">Überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="028c6-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="028c6-104">Namen von Mediendiensten sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="028c6-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="028c6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="028c6-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="028c6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="028c6-106">DESCRIPTION</span></span>
<span data-ttu-id="028c6-107">Das **Cmdlet "Get-AzMediaServiceNameAvailability"** überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="028c6-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="028c6-108">Namen von Mediendiensten sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="028c6-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="028c6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="028c6-109">EXAMPLES</span></span>

### <span data-ttu-id="028c6-110">Beispiel 1: Überprüfen, ob ein Mediendienstname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="028c6-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="028c6-111">Mit diesem Befehl wird überprüft, ob der Name "MediaService1" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="028c6-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="028c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="028c6-112">PARAMETERS</span></span>

### <span data-ttu-id="028c6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="028c6-113">-AccountName</span></span>
<span data-ttu-id="028c6-114">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="028c6-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="028c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028c6-115">-DefaultProfile</span></span>
<span data-ttu-id="028c6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="028c6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="028c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028c6-117">CommonParameters</span></span>
<span data-ttu-id="028c6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028c6-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028c6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="028c6-120">INPUTS</span></span>

### <span data-ttu-id="028c6-121">Keine</span><span class="sxs-lookup"><span data-stu-id="028c6-121">None</span></span>

## <span data-ttu-id="028c6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="028c6-122">OUTPUTS</span></span>

### <span data-ttu-id="028c6-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="028c6-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="028c6-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="028c6-124">NOTES</span></span>

## <span data-ttu-id="028c6-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="028c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="028c6-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="028c6-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="028c6-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="028c6-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="028c6-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="028c6-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="028c6-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="028c6-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


