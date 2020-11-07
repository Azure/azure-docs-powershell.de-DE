---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663907"
---
# <span data-ttu-id="6faf9-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6faf9-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="6faf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6faf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6faf9-103">Überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6faf9-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="6faf9-104">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6faf9-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6faf9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6faf9-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="6faf9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6faf9-106">DESCRIPTION</span></span>
<span data-ttu-id="6faf9-107">Das Cmdlet " **Get-AzureRmMediaServiceNameAvailability** " überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6faf9-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="6faf9-108">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6faf9-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="6faf9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6faf9-109">EXAMPLES</span></span>

### <span data-ttu-id="6faf9-110">Beispiel 1: überprüfen, ob ein Mediendienst Name verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="6faf9-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="6faf9-111">Dieser Befehl überprüft, ob der Name MediaService1 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6faf9-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="6faf9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6faf9-112">PARAMETERS</span></span>

### <span data-ttu-id="6faf9-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6faf9-113">-AccountName</span></span>
<span data-ttu-id="6faf9-114">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6faf9-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6faf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6faf9-115">-DefaultProfile</span></span>
<span data-ttu-id="6faf9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6faf9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6faf9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6faf9-117">CommonParameters</span></span>
<span data-ttu-id="6faf9-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6faf9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6faf9-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6faf9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6faf9-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6faf9-120">INPUTS</span></span>

## <span data-ttu-id="6faf9-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6faf9-121">OUTPUTS</span></span>

### <span data-ttu-id="6faf9-122">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="6faf9-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="6faf9-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6faf9-123">NOTES</span></span>

## <span data-ttu-id="6faf9-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6faf9-124">RELATED LINKS</span></span>

[<span data-ttu-id="6faf9-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="6faf9-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="6faf9-126">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="6faf9-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="6faf9-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="6faf9-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="6faf9-128">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="6faf9-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


