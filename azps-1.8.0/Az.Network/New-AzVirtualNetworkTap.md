---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 11939edc15d49614d2a1fd1692825cd07cd82b2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660460"
---
# <span data-ttu-id="6032a-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6032a-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="6032a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6032a-102">SYNOPSIS</span></span>
<span data-ttu-id="6032a-103">Erstellt eine VirtualNetworkTap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6032a-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="6032a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6032a-104">SYNTAX</span></span>

### <span data-ttu-id="6032a-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="6032a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6032a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6032a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6032a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6032a-107">DESCRIPTION</span></span>
<span data-ttu-id="6032a-108">Das Cmdlet **New-AzVirtualNetworkTap** erstellt eine Azure Virtual Network Tap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6032a-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="6032a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6032a-109">EXAMPLES</span></span>

### <span data-ttu-id="6032a-110">Beispiel 1: Erstellen eines virtuellen Azure-Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="6032a-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="6032a-111">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das über die Konfigurationsdetails des Ziels VM verfügt (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="6032a-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="6032a-112">Der gesamte von der Quelle konfigurierte Zugriff auf den Datenverkehr wird an diesen Ziel-IP +-Port weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6032a-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="6032a-113">Beispiel 2: Erstellen eines virtuellen Azure-Netzwerks Tippen Sie mit LoadBalancer IP</span><span class="sxs-lookup"><span data-stu-id="6032a-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="6032a-114">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das über die Ziel-VM-Konfigurationsdetails (FrontEndIpConfiguration) verfügt.</span><span class="sxs-lookup"><span data-stu-id="6032a-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="6032a-115">Der gesamte von der Quelle konfigurierte Tap-Datenverkehr wird an diesen LoadBalancer-IPKonfigurationsdateiAddress weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6032a-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="6032a-116">Der Standard Zielport ist 4789.</span><span class="sxs-lookup"><span data-stu-id="6032a-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="6032a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6032a-117">PARAMETERS</span></span>

### <span data-ttu-id="6032a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6032a-118">-AsJob</span></span>
<span data-ttu-id="6032a-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6032a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6032a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6032a-120">-DefaultProfile</span></span>
<span data-ttu-id="6032a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6032a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6032a-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6032a-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="6032a-123">Der Verweis auf die IP-Konfigurationsressource des Ziel-Load Balancer-Front-End.</span><span class="sxs-lookup"><span data-stu-id="6032a-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="6032a-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6032a-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="6032a-125">Der Verweis auf die IP-Konfigurationsressource des Ziel-Load Balancer-Front-End.</span><span class="sxs-lookup"><span data-stu-id="6032a-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="6032a-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6032a-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="6032a-127">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerk Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6032a-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="6032a-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6032a-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="6032a-129">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerk Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6032a-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="6032a-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6032a-130">-DestinationPort</span></span>
<span data-ttu-id="6032a-131">Der Ziel-Port des Paket Sammlers</span><span class="sxs-lookup"><span data-stu-id="6032a-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="6032a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="6032a-132">-Force</span></span>
<span data-ttu-id="6032a-133">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="6032a-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6032a-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="6032a-134">-Location</span></span>
<span data-ttu-id="6032a-135">Die Position.</span><span class="sxs-lookup"><span data-stu-id="6032a-135">The location.</span></span>

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

### <span data-ttu-id="6032a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="6032a-136">-Name</span></span>
<span data-ttu-id="6032a-137">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="6032a-137">The name of the tap.</span></span>

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

### <span data-ttu-id="6032a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6032a-138">-ResourceGroupName</span></span>
<span data-ttu-id="6032a-139">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="6032a-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="6032a-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="6032a-140">-Tag</span></span>
<span data-ttu-id="6032a-141">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="6032a-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6032a-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6032a-142">-Confirm</span></span>
<span data-ttu-id="6032a-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6032a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6032a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6032a-144">-WhatIf</span></span>
<span data-ttu-id="6032a-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6032a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6032a-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6032a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6032a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6032a-147">CommonParameters</span></span>
<span data-ttu-id="6032a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6032a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6032a-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6032a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6032a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6032a-150">INPUTS</span></span>

### <span data-ttu-id="6032a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6032a-151">System.String</span></span>

### <span data-ttu-id="6032a-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6032a-152">System.Int32</span></span>

### <span data-ttu-id="6032a-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6032a-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6032a-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6032a-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="6032a-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6032a-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="6032a-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6032a-156">OUTPUTS</span></span>

### <span data-ttu-id="6032a-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6032a-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="6032a-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="6032a-158">NOTES</span></span>

## <span data-ttu-id="6032a-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6032a-159">RELATED LINKS</span></span>

[<span data-ttu-id="6032a-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6032a-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="6032a-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6032a-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="6032a-162">Satz-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6032a-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
