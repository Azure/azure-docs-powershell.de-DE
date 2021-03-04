---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e165b481b1321f5ddd81766452120f55f6f0e153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919880"
---
# <span data-ttu-id="ae863-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="ae863-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="ae863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae863-102">SYNOPSIS</span></span>
<span data-ttu-id="ae863-103">Erhalten oder Auflisten verfügbarer virtueller Netzwerkgeräte-Skus im Bestand.</span><span class="sxs-lookup"><span data-stu-id="ae863-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="ae863-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae863-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae863-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae863-105">DESCRIPTION</span></span>
<span data-ttu-id="ae863-106">Die Get-AzNetworkVirtualApplianceSku ruft verfügbare virtuelle Netzwerkgeräte-Skus im Microsoft Azure-Inventar ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="ae863-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="ae863-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae863-107">EXAMPLES</span></span>

### <span data-ttu-id="ae863-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae863-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="ae863-109">Holen Sie sich eine Sku nach Name.</span><span class="sxs-lookup"><span data-stu-id="ae863-109">Get a sku by name.</span></span>

### <span data-ttu-id="ae863-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ae863-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="ae863-111">Listen Sie alle verfügbaren Skus der virtuellen Netzwerkgeräte auf.</span><span class="sxs-lookup"><span data-stu-id="ae863-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="ae863-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae863-112">PARAMETERS</span></span>

### <span data-ttu-id="ae863-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae863-113">-DefaultProfile</span></span>
<span data-ttu-id="ae863-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae863-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae863-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ae863-115">-SkuName</span></span>
<span data-ttu-id="ae863-116">Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="ae863-116">The Sku name.</span></span>

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

### <span data-ttu-id="ae863-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae863-117">CommonParameters</span></span>
<span data-ttu-id="ae863-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae863-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae863-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae863-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae863-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae863-120">INPUTS</span></span>

### <span data-ttu-id="ae863-121">Keine</span><span class="sxs-lookup"><span data-stu-id="ae863-121">None</span></span>

## <span data-ttu-id="ae863-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae863-122">OUTPUTS</span></span>

### <span data-ttu-id="ae863-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="ae863-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="ae863-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ae863-124">NOTES</span></span>

## <span data-ttu-id="ae863-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ae863-125">RELATED LINKS</span></span>
