---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467403"
---
# <span data-ttu-id="c4bc7-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c4bc7-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c4bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bc7-103">Genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="c4bc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4bc7-104">SYNTAX</span></span>

### <span data-ttu-id="c4bc7-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4bc7-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4bc7-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c4bc7-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4bc7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4bc7-107">DESCRIPTION</span></span>
<span data-ttu-id="c4bc7-108">Das **Cmdlet "Approve-AzPrivateEndpointConnection"** genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="c4bc7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4bc7-109">EXAMPLES</span></span>

### <span data-ttu-id="c4bc7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4bc7-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="c4bc7-111">In diesem Beispiel wird eine private Endpunktverbindung genehmigt.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="c4bc7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4bc7-112">PARAMETERS</span></span>

### <span data-ttu-id="c4bc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bc7-113">-DefaultProfile</span></span>
<span data-ttu-id="c4bc7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bc7-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4bc7-115">-Description</span></span>
<span data-ttu-id="c4bc7-116">Der Grund der Aktion.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bc7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c4bc7-117">-Name</span></span>
<span data-ttu-id="c4bc7-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bc7-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="c4bc7-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="c4bc7-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bc7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4bc7-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4bc7-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bc7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bc7-123">-ResourceId</span></span>
<span data-ttu-id="c4bc7-124">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bc7-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4bc7-125">-ServiceName</span></span>
<span data-ttu-id="c4bc7-126">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-126">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```


### <span data-ttu-id="c4bc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bc7-127">CommonParameters</span></span>
<span data-ttu-id="c4bc7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bc7-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4bc7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bc7-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4bc7-130">INPUTS</span></span>

### <span data-ttu-id="c4bc7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c4bc7-131">System.String</span></span>

## <span data-ttu-id="c4bc7-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4bc7-132">OUTPUTS</span></span>

### <span data-ttu-id="c4bc7-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c4bc7-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c4bc7-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4bc7-134">NOTES</span></span>

## <span data-ttu-id="c4bc7-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4bc7-135">RELATED LINKS</span></span>

[<span data-ttu-id="c4bc7-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c4bc7-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c4bc7-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c4bc7-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c4bc7-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c4bc7-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c4bc7-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c4bc7-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)