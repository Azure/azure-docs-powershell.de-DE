---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004694"
---
# <span data-ttu-id="5b92b-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="5b92b-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="5b92b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b92b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b92b-103">Abrufen einer Liste der Peering-Dienstobjekte eines einzelnen Objekts</span><span class="sxs-lookup"><span data-stu-id="5b92b-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="5b92b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b92b-104">SYNTAX</span></span>

### <span data-ttu-id="5b92b-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b92b-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b92b-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="5b92b-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b92b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b92b-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b92b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b92b-108">DESCRIPTION</span></span>
<span data-ttu-id="5b92b-109">Ruft Peering Dienste für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5b92b-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="5b92b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b92b-110">EXAMPLES</span></span>

### <span data-ttu-id="5b92b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b92b-111">Example 1</span></span>
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

<span data-ttu-id="5b92b-112">Ruft einen peeringdienst für eine Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5b92b-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="5b92b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b92b-113">Example 2</span></span>
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

<span data-ttu-id="5b92b-114">Ruft einen peeringdienst für eine Ressourcengruppe und einen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="5b92b-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="5b92b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b92b-115">Example 3</span></span>
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

<span data-ttu-id="5b92b-116">Ruft einen peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="5b92b-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="5b92b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b92b-117">PARAMETERS</span></span>

### <span data-ttu-id="5b92b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b92b-118">-DefaultProfile</span></span>
<span data-ttu-id="5b92b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b92b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b92b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b92b-120">-Name</span></span>
<span data-ttu-id="5b92b-121">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5b92b-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5b92b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b92b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b92b-123">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="5b92b-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="5b92b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b92b-124">-ResourceId</span></span>
<span data-ttu-id="5b92b-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5b92b-125">The resource id string name.</span></span>

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

### <span data-ttu-id="5b92b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b92b-126">CommonParameters</span></span>
<span data-ttu-id="5b92b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b92b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b92b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b92b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b92b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b92b-129">INPUTS</span></span>

### <span data-ttu-id="5b92b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5b92b-130">System.String</span></span>

## <span data-ttu-id="5b92b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b92b-131">OUTPUTS</span></span>

### <span data-ttu-id="5b92b-132">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="5b92b-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="5b92b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b92b-133">NOTES</span></span>

## <span data-ttu-id="5b92b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b92b-134">RELATED LINKS</span></span>
