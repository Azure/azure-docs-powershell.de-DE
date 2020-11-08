---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004743"
---
# <span data-ttu-id="05d21-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="05d21-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="05d21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05d21-102">SYNOPSIS</span></span>
<span data-ttu-id="05d21-103">Überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="05d21-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="05d21-104">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="05d21-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="05d21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d21-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="05d21-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05d21-106">DESCRIPTION</span></span>
<span data-ttu-id="05d21-107">Das Cmdlet " **Get-AzMediaServiceNameAvailability** " überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="05d21-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="05d21-108">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="05d21-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="05d21-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05d21-109">EXAMPLES</span></span>

### <span data-ttu-id="05d21-110">Beispiel 1: überprüfen, ob ein Mediendienst Name verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="05d21-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="05d21-111">Dieser Befehl überprüft, ob der Name MediaService1 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="05d21-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="05d21-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d21-112">PARAMETERS</span></span>

### <span data-ttu-id="05d21-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="05d21-113">-AccountName</span></span>
<span data-ttu-id="05d21-114">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="05d21-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="05d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d21-115">-DefaultProfile</span></span>
<span data-ttu-id="05d21-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="05d21-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05d21-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d21-117">CommonParameters</span></span>
<span data-ttu-id="05d21-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d21-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d21-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d21-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d21-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05d21-120">INPUTS</span></span>

### <span data-ttu-id="05d21-121">Keine</span><span class="sxs-lookup"><span data-stu-id="05d21-121">None</span></span>

## <span data-ttu-id="05d21-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05d21-122">OUTPUTS</span></span>

### <span data-ttu-id="05d21-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="05d21-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="05d21-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="05d21-124">NOTES</span></span>

## <span data-ttu-id="05d21-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05d21-125">RELATED LINKS</span></span>

[<span data-ttu-id="05d21-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="05d21-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="05d21-127">Neu – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="05d21-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="05d21-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="05d21-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="05d21-129">Satz-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="05d21-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


