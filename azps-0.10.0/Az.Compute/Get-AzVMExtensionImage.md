---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844592"
---
# <span data-ttu-id="9433b-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9433b-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="9433b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9433b-102">SYNOPSIS</span></span>
<span data-ttu-id="9433b-103">Ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="9433b-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="9433b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9433b-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9433b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9433b-105">DESCRIPTION</span></span>
<span data-ttu-id="9433b-106">Das Cmdlet " **Get-AzVMExtensionImage** " ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="9433b-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="9433b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9433b-107">EXAMPLES</span></span>

### <span data-ttu-id="9433b-108">Beispiel 1: Abrufen der Versionen eines Erweiterungs Bilds</span><span class="sxs-lookup"><span data-stu-id="9433b-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="9433b-109">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, Herausgeber und Typ ab.</span><span class="sxs-lookup"><span data-stu-id="9433b-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="9433b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9433b-110">PARAMETERS</span></span>

### <span data-ttu-id="9433b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9433b-111">-DefaultProfile</span></span>
<span data-ttu-id="9433b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9433b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9433b-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9433b-113">-FilterExpression</span></span>
<span data-ttu-id="9433b-114">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="9433b-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="9433b-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="9433b-115">-Location</span></span>
<span data-ttu-id="9433b-116">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="9433b-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="9433b-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9433b-117">-PublisherName</span></span>
<span data-ttu-id="9433b-118">Gibt den Namen eines Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="9433b-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="9433b-119">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9433b-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9433b-120">-Typ</span><span class="sxs-lookup"><span data-stu-id="9433b-120">-Type</span></span>
<span data-ttu-id="9433b-121">Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="9433b-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="9433b-122">Verwenden Sie zum Abrufen eines Erweiterungstyps das Get-AzVMExtensionImageType-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9433b-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="9433b-123">-Version</span><span class="sxs-lookup"><span data-stu-id="9433b-123">-Version</span></span>
<span data-ttu-id="9433b-124">Gibt die Version der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9433b-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9433b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9433b-125">CommonParameters</span></span>
<span data-ttu-id="9433b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9433b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9433b-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9433b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9433b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9433b-128">INPUTS</span></span>

### <span data-ttu-id="9433b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="9433b-129">None</span></span>
<span data-ttu-id="9433b-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9433b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9433b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9433b-131">OUTPUTS</span></span>

### <span data-ttu-id="9433b-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9433b-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="9433b-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="9433b-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="9433b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9433b-134">NOTES</span></span>

## <span data-ttu-id="9433b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9433b-135">RELATED LINKS</span></span>

[<span data-ttu-id="9433b-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9433b-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="9433b-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9433b-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9433b-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9433b-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


