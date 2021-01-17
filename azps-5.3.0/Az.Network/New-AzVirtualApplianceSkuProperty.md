---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385382"
---
# <span data-ttu-id="a9ce4-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="a9ce4-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="a9ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ce4-103">Definieren Sie eine Network Virtual Appliance-SKU für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="a9ce4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9ce4-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ce4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ce4-106">Der New-AzVirtualApplianceSkuProperties definiert eine SKU für die Ressource "Network Virtual Appliance".</span><span class="sxs-lookup"><span data-stu-id="a9ce4-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a9ce4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ce4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9ce4-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="a9ce4-109">Erstellen Sie ein Virtual Appliance SKU Properties-Objekt, das mit dem Befehl New-AzNetworkVirtualAppliance wird.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="a9ce4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9ce4-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ce4-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a9ce4-111">-BundledScaleUnit</span></span>
<span data-ttu-id="a9ce4-112">Die gebündelte Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="a9ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="a9ce4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ce4-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="a9ce4-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="a9ce4-116">Die Marktversion.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-116">The market place version.</span></span>

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

### <span data-ttu-id="a9ce4-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="a9ce4-117">-VendorName</span></span>
<span data-ttu-id="a9ce4-118">Der Name des Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="a9ce4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ce4-119">CommonParameters</span></span>
<span data-ttu-id="a9ce4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ce4-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9ce4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ce4-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9ce4-122">INPUTS</span></span>

### <span data-ttu-id="a9ce4-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a9ce4-123">None</span></span>

## <span data-ttu-id="a9ce4-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9ce4-124">OUTPUTS</span></span>

### <span data-ttu-id="a9ce4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="a9ce4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="a9ce4-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9ce4-126">NOTES</span></span>

## <span data-ttu-id="a9ce4-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9ce4-127">RELATED LINKS</span></span>
