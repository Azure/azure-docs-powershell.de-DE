---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175039"
---
# <span data-ttu-id="70860-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="70860-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="70860-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70860-102">SYNOPSIS</span></span>
<span data-ttu-id="70860-103">Gibt ein Load Balancer-Back-End-Adress config zurück.</span><span class="sxs-lookup"><span data-stu-id="70860-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="70860-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70860-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70860-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70860-105">DESCRIPTION</span></span>
<span data-ttu-id="70860-106">Gibt ein Load Balancer-Back-End-Adress config zurück.</span><span class="sxs-lookup"><span data-stu-id="70860-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="70860-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70860-107">EXAMPLES</span></span>

### <span data-ttu-id="70860-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70860-108">Example 1</span></span>
### <span data-ttu-id="70860-109">Beispiel 2: neue LoadBalancer-Adresskonfiguration mit virtueller Netzwerk Referenz</span><span class="sxs-lookup"><span data-stu-id="70860-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="70860-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70860-110">PARAMETERS</span></span>

### <span data-ttu-id="70860-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70860-111">-DefaultProfile</span></span>
<span data-ttu-id="70860-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70860-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70860-113">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="70860-113">-IpAddress</span></span>
<span data-ttu-id="70860-114">Die IPAddress, die dem Back-End-Pool hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="70860-114">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="70860-115">-Name</span><span class="sxs-lookup"><span data-stu-id="70860-115">-Name</span></span>
<span data-ttu-id="70860-116">Der Name der Back-End-Adresskonfiguration</span><span class="sxs-lookup"><span data-stu-id="70860-116">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="70860-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="70860-117">-VirtualNetworkId</span></span>
<span data-ttu-id="70860-118">Das virtuelle Netzwerk, das der Konfiguration des Back-End-Adressen zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="70860-118">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="70860-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70860-119">-Confirm</span></span>
<span data-ttu-id="70860-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70860-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70860-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70860-121">-WhatIf</span></span>
<span data-ttu-id="70860-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70860-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70860-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70860-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70860-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70860-124">CommonParameters</span></span>
<span data-ttu-id="70860-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70860-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70860-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70860-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70860-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70860-127">INPUTS</span></span>

### <span data-ttu-id="70860-128">System. String</span><span class="sxs-lookup"><span data-stu-id="70860-128">System.String</span></span>

### <span data-ttu-id="70860-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70860-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="70860-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70860-130">OUTPUTS</span></span>

### <span data-ttu-id="70860-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="70860-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="70860-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="70860-132">NOTES</span></span>

## <span data-ttu-id="70860-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70860-133">RELATED LINKS</span></span>
