---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364061"
---
# <span data-ttu-id="c2628-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c2628-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c2628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2628-102">SYNOPSIS</span></span>
<span data-ttu-id="c2628-103">Ruft eine Ressource für die Verbindung mit einem privaten Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="c2628-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="c2628-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2628-104">SYNTAX</span></span>

### <span data-ttu-id="c2628-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2628-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2628-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c2628-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2628-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="c2628-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2628-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2628-108">DESCRIPTION</span></span>
<span data-ttu-id="c2628-109">Das **Cmdlet "Get-AzPrivateEndpointConnection"** ruft eine Verbindungsressource für einen privaten Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="c2628-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="c2628-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2628-110">EXAMPLES</span></span>

### <span data-ttu-id="c2628-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2628-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="c2628-112">Dieses Beispiel gibt eine Liste aller privaten Endpunktverbindungen zurück, die zu einem SQL Server mit dem Namen Mysql gehören.</span><span class="sxs-lookup"><span data-stu-id="c2628-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="c2628-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2628-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="c2628-114">In diesem Beispiel wird eine private Endpunktverbindung namens "MyPrivateEndpointConnection1" zu einem privaten Verknüpfungsdienst namens "MyPrivateLinkService" erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2628-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="c2628-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2628-115">PARAMETERS</span></span>

### <span data-ttu-id="c2628-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2628-116">-DefaultProfile</span></span>
<span data-ttu-id="c2628-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2628-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2628-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2628-118">-Description</span></span>
<span data-ttu-id="c2628-119">Der Grund der Aktion.</span><span class="sxs-lookup"><span data-stu-id="c2628-119">The reason of action.</span></span>

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

### <span data-ttu-id="c2628-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c2628-120">-Name</span></span>
<span data-ttu-id="c2628-121">Der Name der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c2628-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c2628-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c2628-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="c2628-123">Die Azure-Ressourcen-Manager-ID der privaten Verknüpfungsressource, zu der die private Endpunktverbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="c2628-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="c2628-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="c2628-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="c2628-125">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="c2628-125">The private link resource type.</span></span>

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

### <span data-ttu-id="c2628-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2628-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2628-127">Der Ressourcengruppenname der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c2628-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c2628-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2628-128">-ResourceId</span></span>
<span data-ttu-id="c2628-129">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="c2628-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c2628-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c2628-130">-ServiceName</span></span>
<span data-ttu-id="c2628-131">Der Name des Diensts, dem die private Endpunktverbindung angehört.</span><span class="sxs-lookup"><span data-stu-id="c2628-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="c2628-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2628-132">CommonParameters</span></span>
<span data-ttu-id="c2628-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2628-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2628-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2628-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2628-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2628-135">INPUTS</span></span>

### <span data-ttu-id="c2628-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c2628-136">System.String</span></span>

## <span data-ttu-id="c2628-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2628-137">OUTPUTS</span></span>

### <span data-ttu-id="c2628-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c2628-138">System.Boolean</span></span>

## <span data-ttu-id="c2628-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2628-139">NOTES</span></span>

## <span data-ttu-id="c2628-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2628-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2628-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c2628-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c2628-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c2628-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c2628-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c2628-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c2628-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c2628-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
