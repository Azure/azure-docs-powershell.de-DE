---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173708"
---
# <span data-ttu-id="b26e8-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b26e8-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="b26e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b26e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b26e8-103">Überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b26e8-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="b26e8-104">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b26e8-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="b26e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b26e8-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="b26e8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b26e8-106">DESCRIPTION</span></span>
<span data-ttu-id="b26e8-107">Das Cmdlet " **Get-AzMediaServiceNameAvailability** " überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b26e8-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="b26e8-108">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b26e8-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="b26e8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b26e8-109">EXAMPLES</span></span>

### <span data-ttu-id="b26e8-110">Beispiel 1: überprüfen, ob ein Mediendienst Name verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="b26e8-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="b26e8-111">Dieser Befehl überprüft, ob der Name MediaService1 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b26e8-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="b26e8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b26e8-112">PARAMETERS</span></span>

### <span data-ttu-id="b26e8-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b26e8-113">-AccountName</span></span>
<span data-ttu-id="b26e8-114">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b26e8-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b26e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26e8-115">-DefaultProfile</span></span>
<span data-ttu-id="b26e8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b26e8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b26e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26e8-117">CommonParameters</span></span>
<span data-ttu-id="b26e8-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26e8-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b26e8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26e8-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b26e8-120">INPUTS</span></span>

### <span data-ttu-id="b26e8-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b26e8-121">None</span></span>

## <span data-ttu-id="b26e8-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b26e8-122">OUTPUTS</span></span>

### <span data-ttu-id="b26e8-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="b26e8-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="b26e8-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="b26e8-124">NOTES</span></span>

## <span data-ttu-id="b26e8-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b26e8-125">RELATED LINKS</span></span>

[<span data-ttu-id="b26e8-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b26e8-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b26e8-127">Neu – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b26e8-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="b26e8-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b26e8-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="b26e8-129">Satz-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b26e8-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


