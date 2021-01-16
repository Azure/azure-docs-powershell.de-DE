---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300571"
---
# <span data-ttu-id="a06b3-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a06b3-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a06b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a06b3-103">Aktualisiert den Verbindungsstatus eines privaten Endpunkts für den Dienst für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="a06b3-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="a06b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a06b3-104">SYNTAX</span></span>

### <span data-ttu-id="a06b3-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a06b3-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06b3-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a06b3-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a06b3-107">DESCRIPTION</span></span>
<span data-ttu-id="a06b3-108">Das **Cmdlet Set-AzPrivateEndpointConnection** aktualisiert einen privaten Endpunktverbindungsstatus für einen privaten Verknüpfungsdienst</span><span class="sxs-lookup"><span data-stu-id="a06b3-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="a06b3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a06b3-109">EXAMPLES</span></span>

### <span data-ttu-id="a06b3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a06b3-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="a06b3-111">In diesem Beispiel wird der Verbindungsstatus eines privaten Endpunkts auf "Genehmigt" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a06b3-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="a06b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a06b3-112">PARAMETERS</span></span>

### <span data-ttu-id="a06b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06b3-113">-DefaultProfile</span></span>
<span data-ttu-id="a06b3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a06b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06b3-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a06b3-115">-Description</span></span>
<span data-ttu-id="a06b3-116">Der Grund der Aktion.</span><span class="sxs-lookup"><span data-stu-id="a06b3-116">The reason of action.</span></span>

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

### <span data-ttu-id="a06b3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a06b3-117">-Name</span></span>
<span data-ttu-id="a06b3-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a06b3-118">The resource name.</span></span>

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

### <span data-ttu-id="a06b3-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a06b3-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a06b3-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="a06b3-120">The private link resource type.</span></span>

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

### <span data-ttu-id="a06b3-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="a06b3-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="a06b3-122">Genehmigt oder abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="a06b3-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="a06b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="a06b3-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a06b3-124">The resource group name.</span></span>

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

### <span data-ttu-id="a06b3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a06b3-125">-ResourceId</span></span>
<span data-ttu-id="a06b3-126">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="a06b3-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a06b3-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a06b3-127">-ServiceName</span></span>
<span data-ttu-id="a06b3-128">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="a06b3-128">The private link service name.</span></span>

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

### <span data-ttu-id="a06b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06b3-129">CommonParameters</span></span>
<span data-ttu-id="a06b3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06b3-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a06b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06b3-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a06b3-132">INPUTS</span></span>

### <span data-ttu-id="a06b3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a06b3-133">System.String</span></span>

## <span data-ttu-id="a06b3-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a06b3-134">OUTPUTS</span></span>

### <span data-ttu-id="a06b3-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a06b3-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a06b3-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a06b3-136">NOTES</span></span>

## <span data-ttu-id="a06b3-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a06b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="a06b3-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a06b3-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a06b3-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a06b3-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a06b3-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a06b3-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a06b3-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a06b3-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)