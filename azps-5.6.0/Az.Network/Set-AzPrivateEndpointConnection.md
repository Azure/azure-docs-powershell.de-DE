---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7684072abbef4af8344cc07aa4bef6cab88ad3ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932355"
---
# <span data-ttu-id="ed52d-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed52d-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ed52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed52d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed52d-103">Aktualisiert einen privaten Endpunktverbindungszustand für den privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="ed52d-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="ed52d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed52d-104">SYNTAX</span></span>

### <span data-ttu-id="ed52d-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed52d-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed52d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ed52d-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed52d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed52d-107">DESCRIPTION</span></span>
<span data-ttu-id="ed52d-108">Das **Cmdlet Set-AzPrivateEndpointConnection** aktualisiert einen privaten Endpunktverbindungszustand für einen privaten Linkdienst.</span><span class="sxs-lookup"><span data-stu-id="ed52d-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="ed52d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed52d-109">EXAMPLES</span></span>

### <span data-ttu-id="ed52d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed52d-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="ed52d-111">In diesem Beispiel wird ein privater Endpunktverbindungszustand auf Genehmigt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ed52d-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="ed52d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed52d-112">PARAMETERS</span></span>

### <span data-ttu-id="ed52d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed52d-113">-DefaultProfile</span></span>
<span data-ttu-id="ed52d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed52d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed52d-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed52d-115">-Description</span></span>
<span data-ttu-id="ed52d-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="ed52d-116">The reason of action.</span></span>

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

### <span data-ttu-id="ed52d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed52d-117">-Name</span></span>
<span data-ttu-id="ed52d-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ed52d-118">The resource name.</span></span>

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

### <span data-ttu-id="ed52d-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="ed52d-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="ed52d-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="ed52d-120">The private link resource type.</span></span>

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

### <span data-ttu-id="ed52d-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="ed52d-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="ed52d-122">Die Ressource wurde genehmigt oder abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="ed52d-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed52d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed52d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed52d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed52d-124">The resource group name.</span></span>

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

### <span data-ttu-id="ed52d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed52d-125">-ResourceId</span></span>
<span data-ttu-id="ed52d-126">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="ed52d-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ed52d-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ed52d-127">-ServiceName</span></span>
<span data-ttu-id="ed52d-128">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="ed52d-128">The private link service name.</span></span>

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

### <span data-ttu-id="ed52d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed52d-129">CommonParameters</span></span>
<span data-ttu-id="ed52d-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed52d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed52d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed52d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed52d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed52d-132">INPUTS</span></span>

### <span data-ttu-id="ed52d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ed52d-133">System.String</span></span>

## <span data-ttu-id="ed52d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed52d-134">OUTPUTS</span></span>

### <span data-ttu-id="ed52d-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ed52d-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ed52d-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed52d-136">NOTES</span></span>

## <span data-ttu-id="ed52d-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed52d-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed52d-138">Genehmigen-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed52d-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ed52d-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed52d-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ed52d-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed52d-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ed52d-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ed52d-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)