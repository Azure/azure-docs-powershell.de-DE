---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468787"
---
# <span data-ttu-id="cb072-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="cb072-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="cb072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb072-102">SYNOPSIS</span></span>
<span data-ttu-id="cb072-103">Listet die empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="cb072-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb072-104">SYNTAX</span></span>

### <span data-ttu-id="cb072-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb072-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb072-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb072-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb072-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb072-107">DESCRIPTION</span></span>
<span data-ttu-id="cb072-108">Listet empfangene Routen von einem Peering auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="cb072-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb072-109">EXAMPLES</span></span>

### <span data-ttu-id="cb072-110">Liste der 100 empfangenen Routen für ein Peering auf</span><span class="sxs-lookup"><span data-stu-id="cb072-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="cb072-111">Listet alle empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="cb072-112">Nach AS Path filtern</span><span class="sxs-lookup"><span data-stu-id="cb072-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="cb072-113">Listet alle empfangenen Routen für ein Peering mit einem Filter auf AS auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="cb072-114">Filtern nach RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="cb072-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="cb072-115">Listet alle empfangenen Routen für ein Peering mit einem Filter auf "RPKIValidationState" auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="cb072-116">Filtern nach OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="cb072-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="cb072-117">Listet alle empfangenen Routen für ein Peering mit einem Filter auf OriginAsValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="cb072-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="cb072-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb072-118">PARAMETERS</span></span>

### <span data-ttu-id="cb072-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="cb072-119">-AsPath</span></span>
<span data-ttu-id="cb072-120">Filtern nach AS-Pfad.</span><span class="sxs-lookup"><span data-stu-id="cb072-120">Filter by AS Path.</span></span>
<span data-ttu-id="cb072-121">Beispiel: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="cb072-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="cb072-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb072-122">-DefaultProfile</span></span>
<span data-ttu-id="cb072-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb072-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb072-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb072-124">-Name</span></span>
<span data-ttu-id="cb072-125">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="cb072-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="cb072-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="cb072-126">-OriginAsValidationState</span></span>
<span data-ttu-id="cb072-127">Filtern nach Origin AS-Gültigkeitsprüfungszustand.</span><span class="sxs-lookup"><span data-stu-id="cb072-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="cb072-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="cb072-128">-Prefix</span></span>
<span data-ttu-id="cb072-129">Nach Präfix filtern.</span><span class="sxs-lookup"><span data-stu-id="cb072-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="cb072-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb072-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb072-131">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb072-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="cb072-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb072-132">-ResourceId</span></span>
<span data-ttu-id="cb072-133">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cb072-133">The resource id string name.</span></span>

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

### <span data-ttu-id="cb072-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="cb072-134">-RPKIValidationState</span></span>
<span data-ttu-id="cb072-135">Filter nach RPKI-Überprüfungszustand.</span><span class="sxs-lookup"><span data-stu-id="cb072-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="cb072-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb072-136">CommonParameters</span></span>
<span data-ttu-id="cb072-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb072-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb072-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb072-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb072-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb072-139">INPUTS</span></span>

### <span data-ttu-id="cb072-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cb072-140">System.String</span></span>

## <span data-ttu-id="cb072-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb072-141">OUTPUTS</span></span>

### <span data-ttu-id="cb072-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="cb072-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="cb072-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb072-143">NOTES</span></span>

## <span data-ttu-id="cb072-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb072-144">RELATED LINKS</span></span>
