---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 8793da5f73ba1b6891d3522c171c167753188c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660464"
---
# <span data-ttu-id="00f45-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f45-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="00f45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00f45-102">SYNOPSIS</span></span>
<span data-ttu-id="00f45-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="00f45-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="00f45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f45-104">SYNTAX</span></span>

### <span data-ttu-id="00f45-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00f45-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f45-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="00f45-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f45-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00f45-107">DESCRIPTION</span></span>
<span data-ttu-id="00f45-108">Das Cmdlet **New-AzVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem virtuellen Netzwerk Gateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="00f45-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="00f45-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00f45-109">EXAMPLES</span></span>

### <span data-ttu-id="00f45-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="00f45-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="00f45-111">Konfiguriert ein virtuelles Netzwerk Gateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="00f45-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="00f45-112">Die Variable $myGWsubnet wird mit dem Cmdlet **Get-AzVirtualNetworkSubnetConfig** auf der "GatewaySubnet" im virtuellen Netzwerk abgerufen, in dem Sie ein virtuelles Netzwerk Gateway erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="00f45-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="00f45-113">Die Variable $myGWpip wird mit dem Cmdlet **New-AzPublicIpAddress** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="00f45-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="00f45-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f45-114">PARAMETERS</span></span>

### <span data-ttu-id="00f45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f45-115">-DefaultProfile</span></span>
<span data-ttu-id="00f45-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00f45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00f45-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00f45-117">-Name</span></span>
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

### <span data-ttu-id="00f45-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="00f45-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="00f45-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="00f45-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="00f45-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="00f45-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="00f45-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="00f45-121">-Subnet</span></span>
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

### <span data-ttu-id="00f45-122">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="00f45-122">-SubnetId</span></span>
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

### <span data-ttu-id="00f45-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f45-123">CommonParameters</span></span>
<span data-ttu-id="00f45-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f45-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f45-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f45-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f45-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00f45-126">INPUTS</span></span>

### <span data-ttu-id="00f45-127">Keine</span><span class="sxs-lookup"><span data-stu-id="00f45-127">None</span></span>

## <span data-ttu-id="00f45-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00f45-128">OUTPUTS</span></span>

### <span data-ttu-id="00f45-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f45-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="00f45-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="00f45-130">NOTES</span></span>

## <span data-ttu-id="00f45-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00f45-131">RELATED LINKS</span></span>

[<span data-ttu-id="00f45-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f45-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="00f45-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="00f45-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
