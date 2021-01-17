---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380748"
---
# <span data-ttu-id="22be5-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="22be5-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="22be5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22be5-102">SYNOPSIS</span></span>
<span data-ttu-id="22be5-103">Überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="22be5-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="22be5-104">Namen von Mediendiensten sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="22be5-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="22be5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22be5-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="22be5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22be5-106">DESCRIPTION</span></span>
<span data-ttu-id="22be5-107">Das **Cmdlet "Get-AzMediaServiceNameAvailability"** überprüft, ob ein Mediendienstname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="22be5-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="22be5-108">Namen von Mediendiensten sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="22be5-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="22be5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22be5-109">EXAMPLES</span></span>

### <span data-ttu-id="22be5-110">Beispiel 1: Überprüfen, ob ein Mediendienstname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="22be5-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="22be5-111">Mit diesem Befehl wird überprüft, ob der Name "MediaService1" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="22be5-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="22be5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22be5-112">PARAMETERS</span></span>

### <span data-ttu-id="22be5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22be5-113">-AccountName</span></span>
<span data-ttu-id="22be5-114">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="22be5-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="22be5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22be5-115">-DefaultProfile</span></span>
<span data-ttu-id="22be5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="22be5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22be5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22be5-117">CommonParameters</span></span>
<span data-ttu-id="22be5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22be5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22be5-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22be5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22be5-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22be5-120">INPUTS</span></span>

### <span data-ttu-id="22be5-121">Keine</span><span class="sxs-lookup"><span data-stu-id="22be5-121">None</span></span>

## <span data-ttu-id="22be5-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22be5-122">OUTPUTS</span></span>

### <span data-ttu-id="22be5-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="22be5-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="22be5-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22be5-124">NOTES</span></span>

## <span data-ttu-id="22be5-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22be5-125">RELATED LINKS</span></span>

[<span data-ttu-id="22be5-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="22be5-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="22be5-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="22be5-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="22be5-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="22be5-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="22be5-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="22be5-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


