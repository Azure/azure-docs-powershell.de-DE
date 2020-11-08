---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006391"
---
# <span data-ttu-id="3d9ab-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3d9ab-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3d9ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9ab-103">Erstellt eine Azure Virtual Gateway-Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="3d9ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d9ab-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d9ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9ab-106">Das Cmdlet **New-AzureVirtualNetworkGatewayConnection** erstellt eine Azure Virtual Gateway-Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="3d9ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d9ab-107">EXAMPLES</span></span>

## <span data-ttu-id="3d9ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d9ab-108">PARAMETERS</span></span>

### <span data-ttu-id="3d9ab-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3d9ab-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3d9ab-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3d9ab-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3d9ab-111">-EnableBgp</span></span>
<span data-ttu-id="3d9ab-112">Aktiviert das Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="3d9ab-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="3d9ab-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="3d9ab-113">-GatewayConnectionName</span></span>
<span data-ttu-id="3d9ab-114">Gibt einen Namen für die Gateway-Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="3d9ab-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="3d9ab-115">-GatewayConnectionType</span></span>
<span data-ttu-id="3d9ab-116">Gibt den Typ der Gatewayverbindung an.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ab-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d9ab-117">-Profile</span></span>
<span data-ttu-id="3d9ab-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3d9ab-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ab-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="3d9ab-120">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ab-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3d9ab-121">-SharedKey</span></span>
<span data-ttu-id="3d9ab-122">Gibt einen freigegebenen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="3d9ab-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="3d9ab-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="3d9ab-124">Gibt die ID eines virtuellen Netzwerkgateways an.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="3d9ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9ab-125">CommonParameters</span></span>
<span data-ttu-id="3d9ab-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9ab-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9ab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9ab-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d9ab-128">INPUTS</span></span>

## <span data-ttu-id="3d9ab-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d9ab-129">OUTPUTS</span></span>

## <span data-ttu-id="3d9ab-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d9ab-130">NOTES</span></span>

## <span data-ttu-id="3d9ab-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d9ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d9ab-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3d9ab-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3d9ab-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3d9ab-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3d9ab-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3d9ab-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


