---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 8def7a737bd3d97cb4250cb9be0a1d7bcc781d50
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841252"
---
# <span data-ttu-id="71e96-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="71e96-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="71e96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71e96-102">SYNOPSIS</span></span>
<span data-ttu-id="71e96-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="71e96-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="71e96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71e96-104">SYNTAX</span></span>

### <span data-ttu-id="71e96-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71e96-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e96-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="71e96-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e96-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71e96-107">DESCRIPTION</span></span>
<span data-ttu-id="71e96-108">Das Cmdlet **New-AzVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem virtuellen Netzwerk Gateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="71e96-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="71e96-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71e96-109">EXAMPLES</span></span>

### <span data-ttu-id="71e96-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="71e96-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="71e96-111">Konfiguriert ein virtuelles Netzwerk Gateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="71e96-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="71e96-112">Die Variable $myGWsubnet wird mit dem Cmdlet **Get-AzVirtualNetworkSubnetConfig** auf der "GatewaySubnet" im virtuellen Netzwerk abgerufen, in dem Sie ein virtuelles Netzwerk Gateway erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="71e96-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="71e96-113">Die Variable $myGWpip wird mit dem Cmdlet **New-AzPublicIpAddress** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="71e96-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="71e96-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="71e96-114">PARAMETERS</span></span>

### <span data-ttu-id="71e96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e96-115">-DefaultProfile</span></span>
<span data-ttu-id="71e96-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71e96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e96-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71e96-117">-Name</span></span>
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

### <span data-ttu-id="71e96-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="71e96-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="71e96-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="71e96-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="71e96-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="71e96-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="71e96-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="71e96-121">-Subnet</span></span>
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

### <span data-ttu-id="71e96-122">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="71e96-122">-SubnetId</span></span>
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

### <span data-ttu-id="71e96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e96-123">CommonParameters</span></span>
<span data-ttu-id="71e96-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e96-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e96-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e96-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71e96-126">INPUTS</span></span>

## <span data-ttu-id="71e96-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71e96-127">OUTPUTS</span></span>

### <span data-ttu-id="71e96-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="71e96-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="71e96-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="71e96-129">NOTES</span></span>

## <span data-ttu-id="71e96-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71e96-130">RELATED LINKS</span></span>

