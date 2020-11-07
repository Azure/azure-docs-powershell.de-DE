---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 4928df8bd24769e0ebb3eb60728a30a5c55f36fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848144"
---
# <span data-ttu-id="5f424-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5f424-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f424-102">SYNOPSIS</span></span>
<span data-ttu-id="5f424-103">Erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5f424-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f424-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f424-104">SYNTAX</span></span>

### <span data-ttu-id="5f424-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f424-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f424-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5f424-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f424-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f424-107">DESCRIPTION</span></span>
<span data-ttu-id="5f424-108">Das Cmdlet **New-AzureRmApplicationGatewayIPConfiguration** erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5f424-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="5f424-109">Die IP-Konfiguration enthält das Subnetz, in dem Application Gateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5f424-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="5f424-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f424-110">EXAMPLES</span></span>

### <span data-ttu-id="5f424-111">Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="5f424-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="5f424-112">Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.</span><span class="sxs-lookup"><span data-stu-id="5f424-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="5f424-113">Der zweite Befehl ruft die Subnetz-Konfiguration für das Subnetz ab, zu dem das virtuelle Netzwerk im vorherigen Befehl gehört, und speichert es in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5f424-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="5f424-114">Der dritte Befehl erstellt die IP-Konfiguration mithilfe von $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5f424-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="5f424-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f424-115">PARAMETERS</span></span>

### <span data-ttu-id="5f424-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f424-116">-DefaultProfile</span></span>
<span data-ttu-id="5f424-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f424-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f424-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f424-118">-Name</span></span>
<span data-ttu-id="5f424-119">Gibt den Namen der zu erstellende IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5f424-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="5f424-120">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5f424-120">-Subnet</span></span>
<span data-ttu-id="5f424-121">Gibt das Subnet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5f424-121">Specifies the subnet object.</span></span>
<span data-ttu-id="5f424-122">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5f424-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f424-123">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="5f424-123">-SubnetId</span></span>
<span data-ttu-id="5f424-124">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="5f424-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="5f424-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5f424-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f424-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f424-126">CommonParameters</span></span>
<span data-ttu-id="5f424-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f424-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f424-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f424-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f424-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f424-129">INPUTS</span></span>

### <span data-ttu-id="5f424-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5f424-130">System.String</span></span>

## <span data-ttu-id="5f424-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f424-131">OUTPUTS</span></span>

### <span data-ttu-id="5f424-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5f424-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f424-133">NOTES</span></span>

## <span data-ttu-id="5f424-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f424-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f424-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5f424-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5f424-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5f424-138">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f424-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


