---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458884"
---
# <span data-ttu-id="d0ad6-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d0ad6-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="d0ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ad6-103">verweigert eine Verbindung mit einem privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="d0ad6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0ad6-104">SYNTAX</span></span>

### <span data-ttu-id="d0ad6-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0ad6-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ad6-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="d0ad6-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ad6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ad6-108">Das **Cmdlet "Deny-AzPrivateEndpointConnection"** verweigert eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="d0ad6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0ad6-109">EXAMPLES</span></span>

### <span data-ttu-id="d0ad6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0ad6-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="d0ad6-111">In diesem Beispiel wird eine Verbindung mit einem privaten Endpunkt verweigert.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="d0ad6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="d0ad6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ad6-113">-DefaultProfile</span></span>
<span data-ttu-id="d0ad6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ad6-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0ad6-115">-Description</span></span>
<span data-ttu-id="d0ad6-116">Der Grund der Aktion.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-116">The reason of action.</span></span>

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

### <span data-ttu-id="d0ad6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0ad6-117">-Name</span></span>
<span data-ttu-id="d0ad6-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-118">The resource name.</span></span>

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

### <span data-ttu-id="d0ad6-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="d0ad6-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="d0ad6-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-120">The private link resource type.</span></span>

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

### <span data-ttu-id="d0ad6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ad6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0ad6-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-122">The resource group name.</span></span>

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

### <span data-ttu-id="d0ad6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0ad6-123">-ResourceId</span></span>
<span data-ttu-id="d0ad6-124">Die Azure-Ressourcen-Manager-ID der Privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="d0ad6-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d0ad6-125">-ServiceName</span></span>
<span data-ttu-id="d0ad6-126">Der Name des Diensts, zu dem die private Endpunktverbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="d0ad6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ad6-127">CommonParameters</span></span>
<span data-ttu-id="d0ad6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ad6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ad6-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0ad6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ad6-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0ad6-130">INPUTS</span></span>

### <span data-ttu-id="d0ad6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d0ad6-131">System.String</span></span>

## <span data-ttu-id="d0ad6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0ad6-132">OUTPUTS</span></span>

### <span data-ttu-id="d0ad6-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d0ad6-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d0ad6-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0ad6-134">NOTES</span></span>

## <span data-ttu-id="d0ad6-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0ad6-135">RELATED LINKS</span></span>

[<span data-ttu-id="d0ad6-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d0ad6-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d0ad6-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d0ad6-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d0ad6-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d0ad6-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d0ad6-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d0ad6-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)