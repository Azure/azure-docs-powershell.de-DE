---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: d2df4f7f5ed073d357daa1113a8e0c7477a05cce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919723"
---
# <span data-ttu-id="8f92f-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8f92f-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8f92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f92f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f92f-103">Ruft eine private Endpunktverbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="8f92f-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="8f92f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f92f-104">SYNTAX</span></span>

### <span data-ttu-id="8f92f-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f92f-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f92f-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8f92f-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f92f-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="8f92f-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f92f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f92f-108">DESCRIPTION</span></span>
<span data-ttu-id="8f92f-109">Das **Get-AzPrivateEndpointConnection-Cmdlet** ruft eine private Endpunktverbindungsressource ab.</span><span class="sxs-lookup"><span data-stu-id="8f92f-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="8f92f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f92f-110">EXAMPLES</span></span>

### <span data-ttu-id="8f92f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f92f-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="8f92f-112">In diesem Beispiel wird eine Liste aller privaten Endpunktverbindungen mit dem Namen Mysql des Sql Servers zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8f92f-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="8f92f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8f92f-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="8f92f-114">In diesem Beispiel wird eine private Endpunktverbindung namens "MyPrivateEndpointConnection1" zum privaten Linkdienst mit dem Namen "MyPrivateLinkService" erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f92f-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="8f92f-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f92f-115">PARAMETERS</span></span>

### <span data-ttu-id="8f92f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f92f-116">-DefaultProfile</span></span>
<span data-ttu-id="8f92f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f92f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f92f-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f92f-118">-Description</span></span>
<span data-ttu-id="8f92f-119">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="8f92f-119">The reason of action.</span></span>

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

### <span data-ttu-id="8f92f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f92f-120">-Name</span></span>
<span data-ttu-id="8f92f-121">Der Name der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="8f92f-121">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f92f-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8f92f-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8f92f-123">Die Azure-Ressourcen-Manager-ID der privaten Linkressource, zu der die private Endpunktverbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="8f92f-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f92f-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8f92f-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8f92f-125">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="8f92f-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f92f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f92f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f92f-127">Der Ressourcengruppenname der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="8f92f-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8f92f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f92f-128">-ResourceId</span></span>
<span data-ttu-id="8f92f-129">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="8f92f-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8f92f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f92f-130">-ServiceName</span></span>
<span data-ttu-id="8f92f-131">Der Name des Diensts, zu dem die private Endpunktverbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="8f92f-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="8f92f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f92f-132">CommonParameters</span></span>
<span data-ttu-id="8f92f-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f92f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f92f-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f92f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f92f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f92f-135">INPUTS</span></span>

### <span data-ttu-id="8f92f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8f92f-136">System.String</span></span>

## <span data-ttu-id="8f92f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f92f-137">OUTPUTS</span></span>

### <span data-ttu-id="8f92f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f92f-138">System.Boolean</span></span>

## <span data-ttu-id="8f92f-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f92f-139">NOTES</span></span>

## <span data-ttu-id="8f92f-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f92f-140">RELATED LINKS</span></span>

[<span data-ttu-id="8f92f-141">Genehmigen-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8f92f-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8f92f-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8f92f-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8f92f-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8f92f-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8f92f-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8f92f-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
