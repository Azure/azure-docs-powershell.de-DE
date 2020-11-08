---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165791"
---
# <span data-ttu-id="32145-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="32145-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="32145-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32145-102">SYNOPSIS</span></span>
<span data-ttu-id="32145-103">Abrufen oder Auflisten der verfügbaren Network Virtual Appliance-SKUs im Inventar</span><span class="sxs-lookup"><span data-stu-id="32145-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="32145-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32145-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32145-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32145-105">DESCRIPTION</span></span>
<span data-ttu-id="32145-106">Die Get-AzNetworkVirtualApplianceSku ruft die verfügbaren Network Virtual Appliance-SKUs in der Microsoft Azure-Inventur ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="32145-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="32145-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32145-107">EXAMPLES</span></span>

### <span data-ttu-id="32145-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32145-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="32145-109">Besorgen Sie sich eine SKU nach Namen.</span><span class="sxs-lookup"><span data-stu-id="32145-109">Get a sku by name.</span></span>

### <span data-ttu-id="32145-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32145-110">Example 2</span></span>
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

<span data-ttu-id="32145-111">Auflisten aller verfügbaren SKUs der virtuellen Netzwerkanwendung.</span><span class="sxs-lookup"><span data-stu-id="32145-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="32145-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="32145-112">PARAMETERS</span></span>

### <span data-ttu-id="32145-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32145-113">-DefaultProfile</span></span>
<span data-ttu-id="32145-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32145-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32145-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="32145-115">-SkuName</span></span>
<span data-ttu-id="32145-116">Der SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="32145-116">The Sku name.</span></span>

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

### <span data-ttu-id="32145-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32145-117">CommonParameters</span></span>
<span data-ttu-id="32145-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32145-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32145-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32145-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32145-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32145-120">INPUTS</span></span>

### <span data-ttu-id="32145-121">Keine</span><span class="sxs-lookup"><span data-stu-id="32145-121">None</span></span>

## <span data-ttu-id="32145-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32145-122">OUTPUTS</span></span>

### <span data-ttu-id="32145-123">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="32145-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="32145-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="32145-124">NOTES</span></span>

## <span data-ttu-id="32145-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32145-125">RELATED LINKS</span></span>
