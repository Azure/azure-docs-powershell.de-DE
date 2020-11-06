---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505770"
---
# <span data-ttu-id="32162-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="32162-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="32162-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32162-102">SYNOPSIS</span></span>
<span data-ttu-id="32162-103">Ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="32162-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32162-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32162-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32162-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32162-105">DESCRIPTION</span></span>
<span data-ttu-id="32162-106">Das Cmdlet " **Get-AzureRmVMExtensionImage** " ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="32162-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="32162-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32162-107">EXAMPLES</span></span>

### <span data-ttu-id="32162-108">Beispiel 1: Abrufen der Versionen eines Erweiterungs Bilds</span><span class="sxs-lookup"><span data-stu-id="32162-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="32162-109">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, Herausgeber und Typ ab.</span><span class="sxs-lookup"><span data-stu-id="32162-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="32162-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="32162-110">PARAMETERS</span></span>

### <span data-ttu-id="32162-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32162-111">-DefaultProfile</span></span>
<span data-ttu-id="32162-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32162-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32162-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="32162-113">-FilterExpression</span></span>
<span data-ttu-id="32162-114">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="32162-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32162-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="32162-115">-Location</span></span>
<span data-ttu-id="32162-116">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="32162-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="32162-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32162-117">-PublisherName</span></span>
<span data-ttu-id="32162-118">Gibt den Namen eines Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="32162-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="32162-119">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32162-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="32162-120">-Typ</span><span class="sxs-lookup"><span data-stu-id="32162-120">-Type</span></span>
<span data-ttu-id="32162-121">Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="32162-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="32162-122">Verwenden Sie zum Abrufen eines Erweiterungstyps das Get-AzureRmVMExtensionImageType-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32162-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="32162-123">-Version</span><span class="sxs-lookup"><span data-stu-id="32162-123">-Version</span></span>
<span data-ttu-id="32162-124">Gibt die Version der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="32162-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32162-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32162-125">CommonParameters</span></span>
<span data-ttu-id="32162-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32162-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32162-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32162-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32162-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32162-128">INPUTS</span></span>

### <span data-ttu-id="32162-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32162-129">System.String</span></span>

## <span data-ttu-id="32162-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32162-130">OUTPUTS</span></span>

### <span data-ttu-id="32162-131">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="32162-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="32162-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="32162-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="32162-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="32162-133">NOTES</span></span>

## <span data-ttu-id="32162-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32162-134">RELATED LINKS</span></span>

[<span data-ttu-id="32162-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="32162-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="32162-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="32162-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="32162-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32162-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


