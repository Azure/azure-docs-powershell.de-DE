---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 4218dd5441c4f580c89d770556f2d5c329cfd06c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937776"
---
# <span data-ttu-id="ba7f0-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="ba7f0-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="ba7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7f0-103">Ruft den registrierten ASN für Internet Exchange-Routenservertyp-Peerings ab.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="ba7f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba7f0-104">SYNTAX</span></span>

### <span data-ttu-id="ba7f0-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba7f0-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7f0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ba7f0-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7f0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba7f0-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba7f0-108">DESCRIPTION</span></span>
<span data-ttu-id="ba7f0-109">Sie können einen registrierten ASN erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="ba7f0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba7f0-110">EXAMPLES</span></span>

### <span data-ttu-id="ba7f0-111">Liste registrierter ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="ba7f0-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="ba7f0-112">Listen, die als registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-112">Lists registered asn.</span></span>

### <span data-ttu-id="ba7f0-113">Ruft registriertes ASN für Peering nach Name ab</span><span class="sxs-lookup"><span data-stu-id="ba7f0-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="ba7f0-114">Ruft registriertes Peering ab.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="ba7f0-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba7f0-115">PARAMETERS</span></span>

### <span data-ttu-id="ba7f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7f0-116">-DefaultProfile</span></span>
<span data-ttu-id="ba7f0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba7f0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba7f0-118">-InputObject</span></span>
<span data-ttu-id="ba7f0-119">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="ba7f0-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="ba7f0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ba7f0-120">-Name</span></span>
<span data-ttu-id="ba7f0-121">Der Name des registrierten ASN</span><span class="sxs-lookup"><span data-stu-id="ba7f0-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="ba7f0-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ba7f0-122">-PeeringName</span></span>
<span data-ttu-id="ba7f0-123">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ba7f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba7f0-125">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ba7f0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba7f0-126">-ResourceId</span></span>
<span data-ttu-id="ba7f0-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-127">The resource id string name.</span></span>

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

### <span data-ttu-id="ba7f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7f0-128">CommonParameters</span></span>
<span data-ttu-id="ba7f0-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7f0-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba7f0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7f0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba7f0-131">INPUTS</span></span>

### <span data-ttu-id="ba7f0-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="ba7f0-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="ba7f0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ba7f0-133">System.String</span></span>

## <span data-ttu-id="ba7f0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba7f0-134">OUTPUTS</span></span>

### <span data-ttu-id="ba7f0-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="ba7f0-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="ba7f0-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba7f0-136">NOTES</span></span>

## <span data-ttu-id="ba7f0-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba7f0-137">RELATED LINKS</span></span>
