---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: b2ebc3e91f08c2aa33853c8a90c929b31877a014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824043"
---
# <span data-ttu-id="fa91a-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="fa91a-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="fa91a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa91a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa91a-103">Abrufen einer Liste der Peering-Dienstobjekte eines einzelnen Objekts</span><span class="sxs-lookup"><span data-stu-id="fa91a-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="fa91a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa91a-104">SYNTAX</span></span>

### <span data-ttu-id="fa91a-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa91a-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa91a-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="fa91a-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa91a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa91a-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa91a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa91a-108">DESCRIPTION</span></span>
<span data-ttu-id="fa91a-109">Ruft Peering Dienste für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fa91a-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="fa91a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa91a-110">EXAMPLES</span></span>

### <span data-ttu-id="fa91a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa91a-111">Example 1</span></span>
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

<span data-ttu-id="fa91a-112">Ruft einen peeringdienst für eine Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fa91a-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="fa91a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fa91a-113">Example 2</span></span>
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

<span data-ttu-id="fa91a-114">Ruft einen peeringdienst für eine Ressourcengruppe und einen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="fa91a-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="fa91a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fa91a-115">Example 3</span></span>
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

<span data-ttu-id="fa91a-116">Ruft einen peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="fa91a-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="fa91a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa91a-117">PARAMETERS</span></span>

### <span data-ttu-id="fa91a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa91a-118">-DefaultProfile</span></span>
<span data-ttu-id="fa91a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa91a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa91a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fa91a-120">-Name</span></span>
<span data-ttu-id="fa91a-121">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fa91a-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="fa91a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa91a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa91a-123">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="fa91a-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="fa91a-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fa91a-124">-ResourceId</span></span>
<span data-ttu-id="fa91a-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fa91a-125">The resource id string name.</span></span>

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

### <span data-ttu-id="fa91a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa91a-126">CommonParameters</span></span>
<span data-ttu-id="fa91a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa91a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa91a-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa91a-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa91a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa91a-129">INPUTS</span></span>

### <span data-ttu-id="fa91a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fa91a-130">System.String</span></span>

## <span data-ttu-id="fa91a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa91a-131">OUTPUTS</span></span>

### <span data-ttu-id="fa91a-132">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="fa91a-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="fa91a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa91a-133">NOTES</span></span>

## <span data-ttu-id="fa91a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa91a-134">RELATED LINKS</span></span>
