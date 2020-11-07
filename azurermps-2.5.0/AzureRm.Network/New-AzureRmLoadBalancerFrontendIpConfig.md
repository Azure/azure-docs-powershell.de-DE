---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 3cd241b84f7ac03dc268a8f04df0490f6a9f9665
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850387"
---
# <span data-ttu-id="83fe4-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83fe4-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="83fe4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="83fe4-103">Erstellt eine Front-End-IP-Konfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="83fe4-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83fe4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fe4-104">SYNTAX</span></span>

### <span data-ttu-id="83fe4-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="83fe4-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83fe4-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="83fe4-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83fe4-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83fe4-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83fe4-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83fe4-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83fe4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83fe4-109">DESCRIPTION</span></span>
<span data-ttu-id="83fe4-110">Das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** erstellt eine Front-End-IP-Konfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="83fe4-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="83fe4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83fe4-111">EXAMPLES</span></span>

### <span data-ttu-id="83fe4-112">Beispiel 1: Erstellen einer Front-End-IP-Konfiguration für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="83fe4-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="83fe4-113">Der erste Befehl erstellt eine dynamische öffentliche IP-Adresse mit dem Namen MyPublicIP in der Ressourcengruppe mit dem Namen myresourcegroup und speichert Sie dann in der $publicip-Variablen.</span><span class="sxs-lookup"><span data-stu-id="83fe4-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="83fe4-114">Der zweite Befehl erstellt eine Front-End-IP-Konfiguration mit dem Namen FrontendIpConfig01 unter Verwendung der öffentlichen IP-Adresse in $publicip.</span><span class="sxs-lookup"><span data-stu-id="83fe4-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="83fe4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="83fe4-115">PARAMETERS</span></span>

### <span data-ttu-id="83fe4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fe4-116">-DefaultProfile</span></span>
<span data-ttu-id="83fe4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83fe4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83fe4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="83fe4-118">-Name</span></span>
<span data-ttu-id="83fe4-119">Gibt die Front-End-IP-Konfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="83fe4-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="83fe4-120">-PrivateIpAddress</span></span>
<span data-ttu-id="83fe4-121">Gibt die private IP-Adresse des Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="83fe4-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="83fe4-122">Geben Sie diesen Parameter nur an, wenn Sie auch den *Subnet* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="83fe4-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83fe4-123">-PublicIpAddress</span></span>
<span data-ttu-id="83fe4-124">Gibt das **PublicIpAddress** -Objekt an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fe4-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="83fe4-125">-PublicIpAddressId</span></span>
<span data-ttu-id="83fe4-126">Gibt die ID des **PublicIpAddress** -Objekts an, das einer Front-End-IP-Konfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fe4-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-127">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="83fe4-127">-Subnet</span></span>
<span data-ttu-id="83fe4-128">Gibt das **Subnet** -Objekt an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fe4-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-129">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="83fe4-129">-SubnetId</span></span>
<span data-ttu-id="83fe4-130">Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fe4-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fe4-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="83fe4-131">-Zone</span></span>
<span data-ttu-id="83fe4-132">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="83fe4-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="83fe4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fe4-133">CommonParameters</span></span>
<span data-ttu-id="83fe4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fe4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fe4-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fe4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fe4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83fe4-136">INPUTS</span></span>

## <span data-ttu-id="83fe4-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83fe4-137">OUTPUTS</span></span>

### <span data-ttu-id="83fe4-138">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="83fe4-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="83fe4-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="83fe4-139">NOTES</span></span>

## <span data-ttu-id="83fe4-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83fe4-140">RELATED LINKS</span></span>

[<span data-ttu-id="83fe4-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83fe4-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83fe4-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83fe4-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83fe4-143">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83fe4-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="83fe4-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83fe4-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83fe4-145">Satz-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83fe4-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


