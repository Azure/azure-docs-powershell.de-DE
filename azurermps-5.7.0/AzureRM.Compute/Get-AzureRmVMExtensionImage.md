---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478625"
---
# <span data-ttu-id="1a273-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1a273-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="1a273-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a273-102">SYNOPSIS</span></span>
<span data-ttu-id="1a273-103">Ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="1a273-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a273-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a273-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a273-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a273-105">DESCRIPTION</span></span>
<span data-ttu-id="1a273-106">Das Cmdlet " **Get-AzureRmVMExtensionImage** " ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="1a273-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="1a273-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a273-107">EXAMPLES</span></span>

### <span data-ttu-id="1a273-108">Beispiel 1: Abrufen der Versionen eines Erweiterungs Bilds</span><span class="sxs-lookup"><span data-stu-id="1a273-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="1a273-109">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, Herausgeber und Typ ab.</span><span class="sxs-lookup"><span data-stu-id="1a273-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="1a273-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a273-110">PARAMETERS</span></span>

### <span data-ttu-id="1a273-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="1a273-111">-FilterExpression</span></span>
<span data-ttu-id="1a273-112">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="1a273-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a273-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="1a273-113">-Location</span></span>
<span data-ttu-id="1a273-114">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1a273-114">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a273-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1a273-115">-PublisherName</span></span>
<span data-ttu-id="1a273-116">Gibt den Namen eines Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="1a273-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="1a273-117">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a273-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a273-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="1a273-118">-Type</span></span>
<span data-ttu-id="1a273-119">Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1a273-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="1a273-120">Verwenden Sie zum Abrufen eines Erweiterungstyps das Get-AzureRmVMExtensionImageType-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a273-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a273-121">-Version</span><span class="sxs-lookup"><span data-stu-id="1a273-121">-Version</span></span>
<span data-ttu-id="1a273-122">Gibt die Version der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1a273-122">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a273-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a273-123">CommonParameters</span></span>
<span data-ttu-id="1a273-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a273-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a273-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a273-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a273-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a273-126">INPUTS</span></span>

### <span data-ttu-id="1a273-127">Keine</span><span class="sxs-lookup"><span data-stu-id="1a273-127">None</span></span>
<span data-ttu-id="1a273-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1a273-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a273-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a273-129">OUTPUTS</span></span>

## <span data-ttu-id="1a273-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a273-130">NOTES</span></span>

## <span data-ttu-id="1a273-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a273-131">RELATED LINKS</span></span>

[<span data-ttu-id="1a273-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1a273-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="1a273-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1a273-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="1a273-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1a273-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


