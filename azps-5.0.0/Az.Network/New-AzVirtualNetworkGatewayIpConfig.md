---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178320"
---
# <span data-ttu-id="7aa35-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7aa35-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7aa35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7aa35-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa35-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="7aa35-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="7aa35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aa35-104">SYNTAX</span></span>

### <span data-ttu-id="7aa35-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7aa35-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7aa35-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7aa35-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aa35-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7aa35-107">DESCRIPTION</span></span>
<span data-ttu-id="7aa35-108">Das Cmdlet **New-AzVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem virtuellen Netzwerk Gateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7aa35-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="7aa35-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7aa35-109">EXAMPLES</span></span>

### <span data-ttu-id="7aa35-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="7aa35-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="7aa35-111">Konfiguriert ein virtuelles Netzwerk Gateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="7aa35-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="7aa35-112">Die Variable $myGWsubnet wird mit dem Cmdlet **Get-AzVirtualNetworkSubnetConfig** auf der "GatewaySubnet" im virtuellen Netzwerk abgerufen, in dem Sie ein virtuelles Netzwerk Gateway erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7aa35-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="7aa35-113">Die Variable $myGWpip wird mit dem Cmdlet **New-AzPublicIpAddress** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7aa35-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="7aa35-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aa35-114">PARAMETERS</span></span>

### <span data-ttu-id="7aa35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa35-115">-DefaultProfile</span></span>
<span data-ttu-id="7aa35-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7aa35-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa35-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7aa35-117">-Name</span></span>
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

### <span data-ttu-id="7aa35-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7aa35-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="7aa35-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7aa35-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="7aa35-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7aa35-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="7aa35-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="7aa35-121">-Subnet</span></span>
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

### <span data-ttu-id="7aa35-122">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="7aa35-122">-SubnetId</span></span>
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

### <span data-ttu-id="7aa35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa35-123">CommonParameters</span></span>
<span data-ttu-id="7aa35-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa35-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa35-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa35-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7aa35-126">INPUTS</span></span>

### <span data-ttu-id="7aa35-127">Keine</span><span class="sxs-lookup"><span data-stu-id="7aa35-127">None</span></span>

## <span data-ttu-id="7aa35-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7aa35-128">OUTPUTS</span></span>

### <span data-ttu-id="7aa35-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7aa35-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="7aa35-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7aa35-130">NOTES</span></span>

## <span data-ttu-id="7aa35-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7aa35-131">RELATED LINKS</span></span>

[<span data-ttu-id="7aa35-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7aa35-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7aa35-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7aa35-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
