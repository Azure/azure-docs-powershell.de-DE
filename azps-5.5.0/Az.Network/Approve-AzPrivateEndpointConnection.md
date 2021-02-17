---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172929"
---
# <span data-ttu-id="84358-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="84358-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="84358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84358-102">SYNOPSIS</span></span>
<span data-ttu-id="84358-103">Genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="84358-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="84358-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84358-104">SYNTAX</span></span>

### <span data-ttu-id="84358-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="84358-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84358-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="84358-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84358-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84358-107">DESCRIPTION</span></span>
<span data-ttu-id="84358-108">Das **Cmdlet "Approve-AzPrivateEndpointConnection"** genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="84358-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="84358-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84358-109">EXAMPLES</span></span>

### <span data-ttu-id="84358-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84358-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="84358-111">In diesem Beispiel wird eine private Endpunktverbindung genehmigt.</span><span class="sxs-lookup"><span data-stu-id="84358-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="84358-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84358-112">PARAMETERS</span></span>

### <span data-ttu-id="84358-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84358-113">-DefaultProfile</span></span>
<span data-ttu-id="84358-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84358-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84358-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84358-115">-Description</span></span>
<span data-ttu-id="84358-116">Der Grund der Aktion.</span><span class="sxs-lookup"><span data-stu-id="84358-116">The reason of action.</span></span>

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

### <span data-ttu-id="84358-117">-Name</span><span class="sxs-lookup"><span data-stu-id="84358-117">-Name</span></span>
<span data-ttu-id="84358-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="84358-118">The resource name.</span></span>

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

### <span data-ttu-id="84358-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="84358-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="84358-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="84358-120">The private link resource type.</span></span>

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

### <span data-ttu-id="84358-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84358-121">-ResourceGroupName</span></span>
<span data-ttu-id="84358-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84358-122">The resource group name.</span></span>

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

### <span data-ttu-id="84358-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84358-123">-ResourceId</span></span>
<span data-ttu-id="84358-124">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="84358-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="84358-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="84358-125">-ServiceName</span></span>
<span data-ttu-id="84358-126">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="84358-126">The private link service name.</span></span>

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


### <span data-ttu-id="84358-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84358-127">CommonParameters</span></span>
<span data-ttu-id="84358-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84358-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84358-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84358-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84358-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84358-130">INPUTS</span></span>

### <span data-ttu-id="84358-131">System.String</span><span class="sxs-lookup"><span data-stu-id="84358-131">System.String</span></span>

## <span data-ttu-id="84358-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84358-132">OUTPUTS</span></span>

### <span data-ttu-id="84358-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="84358-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="84358-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="84358-134">NOTES</span></span>

## <span data-ttu-id="84358-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="84358-135">RELATED LINKS</span></span>

[<span data-ttu-id="84358-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="84358-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="84358-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="84358-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="84358-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="84358-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="84358-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="84358-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)