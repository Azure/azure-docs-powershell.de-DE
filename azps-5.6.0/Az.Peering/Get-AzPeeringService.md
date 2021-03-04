---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937728"
---
# <span data-ttu-id="871ae-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="871ae-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="871ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="871ae-102">SYNOPSIS</span></span>
<span data-ttu-id="871ae-103">Hier erhalten Sie eine Liste der Peeringdienstobjekte eines einzelnen Objekts.</span><span class="sxs-lookup"><span data-stu-id="871ae-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="871ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="871ae-104">SYNTAX</span></span>

### <span data-ttu-id="871ae-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="871ae-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="871ae-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="871ae-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="871ae-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="871ae-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="871ae-108">DESCRIPTION</span></span>
<span data-ttu-id="871ae-109">Ruft Peeringdienste für ein Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="871ae-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="871ae-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="871ae-110">EXAMPLES</span></span>

### <span data-ttu-id="871ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="871ae-111">Example 1</span></span>
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

<span data-ttu-id="871ae-112">Ruft einen Peeringdienst für eine Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="871ae-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="871ae-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="871ae-113">Example 2</span></span>
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

<span data-ttu-id="871ae-114">Ruft einen Peeringdienst für eine Ressourcengruppe und einen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="871ae-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="871ae-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="871ae-115">Example 3</span></span>
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

<span data-ttu-id="871ae-116">Ruft einen Peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="871ae-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="871ae-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="871ae-117">PARAMETERS</span></span>

### <span data-ttu-id="871ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871ae-118">-DefaultProfile</span></span>
<span data-ttu-id="871ae-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="871ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="871ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="871ae-120">-Name</span></span>
<span data-ttu-id="871ae-121">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="871ae-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="871ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="871ae-123">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="871ae-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="871ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="871ae-124">-ResourceId</span></span>
<span data-ttu-id="871ae-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="871ae-125">The resource id string name.</span></span>

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

### <span data-ttu-id="871ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871ae-126">CommonParameters</span></span>
<span data-ttu-id="871ae-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871ae-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="871ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871ae-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="871ae-129">INPUTS</span></span>

### <span data-ttu-id="871ae-130">System.String</span><span class="sxs-lookup"><span data-stu-id="871ae-130">System.String</span></span>

## <span data-ttu-id="871ae-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="871ae-131">OUTPUTS</span></span>

### <span data-ttu-id="871ae-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="871ae-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="871ae-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="871ae-133">NOTES</span></span>

## <span data-ttu-id="871ae-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="871ae-134">RELATED LINKS</span></span>
