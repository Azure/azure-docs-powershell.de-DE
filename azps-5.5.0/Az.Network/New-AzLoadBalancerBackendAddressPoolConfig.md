---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172625"
---
# <span data-ttu-id="40462-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="40462-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="40462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40462-102">SYNOPSIS</span></span>
<span data-ttu-id="40462-103">Erstellt eine Back-End-Adresspoolkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="40462-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="40462-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40462-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40462-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40462-105">DESCRIPTION</span></span>
<span data-ttu-id="40462-106">Das **Cmdlet "New-AzLoadBalancerBackendAddressPoolConfig"** erstellt eine Back-End-Adresspoolkonfiguration für einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="40462-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="40462-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40462-107">EXAMPLES</span></span>

### <span data-ttu-id="40462-108">Beispiel 1: Erstellen einer Back-End-Adresspoolkonfiguration für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="40462-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="40462-109">Mit diesem Befehl wird eine Back-End-Adresspool-Konfiguration namens Back-EndAddressPool02 für einen Lastenausgleich erstellt.</span><span class="sxs-lookup"><span data-stu-id="40462-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="40462-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40462-110">PARAMETERS</span></span>

### <span data-ttu-id="40462-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40462-111">-DefaultProfile</span></span>
<span data-ttu-id="40462-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40462-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40462-113">-Name</span><span class="sxs-lookup"><span data-stu-id="40462-113">-Name</span></span>
<span data-ttu-id="40462-114">Gibt den Namen der zu erstellenden Konfiguration des Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="40462-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="40462-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40462-115">-Confirm</span></span>
<span data-ttu-id="40462-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40462-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40462-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="40462-117">-WhatIf</span></span>
<span data-ttu-id="40462-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40462-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40462-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40462-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40462-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40462-120">CommonParameters</span></span>
<span data-ttu-id="40462-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40462-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40462-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40462-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40462-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40462-123">INPUTS</span></span>

### <span data-ttu-id="40462-124">Keine</span><span class="sxs-lookup"><span data-stu-id="40462-124">None</span></span>

## <span data-ttu-id="40462-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40462-125">OUTPUTS</span></span>

### <span data-ttu-id="40462-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40462-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="40462-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40462-127">NOTES</span></span>

## <span data-ttu-id="40462-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40462-128">RELATED LINKS</span></span>

[<span data-ttu-id="40462-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="40462-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="40462-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="40462-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="40462-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="40462-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


