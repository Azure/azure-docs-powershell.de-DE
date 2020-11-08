---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: fa520056b9e1d098271cd726575e8d521d7c27f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996502"
---
# <span data-ttu-id="9954f-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9954f-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9954f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9954f-102">SYNOPSIS</span></span>
<span data-ttu-id="9954f-103">Erstellt eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="9954f-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="9954f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9954f-104">SYNTAX</span></span>

### <span data-ttu-id="9954f-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9954f-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9954f-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9954f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9954f-109">DESCRIPTION</span></span>
<span data-ttu-id="9954f-110">Das Cmdlet **New-AzLoadBalancerFrontendIpConfig** erstellt eine Front-End-IP-Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="9954f-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9954f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9954f-111">EXAMPLES</span></span>

### <span data-ttu-id="9954f-112">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="9954f-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="9954f-113">Der erste Befehl erstellt eine dynamische öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9954f-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9954f-114">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip.</span><span class="sxs-lookup"><span data-stu-id="9954f-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="9954f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9954f-115">PARAMETERS</span></span>

### <span data-ttu-id="9954f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9954f-116">-DefaultProfile</span></span>
<span data-ttu-id="9954f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9954f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9954f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9954f-118">-Name</span></span>
<span data-ttu-id="9954f-119">Gibt die Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9954f-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9954f-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-120">-PrivateIpAddress</span></span>
<span data-ttu-id="9954f-121">Gibt die private IP-Adresse des Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="9954f-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="9954f-122">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9954f-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="9954f-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9954f-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9954f-124">Die private IP-Adressenversion der IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9954f-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="9954f-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-125">-PublicIpAddress</span></span>
<span data-ttu-id="9954f-126">Gibt das **PublicIpAddress** -Objekt an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9954f-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9954f-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9954f-127">-PublicIpAddressId</span></span>
<span data-ttu-id="9954f-128">Gibt die ID des **PublicIpAddress** -Objekts an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9954f-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9954f-129">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="9954f-129">-Subnet</span></span>
<span data-ttu-id="9954f-130">Gibt das **Subnet** -Objekt an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9954f-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9954f-131">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="9954f-131">-SubnetId</span></span>
<span data-ttu-id="9954f-132">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9954f-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9954f-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="9954f-133">-Zone</span></span>
<span data-ttu-id="9954f-134">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="9954f-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9954f-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9954f-135">-Confirm</span></span>
<span data-ttu-id="9954f-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9954f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9954f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9954f-137">-WhatIf</span></span>
<span data-ttu-id="9954f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9954f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9954f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9954f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9954f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9954f-140">CommonParameters</span></span>
<span data-ttu-id="9954f-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9954f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9954f-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9954f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9954f-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9954f-143">INPUTS</span></span>

### <span data-ttu-id="9954f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9954f-144">System.String</span></span>

### <span data-ttu-id="9954f-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="9954f-145">System.String[]</span></span>

### <span data-ttu-id="9954f-146">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9954f-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="9954f-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9954f-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9954f-148">OUTPUTS</span></span>

### <span data-ttu-id="9954f-149">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9954f-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9954f-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="9954f-150">NOTES</span></span>

## <span data-ttu-id="9954f-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9954f-151">RELATED LINKS</span></span>

[<span data-ttu-id="9954f-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9954f-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9954f-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9954f-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9954f-154">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9954f-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="9954f-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9954f-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9954f-156">Satz-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9954f-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


