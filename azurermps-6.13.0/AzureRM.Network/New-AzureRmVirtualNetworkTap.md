---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: d40d9c378afdbbc9380114a7b5998b173cb4652f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664818"
---
# <span data-ttu-id="bc548-101">New-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bc548-101">New-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="bc548-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc548-102">SYNOPSIS</span></span>
<span data-ttu-id="bc548-103">Erstellt eine VirtualNetworkTap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc548-103">Creates a VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc548-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc548-104">SYNTAX</span></span>

### <span data-ttu-id="bc548-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc548-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc548-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc548-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc548-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc548-107">DESCRIPTION</span></span>
<span data-ttu-id="bc548-108">Das Cmdlet **New-AzureRmVirtualNetworkTap** erstellt eine Azure Virtual Network Tap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc548-108">The **New-AzureRmVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="bc548-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc548-109">EXAMPLES</span></span>

### <span data-ttu-id="bc548-110">Beispiel 1: Erstellen eines virtuellen Azure-Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="bc548-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="bc548-111">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das über die Konfigurationsdetails des Ziels VM verfügt (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="bc548-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="bc548-112">Der gesamte von der Quelle konfigurierte Zugriff auf den Datenverkehr wird an diesen Ziel-IP +-Port weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc548-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="bc548-113">Beispiel 2: Erstellen eines virtuellen Azure-Netzwerks Tippen Sie mit LoadBalancer IP</span><span class="sxs-lookup"><span data-stu-id="bc548-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="bc548-114">Mit diesem Befehl wird ein virtuelles Netzwerk mit dem Namen "VirtualNetworkTap1" erstellt, das über die Ziel-VM-Konfigurationsdetails (FrontEndIpConfiguration) verfügt.</span><span class="sxs-lookup"><span data-stu-id="bc548-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="bc548-115">Der gesamte von der Quelle konfigurierte Tap-Datenverkehr wird an diesen LoadBalancer-IPKonfigurationsdateiAddress weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc548-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="bc548-116">Der Standard Zielport ist 4789.</span><span class="sxs-lookup"><span data-stu-id="bc548-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="bc548-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc548-117">PARAMETERS</span></span>

### <span data-ttu-id="bc548-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc548-118">-AsJob</span></span>
<span data-ttu-id="bc548-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bc548-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc548-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc548-120">-DefaultProfile</span></span>
<span data-ttu-id="bc548-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc548-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc548-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc548-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="bc548-123">Der Verweis auf die IP-Konfigurationsressource des Ziel-Load Balancer-Front-End.</span><span class="sxs-lookup"><span data-stu-id="bc548-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="bc548-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bc548-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="bc548-125">Der Verweis auf die IP-Konfigurationsressource des Ziel-Load Balancer-Front-End.</span><span class="sxs-lookup"><span data-stu-id="bc548-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="bc548-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc548-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="bc548-127">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerk Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bc548-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="bc548-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bc548-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="bc548-129">Der Verweis auf die IP-Konfigurationsressource der Zielnetzwerk Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bc548-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="bc548-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="bc548-130">-DestinationPort</span></span>
<span data-ttu-id="bc548-131">Der Ziel-Port des Paket Sammlers</span><span class="sxs-lookup"><span data-stu-id="bc548-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="bc548-132">-Force</span><span class="sxs-lookup"><span data-stu-id="bc548-132">-Force</span></span>
<span data-ttu-id="bc548-133">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="bc548-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bc548-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="bc548-134">-Location</span></span>
<span data-ttu-id="bc548-135">Die Position.</span><span class="sxs-lookup"><span data-stu-id="bc548-135">The location.</span></span>

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

### <span data-ttu-id="bc548-136">-Name</span><span class="sxs-lookup"><span data-stu-id="bc548-136">-Name</span></span>
<span data-ttu-id="bc548-137">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="bc548-137">The name of the tap.</span></span>

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

### <span data-ttu-id="bc548-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc548-138">-ResourceGroupName</span></span>
<span data-ttu-id="bc548-139">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="bc548-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="bc548-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc548-140">-Tag</span></span>
<span data-ttu-id="bc548-141">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc548-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bc548-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc548-142">-Confirm</span></span>
<span data-ttu-id="bc548-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc548-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc548-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc548-144">-WhatIf</span></span>
<span data-ttu-id="bc548-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc548-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc548-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc548-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc548-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc548-147">CommonParameters</span></span>
<span data-ttu-id="bc548-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc548-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc548-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc548-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc548-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc548-150">INPUTS</span></span>

### <span data-ttu-id="bc548-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bc548-151">System.String</span></span>

### <span data-ttu-id="bc548-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bc548-152">System.Int32</span></span>

### <span data-ttu-id="bc548-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc548-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc548-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc548-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="bc548-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc548-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="bc548-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc548-156">OUTPUTS</span></span>

### <span data-ttu-id="bc548-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bc548-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="bc548-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc548-158">NOTES</span></span>

## <span data-ttu-id="bc548-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc548-159">RELATED LINKS</span></span>
