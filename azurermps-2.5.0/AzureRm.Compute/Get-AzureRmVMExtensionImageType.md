---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849396"
---
# <span data-ttu-id="a5cfa-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a5cfa-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="a5cfa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cfa-103">Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5cfa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5cfa-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5cfa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cfa-106">Das Cmdlet " **Get-AzureRmVMExtensionImageType** " Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="a5cfa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="a5cfa-108">Beispiel 1: Abrufen eines Erweiterungs Bild Typs</span><span class="sxs-lookup"><span data-stu-id="a5cfa-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="a5cfa-109">Dieser Befehl ruft den Typ der Erweiterungs Grafik für den angegebenen Verleger und Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="a5cfa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="a5cfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cfa-111">-DefaultProfile</span></span>
<span data-ttu-id="a5cfa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5cfa-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="a5cfa-113">-Location</span></span>
<span data-ttu-id="a5cfa-114">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="a5cfa-115">Dieses Cmdlet ruft den Typ für eine Erweiterung an der Position ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5cfa-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a5cfa-116">-PublisherName</span></span>
<span data-ttu-id="a5cfa-117">Gibt den Namen des Herausgebers einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="a5cfa-118">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="a5cfa-119">Dieses Cmdlet ruft den Typ für eine Erweiterung des Herausgebers ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5cfa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cfa-120">CommonParameters</span></span>
<span data-ttu-id="a5cfa-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cfa-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5cfa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cfa-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5cfa-123">INPUTS</span></span>

### <span data-ttu-id="a5cfa-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a5cfa-124">None</span></span>
<span data-ttu-id="a5cfa-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a5cfa-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5cfa-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5cfa-126">OUTPUTS</span></span>

### <span data-ttu-id="a5cfa-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a5cfa-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="a5cfa-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5cfa-128">NOTES</span></span>

## <span data-ttu-id="a5cfa-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5cfa-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5cfa-130">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a5cfa-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="a5cfa-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a5cfa-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


