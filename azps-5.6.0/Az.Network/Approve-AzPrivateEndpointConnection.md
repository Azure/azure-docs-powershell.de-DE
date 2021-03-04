---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932435"
---
# <span data-ttu-id="cdc37-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cdc37-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="cdc37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc37-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc37-103">Genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="cdc37-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="cdc37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdc37-104">SYNTAX</span></span>

### <span data-ttu-id="cdc37-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdc37-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc37-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="cdc37-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdc37-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc37-108">Das **Cmdlet Approve-AzPrivateEndpointConnection** genehmigt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="cdc37-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="cdc37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cdc37-109">EXAMPLES</span></span>

### <span data-ttu-id="cdc37-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdc37-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="cdc37-111">In diesem Beispiel wird eine private Endpunktverbindung genehmigt.</span><span class="sxs-lookup"><span data-stu-id="cdc37-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="cdc37-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cdc37-112">PARAMETERS</span></span>

### <span data-ttu-id="cdc37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc37-113">-DefaultProfile</span></span>
<span data-ttu-id="cdc37-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdc37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc37-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdc37-115">-Description</span></span>
<span data-ttu-id="cdc37-116">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="cdc37-116">The reason of action.</span></span>

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

### <span data-ttu-id="cdc37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cdc37-117">-Name</span></span>
<span data-ttu-id="cdc37-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cdc37-118">The resource name.</span></span>

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

### <span data-ttu-id="cdc37-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="cdc37-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="cdc37-120">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="cdc37-120">The private link resource type.</span></span>

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

### <span data-ttu-id="cdc37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc37-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdc37-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cdc37-122">The resource group name.</span></span>

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

### <span data-ttu-id="cdc37-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdc37-123">-ResourceId</span></span>
<span data-ttu-id="cdc37-124">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="cdc37-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="cdc37-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cdc37-125">-ServiceName</span></span>
<span data-ttu-id="cdc37-126">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="cdc37-126">The private link service name.</span></span>

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


### <span data-ttu-id="cdc37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc37-127">CommonParameters</span></span>
<span data-ttu-id="cdc37-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc37-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdc37-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc37-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cdc37-130">INPUTS</span></span>

### <span data-ttu-id="cdc37-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc37-131">System.String</span></span>

## <span data-ttu-id="cdc37-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cdc37-132">OUTPUTS</span></span>

### <span data-ttu-id="cdc37-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cdc37-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="cdc37-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cdc37-134">NOTES</span></span>

## <span data-ttu-id="cdc37-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cdc37-135">RELATED LINKS</span></span>

[<span data-ttu-id="cdc37-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cdc37-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="cdc37-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cdc37-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="cdc37-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cdc37-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="cdc37-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cdc37-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)