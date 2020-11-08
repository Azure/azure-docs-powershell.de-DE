---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003092"
---
# <span data-ttu-id="c5e93-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c5e93-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="c5e93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5e93-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e93-103">Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="c5e93-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="c5e93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e93-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5e93-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5e93-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e93-106">Das Cmdlet " **Get-AzVMExtensionImageType** " Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="c5e93-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="c5e93-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5e93-107">EXAMPLES</span></span>

### <span data-ttu-id="c5e93-108">Beispiel 1: Abrufen eines Erweiterungs Bild Typs</span><span class="sxs-lookup"><span data-stu-id="c5e93-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="c5e93-109">Dieser Befehl ruft den Typ der Erweiterungs Grafik für den angegebenen Verleger und Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="c5e93-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="c5e93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e93-110">PARAMETERS</span></span>

### <span data-ttu-id="c5e93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e93-111">-DefaultProfile</span></span>
<span data-ttu-id="c5e93-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5e93-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e93-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="c5e93-113">-Location</span></span>
<span data-ttu-id="c5e93-114">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c5e93-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="c5e93-115">Dieses Cmdlet ruft den Typ für eine Erweiterung an der Position ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c5e93-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5e93-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c5e93-116">-PublisherName</span></span>
<span data-ttu-id="c5e93-117">Gibt den Namen des Herausgebers einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c5e93-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="c5e93-118">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e93-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="c5e93-119">Dieses Cmdlet ruft den Typ für eine Erweiterung des Herausgebers ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c5e93-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5e93-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e93-120">CommonParameters</span></span>
<span data-ttu-id="c5e93-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e93-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e93-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5e93-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e93-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5e93-123">INPUTS</span></span>

### <span data-ttu-id="c5e93-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e93-124">System.String</span></span>

## <span data-ttu-id="c5e93-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5e93-125">OUTPUTS</span></span>

### <span data-ttu-id="c5e93-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c5e93-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="c5e93-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5e93-127">NOTES</span></span>

## <span data-ttu-id="c5e93-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5e93-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5e93-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c5e93-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="c5e93-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c5e93-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


