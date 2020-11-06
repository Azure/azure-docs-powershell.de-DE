---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495910"
---
# <span data-ttu-id="929a9-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="929a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="929a9-102">SYNOPSIS</span></span>
<span data-ttu-id="929a9-103">Erstellt eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="929a9-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="929a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="929a9-104">SYNTAX</span></span>

### <span data-ttu-id="929a9-105">SetByResourceSubnet (Standard)</span><span class="sxs-lookup"><span data-stu-id="929a9-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929a9-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="929a9-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929a9-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="929a9-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929a9-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="929a9-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="929a9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="929a9-109">DESCRIPTION</span></span>
<span data-ttu-id="929a9-110">Das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** erstellt eine Front-End-IP-Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="929a9-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="929a9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="929a9-111">EXAMPLES</span></span>

### <span data-ttu-id="929a9-112">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="929a9-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="929a9-113">Der erste Befehl erstellt eine dynamische öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="929a9-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="929a9-114">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip.</span><span class="sxs-lookup"><span data-stu-id="929a9-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="929a9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="929a9-115">PARAMETERS</span></span>

### <span data-ttu-id="929a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929a9-116">-DefaultProfile</span></span>
<span data-ttu-id="929a9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="929a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="929a9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="929a9-118">-Name</span></span>
<span data-ttu-id="929a9-119">Gibt die Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="929a9-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="929a9-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="929a9-120">-PrivateIpAddress</span></span>
<span data-ttu-id="929a9-121">Gibt die private IP-Adresse des Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="929a9-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="929a9-122">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="929a9-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="929a9-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="929a9-123">-PublicIpAddress</span></span>
<span data-ttu-id="929a9-124">Gibt das **PublicIpAddress** -Objekt an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="929a9-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="929a9-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="929a9-125">-PublicIpAddressId</span></span>
<span data-ttu-id="929a9-126">Gibt die ID des **PublicIpAddress** -Objekts an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="929a9-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="929a9-127">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="929a9-127">-Subnet</span></span>
<span data-ttu-id="929a9-128">Gibt das **Subnet** -Objekt an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="929a9-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="929a9-129">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="929a9-129">-SubnetId</span></span>
<span data-ttu-id="929a9-130">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="929a9-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="929a9-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="929a9-131">-Zone</span></span>
<span data-ttu-id="929a9-132">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="929a9-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929a9-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="929a9-133">-Confirm</span></span>
<span data-ttu-id="929a9-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="929a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929a9-135">-WhatIf</span></span>
<span data-ttu-id="929a9-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="929a9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="929a9-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="929a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929a9-138">CommonParameters</span></span>
<span data-ttu-id="929a9-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929a9-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929a9-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="929a9-141">INPUTS</span></span>

### <span data-ttu-id="929a9-142">System. Collections. Generic. List \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="929a9-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="929a9-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="929a9-143">OUTPUTS</span></span>

### <span data-ttu-id="929a9-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="929a9-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="929a9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="929a9-145">NOTES</span></span>

## <span data-ttu-id="929a9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="929a9-146">RELATED LINKS</span></span>

[<span data-ttu-id="929a9-147">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="929a9-148">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="929a9-149">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="929a9-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="929a9-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="929a9-151">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="929a9-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


