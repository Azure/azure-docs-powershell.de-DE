---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 45accc1c3fd52720d3764a9167f6354316a0c9fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479898"
---
# <span data-ttu-id="63d9c-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="63d9c-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="63d9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="63d9c-103">Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="63d9c-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63d9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63d9c-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63d9c-105">DESCRIPTION</span></span>
<span data-ttu-id="63d9c-106">Das Cmdlet " **Get-AzureRmVMExtensionImageType** " Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="63d9c-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="63d9c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63d9c-107">EXAMPLES</span></span>

### <span data-ttu-id="63d9c-108">Beispiel 1: Abrufen eines Erweiterungs Bild Typs</span><span class="sxs-lookup"><span data-stu-id="63d9c-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="63d9c-109">Dieser Befehl ruft den Typ der Erweiterungs Grafik für den angegebenen Verleger und Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="63d9c-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="63d9c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="63d9c-110">PARAMETERS</span></span>

### <span data-ttu-id="63d9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d9c-111">-DefaultProfile</span></span>
<span data-ttu-id="63d9c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63d9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d9c-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="63d9c-113">-Location</span></span>
<span data-ttu-id="63d9c-114">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="63d9c-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="63d9c-115">Dieses Cmdlet ruft den Typ für eine Erweiterung an der Position ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="63d9c-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d9c-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="63d9c-116">-PublisherName</span></span>
<span data-ttu-id="63d9c-117">Gibt den Namen des Herausgebers einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="63d9c-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="63d9c-118">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d9c-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="63d9c-119">Dieses Cmdlet ruft den Typ für eine Erweiterung des Herausgebers ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="63d9c-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d9c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d9c-120">CommonParameters</span></span>
<span data-ttu-id="63d9c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d9c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d9c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d9c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d9c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63d9c-123">INPUTS</span></span>

## <span data-ttu-id="63d9c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63d9c-124">OUTPUTS</span></span>

## <span data-ttu-id="63d9c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="63d9c-125">NOTES</span></span>

## <span data-ttu-id="63d9c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63d9c-126">RELATED LINKS</span></span>

[<span data-ttu-id="63d9c-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="63d9c-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="63d9c-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="63d9c-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


