---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379922"
---
# <span data-ttu-id="b4227-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b4227-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b4227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4227-102">SYNOPSIS</span></span>
<span data-ttu-id="b4227-103">Holen Sie sich die verfügbaren SKU für virtuelle Network Appliances in den Bestand, oder listen Sie sie auf.</span><span class="sxs-lookup"><span data-stu-id="b4227-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="b4227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4227-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4227-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4227-105">DESCRIPTION</span></span>
<span data-ttu-id="b4227-106">Die Get-AzNetworkVirtualApplianceSku die im Microsoft Azure-Bestand verfügbaren virtuellen Network Appliance-SKU erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="b4227-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="b4227-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4227-107">EXAMPLES</span></span>

### <span data-ttu-id="b4227-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4227-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="b4227-109">Holen Sie sich eine SKU nach Name.</span><span class="sxs-lookup"><span data-stu-id="b4227-109">Get a sku by name.</span></span>

### <span data-ttu-id="b4227-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4227-110">Example 2</span></span>
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

<span data-ttu-id="b4227-111">Listet alle verfügbaren SKUs der virtuellen Network Appliance auf.</span><span class="sxs-lookup"><span data-stu-id="b4227-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="b4227-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4227-112">PARAMETERS</span></span>

### <span data-ttu-id="b4227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4227-113">-DefaultProfile</span></span>
<span data-ttu-id="b4227-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4227-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4227-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4227-115">-SkuName</span></span>
<span data-ttu-id="b4227-116">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="b4227-116">The Sku name.</span></span>

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

### <span data-ttu-id="b4227-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4227-117">CommonParameters</span></span>
<span data-ttu-id="b4227-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4227-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4227-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4227-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4227-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4227-120">INPUTS</span></span>

### <span data-ttu-id="b4227-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b4227-121">None</span></span>

## <span data-ttu-id="b4227-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4227-122">OUTPUTS</span></span>

### <span data-ttu-id="b4227-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="b4227-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="b4227-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4227-124">NOTES</span></span>

## <span data-ttu-id="b4227-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4227-125">RELATED LINKS</span></span>
