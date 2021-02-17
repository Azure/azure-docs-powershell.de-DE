---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172320"
---
# <span data-ttu-id="541fb-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="541fb-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="541fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="541fb-102">SYNOPSIS</span></span>
<span data-ttu-id="541fb-103">Hier erhalten Sie eine Liste der Peeringdienstobjekte eines einzelnen Objekts.</span><span class="sxs-lookup"><span data-stu-id="541fb-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="541fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="541fb-104">SYNTAX</span></span>

### <span data-ttu-id="541fb-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="541fb-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="541fb-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="541fb-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="541fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="541fb-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="541fb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="541fb-108">DESCRIPTION</span></span>
<span data-ttu-id="541fb-109">Ruft Peeringdienste für ein Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="541fb-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="541fb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="541fb-110">EXAMPLES</span></span>

### <span data-ttu-id="541fb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="541fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="541fb-112">Ruft einen Peeringdienst für eine Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="541fb-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="541fb-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="541fb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="541fb-114">Ruft einen Peeringdienst für eine Ressourcengruppe und einen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="541fb-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="541fb-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="541fb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="541fb-116">Ruft einen Peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="541fb-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="541fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="541fb-117">PARAMETERS</span></span>

### <span data-ttu-id="541fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541fb-118">-DefaultProfile</span></span>
<span data-ttu-id="541fb-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="541fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="541fb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="541fb-120">-Name</span></span>
<span data-ttu-id="541fb-121">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="541fb-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="541fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="541fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="541fb-123">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="541fb-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="541fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="541fb-124">-ResourceId</span></span>
<span data-ttu-id="541fb-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="541fb-125">The resource id string name.</span></span>

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

### <span data-ttu-id="541fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541fb-126">CommonParameters</span></span>
<span data-ttu-id="541fb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="541fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541fb-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="541fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541fb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="541fb-129">INPUTS</span></span>

### <span data-ttu-id="541fb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="541fb-130">System.String</span></span>

## <span data-ttu-id="541fb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="541fb-131">OUTPUTS</span></span>

### <span data-ttu-id="541fb-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="541fb-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="541fb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="541fb-133">NOTES</span></span>

## <span data-ttu-id="541fb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="541fb-134">RELATED LINKS</span></span>
