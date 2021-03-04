---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945904"
---
# <span data-ttu-id="899a7-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="899a7-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="899a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899a7-102">SYNOPSIS</span></span>
<span data-ttu-id="899a7-103">Definieren Sie eine Sku für virtuelle Netzwerkgeräte für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="899a7-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="899a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="899a7-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="899a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="899a7-105">DESCRIPTION</span></span>
<span data-ttu-id="899a7-106">Der New-AzVirtualApplianceSkuProperties definiert eine Sku für virtuelle Netzwerkgeräteressource.</span><span class="sxs-lookup"><span data-stu-id="899a7-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="899a7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="899a7-107">EXAMPLES</span></span>

### <span data-ttu-id="899a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="899a7-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="899a7-109">Erstellen Sie ein Virtual Appliance Sku Properties-Objekt, das mit dem Befehl New-AzNetworkVirtualAppliance wird.</span><span class="sxs-lookup"><span data-stu-id="899a7-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="899a7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="899a7-110">PARAMETERS</span></span>

### <span data-ttu-id="899a7-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="899a7-111">-BundledScaleUnit</span></span>
<span data-ttu-id="899a7-112">Die gebündelte Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="899a7-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899a7-113">-DefaultProfile</span></span>
<span data-ttu-id="899a7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="899a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="899a7-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="899a7-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="899a7-116">Die Market Place-Version.</span><span class="sxs-lookup"><span data-stu-id="899a7-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899a7-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="899a7-117">-VendorName</span></span>
<span data-ttu-id="899a7-118">Der Name des Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="899a7-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899a7-119">CommonParameters</span></span>
<span data-ttu-id="899a7-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899a7-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="899a7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899a7-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="899a7-122">INPUTS</span></span>

### <span data-ttu-id="899a7-123">Keine</span><span class="sxs-lookup"><span data-stu-id="899a7-123">None</span></span>

## <span data-ttu-id="899a7-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="899a7-124">OUTPUTS</span></span>

### <span data-ttu-id="899a7-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="899a7-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="899a7-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="899a7-126">NOTES</span></span>

## <span data-ttu-id="899a7-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="899a7-127">RELATED LINKS</span></span>
