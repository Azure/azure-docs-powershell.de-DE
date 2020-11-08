---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180221"
---
# <span data-ttu-id="26986-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26986-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="26986-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26986-102">SYNOPSIS</span></span>
<span data-ttu-id="26986-103">Fügt eine Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="26986-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="26986-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26986-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26986-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26986-105">DESCRIPTION</span></span>
<span data-ttu-id="26986-106">Das Cmdlet **Add-AzLoadBalancerBackend** fügt einem Azure Load Balancer einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="26986-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="26986-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26986-107">EXAMPLES</span></span>

### <span data-ttu-id="26986-108">Beispiel 1: Hinzufügen einer Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="26986-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="26986-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab, fügt den Back-End-Adresspool mit dem Namen BackendAddressPool02 zu MyLoadBalancer hinzu und verwendet dann das Cmdlet " **Satz-AzLoadBalancer** ", um MyLoadBalancer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="26986-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="26986-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26986-110">PARAMETERS</span></span>

### <span data-ttu-id="26986-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26986-111">-DefaultProfile</span></span>
<span data-ttu-id="26986-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26986-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26986-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26986-113">-LoadBalancer</span></span>
<span data-ttu-id="26986-114">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="26986-114">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26986-115">-Name</span><span class="sxs-lookup"><span data-stu-id="26986-115">-Name</span></span>
<span data-ttu-id="26986-116">Gibt den Namen der hinzuzufügenden Konfiguration des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="26986-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="26986-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26986-117">-Confirm</span></span>
<span data-ttu-id="26986-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26986-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26986-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26986-119">-WhatIf</span></span>
<span data-ttu-id="26986-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26986-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26986-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26986-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26986-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26986-122">CommonParameters</span></span>
<span data-ttu-id="26986-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26986-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26986-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26986-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26986-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26986-125">INPUTS</span></span>

### <span data-ttu-id="26986-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26986-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26986-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26986-127">OUTPUTS</span></span>

### <span data-ttu-id="26986-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26986-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26986-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="26986-129">NOTES</span></span>

## <span data-ttu-id="26986-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26986-130">RELATED LINKS</span></span>

[<span data-ttu-id="26986-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26986-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="26986-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="26986-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="26986-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26986-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="26986-134">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26986-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="26986-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="26986-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


