---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 38a8083b96915ad40aafcb4437b88d9266cae1bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660768"
---
# <span data-ttu-id="72c72-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72c72-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="72c72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72c72-102">SYNOPSIS</span></span>
<span data-ttu-id="72c72-103">Ruft ein Lastenausgleichsmodul ab.</span><span class="sxs-lookup"><span data-stu-id="72c72-103">Gets a load balancer.</span></span>

## <span data-ttu-id="72c72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72c72-104">SYNTAX</span></span>

### <span data-ttu-id="72c72-105">NOEXPAND (Standard)</span><span class="sxs-lookup"><span data-stu-id="72c72-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72c72-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="72c72-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72c72-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72c72-107">DESCRIPTION</span></span>
<span data-ttu-id="72c72-108">Das Cmdlet " **Get-AzLoadBalancer** " Ruft einen oder mehrere Azure-Lastenausgleichs Elemente ab, die in einer Ressourcengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="72c72-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="72c72-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72c72-109">EXAMPLES</span></span>

### <span data-ttu-id="72c72-110">Beispiel 1: Abrufen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="72c72-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="72c72-111">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab.</span><span class="sxs-lookup"><span data-stu-id="72c72-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="72c72-112">Bevor Sie dieses Cmdlet ausführen können, muss ein Lastenausgleichsmodul vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="72c72-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="72c72-113">Beispiel 2: Auflisten von Lastenausgleichsfunktionen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="72c72-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="72c72-114">Dieser Befehl ruft alle Load-Salden mit einem Namen ab, der mit "MyLoadBalancer" beginnt.</span><span class="sxs-lookup"><span data-stu-id="72c72-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="72c72-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="72c72-115">PARAMETERS</span></span>

### <span data-ttu-id="72c72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c72-116">-DefaultProfile</span></span>
<span data-ttu-id="72c72-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72c72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c72-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="72c72-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c72-119">-Name</span><span class="sxs-lookup"><span data-stu-id="72c72-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="72c72-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c72-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="72c72-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c72-121">CommonParameters</span></span>
<span data-ttu-id="72c72-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c72-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c72-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72c72-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c72-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72c72-124">INPUTS</span></span>

### <span data-ttu-id="72c72-125">System. String</span><span class="sxs-lookup"><span data-stu-id="72c72-125">System.String</span></span>

## <span data-ttu-id="72c72-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72c72-126">OUTPUTS</span></span>

### <span data-ttu-id="72c72-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72c72-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="72c72-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="72c72-128">NOTES</span></span>

## <span data-ttu-id="72c72-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72c72-129">RELATED LINKS</span></span>

[<span data-ttu-id="72c72-130">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72c72-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="72c72-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72c72-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="72c72-132">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72c72-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


