---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b00c3950140c0ebf158170a8ddd2396e62c2b2c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663352"
---
# <span data-ttu-id="2ed86-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ed86-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="2ed86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ed86-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed86-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="2ed86-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ed86-104">SYNTAX</span></span>

### <span data-ttu-id="2ed86-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ed86-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ed86-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2ed86-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed86-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ed86-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed86-108">Das Cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem virtuellen Netzwerk Gateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2ed86-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="2ed86-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ed86-109">EXAMPLES</span></span>

### <span data-ttu-id="2ed86-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="2ed86-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="2ed86-111">Konfiguriert ein virtuelles Netzwerk Gateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2ed86-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="2ed86-112">Die Variable $myGWsubnet wird mit dem Cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** auf der "GatewaySubnet" im virtuellen Netzwerk abgerufen, in dem Sie ein virtuelles Netzwerk Gateway erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2ed86-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="2ed86-113">Die Variable $myGWpip wird mit dem Cmdlet **New-AzureRmPublicIpAddress** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2ed86-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="2ed86-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ed86-114">PARAMETERS</span></span>

### <span data-ttu-id="2ed86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed86-115">-DefaultProfile</span></span>
<span data-ttu-id="2ed86-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ed86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed86-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2ed86-117">-Name</span></span>
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

### <span data-ttu-id="2ed86-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ed86-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed86-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ed86-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed86-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2ed86-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="2ed86-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="2ed86-121">-Subnet</span></span>
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

### <span data-ttu-id="2ed86-122">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="2ed86-122">-SubnetId</span></span>
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

### <span data-ttu-id="2ed86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed86-123">CommonParameters</span></span>
<span data-ttu-id="2ed86-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed86-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed86-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed86-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ed86-126">INPUTS</span></span>

### <span data-ttu-id="2ed86-127">Keine</span><span class="sxs-lookup"><span data-stu-id="2ed86-127">None</span></span>

## <span data-ttu-id="2ed86-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ed86-128">OUTPUTS</span></span>

### <span data-ttu-id="2ed86-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed86-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="2ed86-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ed86-130">NOTES</span></span>

## <span data-ttu-id="2ed86-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ed86-131">RELATED LINKS</span></span>
