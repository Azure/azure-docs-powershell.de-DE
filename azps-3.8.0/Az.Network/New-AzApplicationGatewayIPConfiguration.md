---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005008"
---
# <span data-ttu-id="13734-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="13734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13734-102">SYNOPSIS</span></span>
<span data-ttu-id="13734-103">Erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="13734-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="13734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13734-104">SYNTAX</span></span>

### <span data-ttu-id="13734-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13734-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13734-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="13734-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13734-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13734-107">DESCRIPTION</span></span>
<span data-ttu-id="13734-108">Das Cmdlet **New-AzApplicationGatewayIPConfiguration** erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="13734-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="13734-109">Die IP-Konfiguration enthält das Subnetz, in dem Application Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="13734-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="13734-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13734-110">EXAMPLES</span></span>

### <span data-ttu-id="13734-111">Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="13734-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="13734-112">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.</span><span class="sxs-lookup"><span data-stu-id="13734-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="13734-113">Der zweite Befehl ruft die Subnetz-Konfiguration für das Subnetz ab, zu dem das virtuelle Netzwerk im vorherigen Befehl gehört, und speichert es in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="13734-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="13734-114">Der dritte Befehl erstellt die IP-Konfiguration mithilfe von $Subnet.</span><span class="sxs-lookup"><span data-stu-id="13734-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="13734-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="13734-115">PARAMETERS</span></span>

### <span data-ttu-id="13734-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13734-116">-DefaultProfile</span></span>
<span data-ttu-id="13734-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13734-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13734-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13734-118">-Name</span></span>
<span data-ttu-id="13734-119">Gibt den Namen der zu erstellende IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="13734-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="13734-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="13734-120">-Subnet</span></span>
<span data-ttu-id="13734-121">Gibt das Subnet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="13734-121">Specifies the subnet object.</span></span>
<span data-ttu-id="13734-122">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="13734-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13734-123">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="13734-123">-SubnetId</span></span>
<span data-ttu-id="13734-124">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="13734-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="13734-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="13734-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13734-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13734-126">CommonParameters</span></span>
<span data-ttu-id="13734-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13734-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13734-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13734-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13734-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13734-129">INPUTS</span></span>

### <span data-ttu-id="13734-130">Keine</span><span class="sxs-lookup"><span data-stu-id="13734-130">None</span></span>

## <span data-ttu-id="13734-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13734-131">OUTPUTS</span></span>

### <span data-ttu-id="13734-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="13734-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="13734-133">NOTES</span></span>

## <span data-ttu-id="13734-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13734-134">RELATED LINKS</span></span>

[<span data-ttu-id="13734-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="13734-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="13734-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="13734-138">Satz-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13734-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


