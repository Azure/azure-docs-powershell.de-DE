---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: ed91cc0c6558797ee1b46070978fe2a41dfb94e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499825"
---
# <span data-ttu-id="0acca-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0acca-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="0acca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0acca-102">SYNOPSIS</span></span>
<span data-ttu-id="0acca-103">Überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0acca-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="0acca-104">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0acca-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0acca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0acca-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="0acca-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0acca-106">DESCRIPTION</span></span>
<span data-ttu-id="0acca-107">Das Cmdlet " **Get-AzureRmMediaServiceNameAvailability** " überprüft, ob ein Mediendienst Name verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0acca-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="0acca-108">Mediendienst Namen sind global eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0acca-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="0acca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0acca-109">EXAMPLES</span></span>

### <span data-ttu-id="0acca-110">Beispiel 1: überprüfen, ob ein Mediendienst Name verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="0acca-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="0acca-111">Dieser Befehl überprüft, ob der Name MediaService1 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0acca-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="0acca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0acca-112">PARAMETERS</span></span>

### <span data-ttu-id="0acca-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="0acca-113">-AccountName</span></span>
<span data-ttu-id="0acca-114">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0acca-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0acca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0acca-115">-DefaultProfile</span></span>
<span data-ttu-id="0acca-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0acca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0acca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0acca-117">CommonParameters</span></span>
<span data-ttu-id="0acca-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0acca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0acca-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0acca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0acca-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0acca-120">INPUTS</span></span>

### <span data-ttu-id="0acca-121">Keine</span><span class="sxs-lookup"><span data-stu-id="0acca-121">None</span></span>
<span data-ttu-id="0acca-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0acca-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0acca-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0acca-123">OUTPUTS</span></span>

### <span data-ttu-id="0acca-124">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="0acca-124">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="0acca-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0acca-125">NOTES</span></span>

## <span data-ttu-id="0acca-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0acca-126">RELATED LINKS</span></span>

[<span data-ttu-id="0acca-127">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="0acca-127">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="0acca-128">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="0acca-128">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="0acca-129">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="0acca-129">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="0acca-130">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="0acca-130">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


