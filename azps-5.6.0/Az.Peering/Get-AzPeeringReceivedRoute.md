---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: e5f961b5bd3acc1db716d68f43147e1a6c5611f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937784"
---
# <span data-ttu-id="4140d-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="4140d-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="4140d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4140d-102">SYNOPSIS</span></span>
<span data-ttu-id="4140d-103">Listet die empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="4140d-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="4140d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4140d-104">SYNTAX</span></span>

### <span data-ttu-id="4140d-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4140d-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4140d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4140d-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4140d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4140d-107">DESCRIPTION</span></span>
<span data-ttu-id="4140d-108">Listen empfangener Routen von einem Peering</span><span class="sxs-lookup"><span data-stu-id="4140d-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="4140d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4140d-109">EXAMPLES</span></span>

### <span data-ttu-id="4140d-110">Liste der top 100 empfangenen Routen für ein Peering</span><span class="sxs-lookup"><span data-stu-id="4140d-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="4140d-111">Listet alle empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="4140d-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="4140d-112">Filtern nach AS-Pfad</span><span class="sxs-lookup"><span data-stu-id="4140d-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="4140d-113">Listet alle empfangenen Routen für ein Peering mit einem Filter auf AS auf.</span><span class="sxs-lookup"><span data-stu-id="4140d-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="4140d-114">Filtern nach RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="4140d-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="4140d-115">Listet alle empfangenen Routen für ein Peering mit einem Filter in RPKIValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="4140d-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="4140d-116">Filtern nach OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="4140d-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="4140d-117">Listet alle empfangenen Routen für ein Peering mit einem Filter in OriginAsValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="4140d-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="4140d-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4140d-118">PARAMETERS</span></span>

### <span data-ttu-id="4140d-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="4140d-119">-AsPath</span></span>
<span data-ttu-id="4140d-120">Filtern sie nach AS-Pfad.</span><span class="sxs-lookup"><span data-stu-id="4140d-120">Filter by AS Path.</span></span>
<span data-ttu-id="4140d-121">Beispiel: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="4140d-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="4140d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4140d-122">-DefaultProfile</span></span>
<span data-ttu-id="4140d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4140d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4140d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4140d-124">-Name</span></span>
<span data-ttu-id="4140d-125">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="4140d-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4140d-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="4140d-126">-OriginAsValidationState</span></span>
<span data-ttu-id="4140d-127">Filtern sie nach Dem Herkunfts-AS-Gültigkeitszustand.</span><span class="sxs-lookup"><span data-stu-id="4140d-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="4140d-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4140d-128">-Prefix</span></span>
<span data-ttu-id="4140d-129">Filtern sie nach Präfix.</span><span class="sxs-lookup"><span data-stu-id="4140d-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="4140d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4140d-130">-ResourceGroupName</span></span>
<span data-ttu-id="4140d-131">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="4140d-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4140d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4140d-132">-ResourceId</span></span>
<span data-ttu-id="4140d-133">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4140d-133">The resource id string name.</span></span>

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

### <span data-ttu-id="4140d-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="4140d-134">-RPKIValidationState</span></span>
<span data-ttu-id="4140d-135">Filtern sie nach DEM STATUS der RPKI-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="4140d-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="4140d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4140d-136">CommonParameters</span></span>
<span data-ttu-id="4140d-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4140d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4140d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4140d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4140d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4140d-139">INPUTS</span></span>

### <span data-ttu-id="4140d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4140d-140">System.String</span></span>

## <span data-ttu-id="4140d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4140d-141">OUTPUTS</span></span>

### <span data-ttu-id="4140d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="4140d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="4140d-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4140d-143">NOTES</span></span>

## <span data-ttu-id="4140d-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4140d-144">RELATED LINKS</span></span>
