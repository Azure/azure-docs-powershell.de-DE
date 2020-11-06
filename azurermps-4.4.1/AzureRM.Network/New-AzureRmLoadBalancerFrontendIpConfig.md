---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0f5db9dd785f5fdfc45bf75b4da082900a563632
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504041"
---
# <span data-ttu-id="458b6-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="458b6-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="458b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="458b6-102">SYNOPSIS</span></span>
<span data-ttu-id="458b6-103">Erstellt eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="458b6-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="458b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="458b6-104">SYNTAX</span></span>

### <span data-ttu-id="458b6-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="458b6-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="458b6-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="458b6-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="458b6-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="458b6-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="458b6-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="458b6-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="458b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="458b6-109">DESCRIPTION</span></span>
<span data-ttu-id="458b6-110">Das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** erstellt eine Front-End-IP-Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="458b6-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="458b6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="458b6-111">EXAMPLES</span></span>

### <span data-ttu-id="458b6-112">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="458b6-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="458b6-113">Der erste Befehl erstellt eine dynamische öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="458b6-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="458b6-114">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip.</span><span class="sxs-lookup"><span data-stu-id="458b6-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="458b6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="458b6-115">PARAMETERS</span></span>

### <span data-ttu-id="458b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458b6-116">-DefaultProfile</span></span>
<span data-ttu-id="458b6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="458b6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458b6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="458b6-118">-Name</span></span>
<span data-ttu-id="458b6-119">Gibt die Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="458b6-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="458b6-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="458b6-120">-PrivateIpAddress</span></span>
<span data-ttu-id="458b6-121">Gibt die private IP-Adresse des Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="458b6-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="458b6-122">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="458b6-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458b6-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="458b6-123">-PublicIpAddress</span></span>
<span data-ttu-id="458b6-124">Gibt das **PublicIpAddress** -Objekt an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="458b6-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458b6-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="458b6-125">-PublicIpAddressId</span></span>
<span data-ttu-id="458b6-126">Gibt die ID des **PublicIpAddress** -Objekts an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="458b6-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458b6-127">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="458b6-127">-Subnet</span></span>
<span data-ttu-id="458b6-128">Gibt das **Subnet** -Objekt an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="458b6-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458b6-129">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="458b6-129">-SubnetId</span></span>
<span data-ttu-id="458b6-130">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="458b6-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458b6-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="458b6-131">-Zone</span></span>
<span data-ttu-id="458b6-132">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="458b6-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="458b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458b6-133">CommonParameters</span></span>
<span data-ttu-id="458b6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458b6-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458b6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458b6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="458b6-136">INPUTS</span></span>

## <span data-ttu-id="458b6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="458b6-137">OUTPUTS</span></span>

### <span data-ttu-id="458b6-138">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="458b6-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="458b6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="458b6-139">NOTES</span></span>

## <span data-ttu-id="458b6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="458b6-140">RELATED LINKS</span></span>

[<span data-ttu-id="458b6-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="458b6-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="458b6-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="458b6-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="458b6-143">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="458b6-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="458b6-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="458b6-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="458b6-145">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="458b6-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


