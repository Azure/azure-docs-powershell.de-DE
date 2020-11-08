---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173232"
---
# <span data-ttu-id="e34a8-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e34a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e34a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e34a8-103">Erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e34a8-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="e34a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e34a8-104">SYNTAX</span></span>

### <span data-ttu-id="e34a8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e34a8-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e34a8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e34a8-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e34a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e34a8-107">DESCRIPTION</span></span>
<span data-ttu-id="e34a8-108">Das Cmdlet **New-AzApplicationGatewayIPConfiguration** erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e34a8-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="e34a8-109">Die IP-Konfiguration enthält das Subnetz, in dem Application Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e34a8-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="e34a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e34a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e34a8-111">Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e34a8-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="e34a8-112">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.</span><span class="sxs-lookup"><span data-stu-id="e34a8-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="e34a8-113">Der zweite Befehl ruft die Subnetz-Konfiguration für das Subnetz ab, zu dem das virtuelle Netzwerk im vorherigen Befehl gehört, und speichert es in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e34a8-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="e34a8-114">Der dritte Befehl erstellt die IP-Konfiguration mithilfe von $Subnet.</span><span class="sxs-lookup"><span data-stu-id="e34a8-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="e34a8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e34a8-115">PARAMETERS</span></span>

### <span data-ttu-id="e34a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e34a8-116">-DefaultProfile</span></span>
<span data-ttu-id="e34a8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e34a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e34a8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e34a8-118">-Name</span></span>
<span data-ttu-id="e34a8-119">Gibt den Namen der zu erstellende IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e34a8-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="e34a8-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="e34a8-120">-Subnet</span></span>
<span data-ttu-id="e34a8-121">Gibt das Subnet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e34a8-121">Specifies the subnet object.</span></span>
<span data-ttu-id="e34a8-122">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e34a8-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e34a8-123">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="e34a8-123">-SubnetId</span></span>
<span data-ttu-id="e34a8-124">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="e34a8-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="e34a8-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e34a8-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="e34a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34a8-126">CommonParameters</span></span>
<span data-ttu-id="e34a8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e34a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34a8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e34a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34a8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e34a8-129">INPUTS</span></span>

### <span data-ttu-id="e34a8-130">Keine</span><span class="sxs-lookup"><span data-stu-id="e34a8-130">None</span></span>

## <span data-ttu-id="e34a8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e34a8-131">OUTPUTS</span></span>

### <span data-ttu-id="e34a8-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e34a8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e34a8-133">NOTES</span></span>

## <span data-ttu-id="e34a8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e34a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="e34a8-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e34a8-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e34a8-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e34a8-138">Satz-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e34a8-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


