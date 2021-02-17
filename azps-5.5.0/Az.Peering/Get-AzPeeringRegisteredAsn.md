---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169521"
---
# <span data-ttu-id="eb527-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="eb527-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="eb527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb527-102">SYNOPSIS</span></span>
<span data-ttu-id="eb527-103">Ruft den registrierten ASN für Peerings vom Typ "Internet Exchange-Routeserver" ab.</span><span class="sxs-lookup"><span data-stu-id="eb527-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="eb527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb527-104">SYNTAX</span></span>

### <span data-ttu-id="eb527-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb527-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb527-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb527-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb527-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb527-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb527-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb527-108">DESCRIPTION</span></span>
<span data-ttu-id="eb527-109">Sie können einen registrierten ASN erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="eb527-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="eb527-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb527-110">EXAMPLES</span></span>

### <span data-ttu-id="eb527-111">Liste registrierter ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="eb527-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="eb527-112">Listen, die als "registriert" registriert sind.</span><span class="sxs-lookup"><span data-stu-id="eb527-112">Lists registered asn.</span></span>

### <span data-ttu-id="eb527-113">Wird asN für Peering nach Name registriert</span><span class="sxs-lookup"><span data-stu-id="eb527-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="eb527-114">Ruft asn registriertes Peering ab.</span><span class="sxs-lookup"><span data-stu-id="eb527-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="eb527-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb527-115">PARAMETERS</span></span>

### <span data-ttu-id="eb527-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb527-116">-DefaultProfile</span></span>
<span data-ttu-id="eb527-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb527-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb527-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb527-118">-InputObject</span></span>
<span data-ttu-id="eb527-119">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="eb527-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb527-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eb527-120">-Name</span></span>
<span data-ttu-id="eb527-121">Der Name des registrierten ASNs</span><span class="sxs-lookup"><span data-stu-id="eb527-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb527-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="eb527-122">-PeeringName</span></span>
<span data-ttu-id="eb527-123">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="eb527-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb527-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb527-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb527-125">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb527-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb527-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb527-126">-ResourceId</span></span>
<span data-ttu-id="eb527-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="eb527-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb527-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb527-128">CommonParameters</span></span>
<span data-ttu-id="eb527-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb527-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb527-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb527-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb527-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb527-131">INPUTS</span></span>

### <span data-ttu-id="eb527-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="eb527-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="eb527-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eb527-133">System.String</span></span>

## <span data-ttu-id="eb527-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb527-134">OUTPUTS</span></span>

### <span data-ttu-id="eb527-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="eb527-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="eb527-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb527-136">NOTES</span></span>

## <span data-ttu-id="eb527-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb527-137">RELATED LINKS</span></span>
