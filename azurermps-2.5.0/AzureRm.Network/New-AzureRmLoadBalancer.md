---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 7abc575915eb65bf6c14994833bad64e6c7cd561
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849604"
---
# <span data-ttu-id="a5064-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5064-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="a5064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5064-102">SYNOPSIS</span></span>
<span data-ttu-id="a5064-103">Erstellt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="a5064-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5064-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5064-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5064-105">DESCRIPTION</span></span>
<span data-ttu-id="a5064-106">Das Cmdlet **New-AzureRmLoadBalancer** erstellt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a5064-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="a5064-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5064-107">EXAMPLES</span></span>

### <span data-ttu-id="a5064-108">Beispiel 1: Erstellen eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="a5064-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a5064-109">Zum Bereitstellen eines Load Balancer müssen Sie zunächst mehrere Objekte erstellen, und die ersten sieben Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5064-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="a5064-110">Mit dem achten Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5064-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="a5064-111">Der neunte und letzte Befehl ruft das neue Lastenausgleichsmodul ab, um sicherzustellen, dass es erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a5064-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="a5064-112">Beachten Sie, dass in diesem Beispiel nur gezeigt wird, wie ein Load Balancer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5064-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="a5064-113">Sie müssen es auch mit dem Add-AzureRmNetworkInterfaceIpConfig-Cmdlet konfigurieren, um die NICs verschiedenen virtuellen Computern zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a5064-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="a5064-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5064-114">PARAMETERS</span></span>

### <span data-ttu-id="a5064-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5064-115">-AsJob</span></span>
<span data-ttu-id="a5064-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a5064-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5064-117">-BackendAddressPool</span></span>
<span data-ttu-id="a5064-118">Gibt einen Back-End-Adresspool an, der einem Lastenausgleichsmodul zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5064-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5064-119">-DefaultProfile</span></span>
<span data-ttu-id="a5064-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5064-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a5064-121">-Force</span></span>
<span data-ttu-id="a5064-122">Gibt an, dass dieses Cmdlet ein Lastenausgleichsmodul erstellt, auch wenn bereits ein Lastenausgleichsmodul mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a5064-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5064-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a5064-124">Gibt eine Liste der Front-End-IP-Adressen an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5064-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="a5064-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a5064-126">-InboundNatRule</span></span>
<span data-ttu-id="a5064-127">Gibt eine Liste der eingehenden NAT-Regeln (Network Address Translation) an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5064-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a5064-128">-LoadBalancingRule</span></span>
<span data-ttu-id="a5064-129">Gibt eine Liste der Lastenausgleichs Regeln an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5064-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="a5064-130">-Location</span></span>
<span data-ttu-id="a5064-131">Gibt den Bereich an, in dem ein Lastenausgleichsmodul erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5064-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a5064-132">-Name</span></span>
<span data-ttu-id="a5064-133">Gibt den Namen des Load Balancer an, den dieser erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5064-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-134">-Sonde</span><span class="sxs-lookup"><span data-stu-id="a5064-134">-Probe</span></span>
<span data-ttu-id="a5064-135">Gibt eine Liste der Prüfpunkte an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a5064-135">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5064-136">-ResourceGroupName</span></span>
<span data-ttu-id="a5064-137">Gibt den Namen der Ressourcengruppe an, in der ein Lastenausgleichsmodul erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5064-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5064-138">-Sku</span></span>
<span data-ttu-id="a5064-139">Der SKU-Name des Lastenausgleichsmoduls.</span><span class="sxs-lookup"><span data-stu-id="a5064-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5064-140">-Tag</span></span>
<span data-ttu-id="a5064-141">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a5064-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5064-142">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a5064-142">For example:</span></span>

<span data-ttu-id="a5064-143">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a5064-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5064-144">-Confirm</span></span>
<span data-ttu-id="a5064-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5064-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5064-146">-WhatIf</span></span>
<span data-ttu-id="a5064-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5064-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5064-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5064-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5064-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5064-149">CommonParameters</span></span>
<span data-ttu-id="a5064-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5064-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5064-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5064-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5064-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5064-152">INPUTS</span></span>

## <span data-ttu-id="a5064-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5064-153">OUTPUTS</span></span>

### <span data-ttu-id="a5064-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5064-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a5064-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5064-155">NOTES</span></span>

## <span data-ttu-id="a5064-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5064-156">RELATED LINKS</span></span>

[<span data-ttu-id="a5064-157">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5064-157">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a5064-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5064-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a5064-159">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5064-159">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="a5064-160">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5064-160">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
