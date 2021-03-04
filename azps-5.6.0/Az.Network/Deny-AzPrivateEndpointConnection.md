---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 1522e8d9c66ccd2429ab331e1f39d26c06da5930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931819"
---
# <span data-ttu-id="04411-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04411-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="04411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04411-102">SYNOPSIS</span></span>
<span data-ttu-id="04411-103">verweigert eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="04411-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="04411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04411-104">SYNTAX</span></span>

### <span data-ttu-id="04411-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="04411-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04411-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="04411-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04411-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04411-107">DESCRIPTION</span></span>
<span data-ttu-id="04411-108">Das **Cmdlet Deny-AzPrivateEndpointConnection** verweigert eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="04411-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="04411-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04411-109">EXAMPLES</span></span>

### <span data-ttu-id="04411-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04411-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="04411-111">In diesem Beispiel wird eine private Endpunktverbindung verweigert.</span><span class="sxs-lookup"><span data-stu-id="04411-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="04411-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04411-112">PARAMETERS</span></span>

### <span data-ttu-id="04411-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04411-113">-DefaultProfile</span></span>
<span data-ttu-id="04411-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04411-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04411-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04411-115">-Description</span></span>
<span data-ttu-id="04411-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="04411-116">The reason of action.</span></span>

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

### <span data-ttu-id="04411-117">-Name</span><span class="sxs-lookup"><span data-stu-id="04411-117">-Name</span></span>
<span data-ttu-id="04411-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="04411-118">The resource name.</span></span>

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

### <span data-ttu-id="04411-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="04411-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="04411-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="04411-120">The private link resource type.</span></span>

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

### <span data-ttu-id="04411-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04411-121">-ResourceGroupName</span></span>
<span data-ttu-id="04411-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04411-122">The resource group name.</span></span>

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

### <span data-ttu-id="04411-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04411-123">-ResourceId</span></span>
<span data-ttu-id="04411-124">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="04411-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="04411-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="04411-125">-ServiceName</span></span>
<span data-ttu-id="04411-126">Der Name des Diensts, zu dem die private Endpunktverbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="04411-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="04411-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04411-127">CommonParameters</span></span>
<span data-ttu-id="04411-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04411-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04411-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04411-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04411-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04411-130">INPUTS</span></span>

### <span data-ttu-id="04411-131">System.String</span><span class="sxs-lookup"><span data-stu-id="04411-131">System.String</span></span>

## <span data-ttu-id="04411-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04411-132">OUTPUTS</span></span>

### <span data-ttu-id="04411-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04411-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="04411-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="04411-134">NOTES</span></span>

## <span data-ttu-id="04411-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="04411-135">RELATED LINKS</span></span>

[<span data-ttu-id="04411-136">Genehmigen-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04411-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="04411-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04411-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="04411-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04411-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="04411-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04411-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)