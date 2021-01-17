---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473468"
---
# <span data-ttu-id="da7b7-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da7b7-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="da7b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="da7b7-103">Erstellt eine Front-End-IP-Konfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="da7b7-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="da7b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da7b7-104">SYNTAX</span></span>

### <span data-ttu-id="da7b7-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="da7b7-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7b7-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="da7b7-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7b7-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7b7-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7b7-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="da7b7-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7b7-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="da7b7-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7b7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da7b7-111">DESCRIPTION</span></span>
<span data-ttu-id="da7b7-112">Das **Cmdlet "New-AzLoadBalancerFrontendIpConfig"** erstellt eine Front-End-IP-Konfiguration für einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="da7b7-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="da7b7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da7b7-113">EXAMPLES</span></span>

### <span data-ttu-id="da7b7-114">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="da7b7-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="da7b7-115">Der erste Befehl erstellt eine dynamische öffentliche IP-Adresse namens "MyPublicIP" in der Ressourcengruppe namens "MyResourceGroup" und speichert sie dann in der $publicip Variable.</span><span class="sxs-lookup"><span data-stu-id="da7b7-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="da7b7-116">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration namens FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip.</span><span class="sxs-lookup"><span data-stu-id="da7b7-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="da7b7-117">Beispiel 2: Erstellen einer Front-End-IP-Konfiguration für einen Lastenausgleich mit dem IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="da7b7-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="da7b7-118">Der erste Befehl erstellt ein öffentliches ip-Präfix namens "MyPublicIP" mit der Länge 28 in der Ressourcengruppe namens "MyResourceGroup" und speichert es dann in der $publicipprefix Variable.</span><span class="sxs-lookup"><span data-stu-id="da7b7-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="da7b7-119">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration namens FrontendIpConfig01 mit dem öffentlichen IP-Präfix in $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="da7b7-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="da7b7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da7b7-120">PARAMETERS</span></span>

### <span data-ttu-id="da7b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7b7-121">-DefaultProfile</span></span>
<span data-ttu-id="da7b7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da7b7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da7b7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="da7b7-123">-Name</span></span>
<span data-ttu-id="da7b7-124">Gibt die Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="da7b7-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da7b7-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-125">-PrivateIpAddress</span></span>
<span data-ttu-id="da7b7-126">Gibt die private IP-Adresse des Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="da7b7-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="da7b7-127">Geben Sie diesen Parameter nur an, wenn Sie auch den Parameter *"Subnet"* angeben.</span><span class="sxs-lookup"><span data-stu-id="da7b7-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="da7b7-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="da7b7-129">Die private IP-Adressversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="da7b7-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-130">-PublicIpAddress</span></span>
<span data-ttu-id="da7b7-131">Gibt das **PublicIpAddress-Objekt** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="da7b7-132">-PublicIpAddressId</span></span>
<span data-ttu-id="da7b7-133">Gibt die ID des **PublicIpAddress-Objekts** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="da7b7-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="da7b7-135">Gibt das **PublicIpAddressPrefix-Objekt** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="da7b7-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="da7b7-137">Gibt die ID des **PublicIpAddressPrefix-Objekts** an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="da7b7-138">-Subnet</span></span>
<span data-ttu-id="da7b7-139">Gibt das **Subnetzobjekt** an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="da7b7-140">-SubnetId</span></span>
<span data-ttu-id="da7b7-141">Gibt die ID des Subnetzes an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da7b7-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="da7b7-142">-Zone</span></span>
<span data-ttu-id="da7b7-143">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="da7b7-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7b7-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da7b7-144">-Confirm</span></span>
<span data-ttu-id="da7b7-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da7b7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7b7-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da7b7-146">-WhatIf</span></span>
<span data-ttu-id="da7b7-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da7b7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da7b7-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da7b7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7b7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7b7-149">CommonParameters</span></span>
<span data-ttu-id="da7b7-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7b7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7b7-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da7b7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7b7-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da7b7-152">INPUTS</span></span>

### <span data-ttu-id="da7b7-153">System.String</span><span class="sxs-lookup"><span data-stu-id="da7b7-153">System.String</span></span>

### <span data-ttu-id="da7b7-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="da7b7-154">System.String[]</span></span>

### <span data-ttu-id="da7b7-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="da7b7-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="da7b7-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="da7b7-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da7b7-157">OUTPUTS</span></span>

### <span data-ttu-id="da7b7-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="da7b7-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="da7b7-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da7b7-159">NOTES</span></span>

## <span data-ttu-id="da7b7-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da7b7-160">RELATED LINKS</span></span>

[<span data-ttu-id="da7b7-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da7b7-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da7b7-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da7b7-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da7b7-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="da7b7-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="da7b7-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da7b7-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da7b7-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da7b7-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


