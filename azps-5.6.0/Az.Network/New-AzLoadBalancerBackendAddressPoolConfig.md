---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920512"
---
# <span data-ttu-id="a3fb6-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3fb6-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a3fb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fb6-103">Erstellt eine Back-End-Adresspoolkonfiguration für einen Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="a3fb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3fb6-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3fb6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="a3fb6-106">Das **Cmdlet New-AzLoadBalancerBackendAddressPoolConfig** erstellt eine Back-End-Adresspoolkonfiguration für einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a3fb6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fb6-108">Beispiel 1: Erstellen einer Back-End-Adresspoolkonfiguration für einen Load Balancer</span><span class="sxs-lookup"><span data-stu-id="a3fb6-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="a3fb6-109">Mit diesem Befehl wird eine Back-End-Adresspoolkonfiguration namens Back-EndAddressPool02 für einen Load Balancer erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="a3fb6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="a3fb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fb6-111">-DefaultProfile</span></span>
<span data-ttu-id="a3fb6-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3fb6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a3fb6-113">-Name</span></span>
<span data-ttu-id="a3fb6-114">Gibt den Namen der zu erstellenden Konfiguration des Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fb6-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3fb6-115">-Confirm</span></span>
<span data-ttu-id="a3fb6-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3fb6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3fb6-117">-WhatIf</span></span>
<span data-ttu-id="a3fb6-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3fb6-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3fb6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fb6-120">CommonParameters</span></span>
<span data-ttu-id="a3fb6-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fb6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fb6-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fb6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fb6-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3fb6-123">INPUTS</span></span>

### <span data-ttu-id="a3fb6-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a3fb6-124">None</span></span>

## <span data-ttu-id="a3fb6-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3fb6-125">OUTPUTS</span></span>

### <span data-ttu-id="a3fb6-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a3fb6-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a3fb6-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3fb6-127">NOTES</span></span>

## <span data-ttu-id="a3fb6-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3fb6-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3fb6-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3fb6-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a3fb6-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3fb6-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a3fb6-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a3fb6-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


