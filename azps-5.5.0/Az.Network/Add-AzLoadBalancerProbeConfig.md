---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170070"
---
# <span data-ttu-id="f67a2-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f67a2-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f67a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f67a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f67a2-103">Fügt eine Sondenkonfiguration zu einem Lastenausgleich hinzu.</span><span class="sxs-lookup"><span data-stu-id="f67a2-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="f67a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f67a2-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f67a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f67a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f67a2-106">Das **Cmdlet "Add-AzLoadBalancerProbeConfig"** fügt einem Azure Load Balancer eine Beispielkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f67a2-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f67a2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f67a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f67a2-108">Beispiel 1: Hinzufügen einer Probekonfiguration zu einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="f67a2-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="f67a2-109">Dieser Befehl ruft den Lastenausgleich namens "myLb" ab, fügt ihm die angegebene Sondenkonfiguration hinzu und aktualisiert dann den Lastenausgleich mit dem **Set-AzLoadBalancer-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="f67a2-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="f67a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f67a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f67a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67a2-111">-DefaultProfile</span></span>
<span data-ttu-id="f67a2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f67a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f67a2-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f67a2-113">-IntervalInSeconds</span></span>
<span data-ttu-id="f67a2-114">Gibt das Intervall (in Sekunden) zwischen den Einzelnen Instanzen des Diensts mit Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="f67a2-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a2-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f67a2-115">-LoadBalancer</span></span>
<span data-ttu-id="f67a2-116">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f67a2-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f67a2-117">Dieses Cmdlet fügt dem Lastenausgleich, den dieser Parameter angibt, eine Beispielkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f67a2-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f67a2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f67a2-118">-Name</span></span>
<span data-ttu-id="f67a2-119">Gibt den Namen der Hinzuzufügendenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="f67a2-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="f67a2-120">-Port</span><span class="sxs-lookup"><span data-stu-id="f67a2-120">-Port</span></span>
<span data-ttu-id="f67a2-121">Gibt den Port an, an dem Sonden eine Verbindung mit einem Dienst mit Lastenausgleich herstellen sollen.</span><span class="sxs-lookup"><span data-stu-id="f67a2-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a2-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="f67a2-122">-ProbeCount</span></span>
<span data-ttu-id="f67a2-123">Gibt die Anzahl der aufeinanderfolgenden Instanzfehler für eine Instanz an, die als fehlerhaft angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="f67a2-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a2-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f67a2-124">-Protocol</span></span>
<span data-ttu-id="f67a2-125">Gibt das Protokoll an, das für die Sonde verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f67a2-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="f67a2-126">Die zulässigen Werte für diesen Parameter sind: Tcp oder Http.</span><span class="sxs-lookup"><span data-stu-id="f67a2-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="f67a2-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="f67a2-127">-RequestPath</span></span>
<span data-ttu-id="f67a2-128">Gibt den Pfad im Dienst mit Lastenausgleich an, um die Integrität zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f67a2-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="f67a2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f67a2-129">-Confirm</span></span>
<span data-ttu-id="f67a2-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f67a2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f67a2-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f67a2-131">-WhatIf</span></span>
<span data-ttu-id="f67a2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f67a2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f67a2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f67a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f67a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67a2-134">CommonParameters</span></span>
<span data-ttu-id="f67a2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67a2-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67a2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67a2-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f67a2-137">INPUTS</span></span>

### <span data-ttu-id="f67a2-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f67a2-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f67a2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f67a2-139">System.String</span></span>

### <span data-ttu-id="f67a2-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f67a2-140">System.Int32</span></span>

## <span data-ttu-id="f67a2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f67a2-141">OUTPUTS</span></span>

### <span data-ttu-id="f67a2-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f67a2-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f67a2-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f67a2-143">NOTES</span></span>

## <span data-ttu-id="f67a2-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f67a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="f67a2-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f67a2-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f67a2-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f67a2-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f67a2-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f67a2-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="f67a2-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f67a2-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="f67a2-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f67a2-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


