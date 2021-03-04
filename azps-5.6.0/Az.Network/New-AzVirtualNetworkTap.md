---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 93bc2a622d2bba077b5176c67df4d7894a95d4ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931744"
---
# <span data-ttu-id="aaad7-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aaad7-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="aaad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaad7-102">SYNOPSIS</span></span>
<span data-ttu-id="aaad7-103">Erstellt eine VirtualNetworkTap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="aaad7-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="aaad7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aaad7-104">SYNTAX</span></span>

### <span data-ttu-id="aaad7-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="aaad7-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaad7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaad7-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaad7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aaad7-107">DESCRIPTION</span></span>
<span data-ttu-id="aaad7-108">Das **Cmdlet New-AzVirtualNetworkTap** erstellt eine Azure Virtual Network Tap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="aaad7-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="aaad7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aaad7-109">EXAMPLES</span></span>

### <span data-ttu-id="aaad7-110">Beispiel 1: Erstellen eines virtuellen Azure-Netzwerks</span><span class="sxs-lookup"><span data-stu-id="aaad7-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="aaad7-111">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das die Konfigurationsdetails der Ziel-VM enthält (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="aaad7-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="aaad7-112">Der datenverkehr des konfigurierten virtuellen Computers wird an diese Ziel-IP+ Port geroutet.</span><span class="sxs-lookup"><span data-stu-id="aaad7-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="aaad7-113">Beispiel 2: Erstellen eines Azure Virtual Network Tap mit LoadBalancer IP</span><span class="sxs-lookup"><span data-stu-id="aaad7-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="aaad7-114">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das die Konfigurationsdetails der Ziel-VM enthält (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="aaad7-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="aaad7-115">Der datenverkehr des konfigurierten virtuellen Computers wird an diese LoadBalancer-IpConfiguration geroutet.</span><span class="sxs-lookup"><span data-stu-id="aaad7-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="aaad7-116">Der Standardzielport ist 4789.</span><span class="sxs-lookup"><span data-stu-id="aaad7-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="aaad7-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aaad7-117">PARAMETERS</span></span>

### <span data-ttu-id="aaad7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaad7-118">-AsJob</span></span>
<span data-ttu-id="aaad7-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aaad7-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaad7-120">-DefaultProfile</span></span>
<span data-ttu-id="aaad7-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aaad7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaad7-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaad7-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="aaad7-123">Der Verweis auf die Front-End-IP-Konfigurationsressource des Zielladeausgleichs.</span><span class="sxs-lookup"><span data-stu-id="aaad7-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="aaad7-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="aaad7-125">Der Verweis auf die Front-End-IP-Konfigurationsressource des Zielladeausgleichs.</span><span class="sxs-lookup"><span data-stu-id="aaad7-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaad7-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="aaad7-127">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aaad7-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="aaad7-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="aaad7-129">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aaad7-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="aaad7-130">-DestinationPort</span></span>
<span data-ttu-id="aaad7-131">Der Zielport des Paketsammlers</span><span class="sxs-lookup"><span data-stu-id="aaad7-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-132">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="aaad7-132">-Force</span></span>
<span data-ttu-id="aaad7-133">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="aaad7-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-134">-Location</span><span class="sxs-lookup"><span data-stu-id="aaad7-134">-Location</span></span>
<span data-ttu-id="aaad7-135">Der Speicherort.</span><span class="sxs-lookup"><span data-stu-id="aaad7-135">The location.</span></span>

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

### <span data-ttu-id="aaad7-136">-Name</span><span class="sxs-lookup"><span data-stu-id="aaad7-136">-Name</span></span>
<span data-ttu-id="aaad7-137">Der Name des Tippens.</span><span class="sxs-lookup"><span data-stu-id="aaad7-137">The name of the tap.</span></span>

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

### <span data-ttu-id="aaad7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaad7-138">-ResourceGroupName</span></span>
<span data-ttu-id="aaad7-139">Der Ressourcengruppenname des virtuellen Netzwerks tippen.</span><span class="sxs-lookup"><span data-stu-id="aaad7-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="aaad7-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaad7-140">-Tag</span></span>
<span data-ttu-id="aaad7-141">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="aaad7-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaad7-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aaad7-142">-Confirm</span></span>
<span data-ttu-id="aaad7-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aaad7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaad7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaad7-144">-WhatIf</span></span>
<span data-ttu-id="aaad7-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aaad7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaad7-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaad7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaad7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaad7-147">CommonParameters</span></span>
<span data-ttu-id="aaad7-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaad7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaad7-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaad7-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaad7-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aaad7-150">INPUTS</span></span>

### <span data-ttu-id="aaad7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="aaad7-151">System.String</span></span>

### <span data-ttu-id="aaad7-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aaad7-152">System.Int32</span></span>

### <span data-ttu-id="aaad7-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aaad7-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aaad7-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaad7-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="aaad7-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaad7-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="aaad7-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aaad7-156">OUTPUTS</span></span>

### <span data-ttu-id="aaad7-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aaad7-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="aaad7-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aaad7-158">NOTES</span></span>

## <span data-ttu-id="aaad7-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aaad7-159">RELATED LINKS</span></span>

[<span data-ttu-id="aaad7-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aaad7-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="aaad7-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aaad7-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="aaad7-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aaad7-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
