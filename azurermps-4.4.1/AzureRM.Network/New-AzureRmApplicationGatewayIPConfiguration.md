---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502670"
---
# <span data-ttu-id="9beb0-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9beb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9beb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9beb0-103">Erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9beb0-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9beb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9beb0-104">SYNTAX</span></span>

### <span data-ttu-id="9beb0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9beb0-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9beb0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9beb0-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9beb0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9beb0-107">DESCRIPTION</span></span>
<span data-ttu-id="9beb0-108">Das Cmdlet **New-AzureRmApplicationGatewayIPConfiguration** erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9beb0-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="9beb0-109">Die IP-Konfiguration enthält das Subnetz, in dem Application Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9beb0-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="9beb0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9beb0-110">EXAMPLES</span></span>

### <span data-ttu-id="9beb0-111">Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9beb0-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="9beb0-112">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.</span><span class="sxs-lookup"><span data-stu-id="9beb0-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="9beb0-113">Der zweite Befehl ruft die Subnetz-Konfiguration für das Subnetz ab, zu dem das virtuelle Netzwerk im vorherigen Befehl gehört, und speichert es in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9beb0-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="9beb0-114">Der dritte Befehl erstellt die IP-Konfiguration mithilfe von $Subnet.</span><span class="sxs-lookup"><span data-stu-id="9beb0-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="9beb0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9beb0-115">PARAMETERS</span></span>

### <span data-ttu-id="9beb0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9beb0-116">-Name</span></span>
<span data-ttu-id="9beb0-117">Gibt den Namen der zu erstellende IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9beb0-117">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="9beb0-118">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="9beb0-118">-Subnet</span></span>
<span data-ttu-id="9beb0-119">Gibt das Subnet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9beb0-119">Specifies the subnet object.</span></span>
<span data-ttu-id="9beb0-120">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9beb0-120">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="9beb0-121">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="9beb0-121">-SubnetId</span></span>
<span data-ttu-id="9beb0-122">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="9beb0-122">Specifies the subnet ID.</span></span>
<span data-ttu-id="9beb0-123">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9beb0-123">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="9beb0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9beb0-124">-DefaultProfile</span></span>
<span data-ttu-id="9beb0-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9beb0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9beb0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9beb0-126">CommonParameters</span></span>
<span data-ttu-id="9beb0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9beb0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9beb0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9beb0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9beb0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9beb0-129">INPUTS</span></span>

### <span data-ttu-id="9beb0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9beb0-130">System.String</span></span>

## <span data-ttu-id="9beb0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9beb0-131">OUTPUTS</span></span>

### <span data-ttu-id="9beb0-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9beb0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9beb0-133">NOTES</span></span>

## <span data-ttu-id="9beb0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9beb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="9beb0-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9beb0-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9beb0-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9beb0-138">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9beb0-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


