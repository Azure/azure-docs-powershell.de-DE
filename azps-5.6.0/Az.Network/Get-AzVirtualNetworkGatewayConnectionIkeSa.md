---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924739"
---
# <span data-ttu-id="d0fed-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="d0fed-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="d0fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0fed-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fed-103">IKE-Sicherheitszuordnungen einer Virtuellen Netzwerkgatewayverbindung erhalten</span><span class="sxs-lookup"><span data-stu-id="d0fed-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="d0fed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0fed-104">SYNTAX</span></span>

### <span data-ttu-id="d0fed-105">ByName</span><span class="sxs-lookup"><span data-stu-id="d0fed-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0fed-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0fed-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0fed-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0fed-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0fed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0fed-108">DESCRIPTION</span></span>
<span data-ttu-id="d0fed-109">Das **Get-AzVirtualNetworkGatewayConnectionIkeSa-Cmdlet** gibt die IKE-Sicherheitszuordnungen Ihrer Verbindung basierend auf dem Verbindungsnamen und ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="d0fed-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="d0fed-110">Wenn das **Get-AzVirtualNetworkGatewayConnection-Cmdlet** ohne Angabe des -Name-Parameters ausgegeben wird, werden in der Ausgabe die IKE-Sicherheitszuordnungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d0fed-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="d0fed-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0fed-111">EXAMPLES</span></span>

### <span data-ttu-id="d0fed-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0fed-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="d0fed-113">Gibt die IKE-Sicherheitszuordnungen für die Virtual Network Gateway-Verbindung mit dem Namen "myTunnel" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="d0fed-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="d0fed-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d0fed-114">PARAMETERS</span></span>

### <span data-ttu-id="d0fed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0fed-115">-AsJob</span></span>
<span data-ttu-id="d0fed-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="d0fed-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0fed-117">-DefaultProfile</span></span>
<span data-ttu-id="d0fed-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0fed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0fed-119">-InputObject</span></span>
<span data-ttu-id="d0fed-120">Das Verbindungsobjekt des virtuellen Netzwerkgateways, für das IKE-SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d0fed-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0fed-121">-Name</span></span>
<span data-ttu-id="d0fed-122">Der Name der Virtuellen Netzwerkgatewayverbindung, für den IKE-SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d0fed-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fed-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0fed-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0fed-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0fed-125">-ResourceId</span></span>
<span data-ttu-id="d0fed-126">Die Azure-Ressourcen-ID der Virtual Network Gateway-Verbindung, für die IKE-SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d0fed-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fed-127">CommonParameters</span></span>
<span data-ttu-id="d0fed-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0fed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fed-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0fed-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fed-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0fed-130">INPUTS</span></span>

### <span data-ttu-id="d0fed-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d0fed-131">System.String</span></span>

## <span data-ttu-id="d0fed-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0fed-132">OUTPUTS</span></span>

### <span data-ttu-id="d0fed-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="d0fed-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="d0fed-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d0fed-134">NOTES</span></span>

## <span data-ttu-id="d0fed-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d0fed-135">RELATED LINKS</span></span>
