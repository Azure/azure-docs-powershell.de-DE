---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850656"
---
# <span data-ttu-id="7c95e-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c95e-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7c95e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c95e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c95e-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="7c95e-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c95e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c95e-104">SYNTAX</span></span>

### <span data-ttu-id="7c95e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c95e-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c95e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7c95e-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c95e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c95e-107">DESCRIPTION</span></span>
<span data-ttu-id="7c95e-108">Das Cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem virtuellen Netzwerk Gateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7c95e-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="7c95e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c95e-109">EXAMPLES</span></span>

### <span data-ttu-id="7c95e-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="7c95e-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="7c95e-111">Konfiguriert ein virtuelles Netzwerk Gateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="7c95e-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="7c95e-112">Die Variable $myGWsubnet wird mit dem Cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** auf der "GatewaySubnet" im virtuellen Netzwerk abgerufen, in dem Sie ein virtuelles Netzwerk Gateway erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c95e-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="7c95e-113">Die Variable $myGWpip wird mit dem Cmdlet **New-AzureRmPublicIpAddress** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c95e-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="7c95e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c95e-114">PARAMETERS</span></span>

### <span data-ttu-id="7c95e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c95e-115">-DefaultProfile</span></span>
<span data-ttu-id="7c95e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c95e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c95e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7c95e-117">-Name</span></span>
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

### <span data-ttu-id="7c95e-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7c95e-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c95e-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7c95e-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c95e-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7c95e-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="7c95e-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="7c95e-121">-Subnet</span></span>
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

### <span data-ttu-id="7c95e-122">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="7c95e-122">-SubnetId</span></span>
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

### <span data-ttu-id="7c95e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c95e-123">CommonParameters</span></span>
<span data-ttu-id="7c95e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c95e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c95e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c95e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c95e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c95e-126">INPUTS</span></span>

## <span data-ttu-id="7c95e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c95e-127">OUTPUTS</span></span>

### <span data-ttu-id="7c95e-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c95e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="7c95e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c95e-129">NOTES</span></span>

## <span data-ttu-id="7c95e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c95e-130">RELATED LINKS</span></span>

