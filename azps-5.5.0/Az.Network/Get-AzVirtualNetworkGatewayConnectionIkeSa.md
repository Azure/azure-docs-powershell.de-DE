---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147036"
---
# <span data-ttu-id="a65ec-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="a65ec-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="a65ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a65ec-103">Erhalten von IKE-Sicherheitszuordnungen einer virtuellen Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="a65ec-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="a65ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a65ec-104">SYNTAX</span></span>

### <span data-ttu-id="a65ec-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a65ec-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65ec-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a65ec-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65ec-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a65ec-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a65ec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a65ec-108">DESCRIPTION</span></span>
<span data-ttu-id="a65ec-109">Das **Cmdlet "Get-AzVirtualNetworkGatewayConnectionIkeSa"** gibt die IKE-Sicherheitszuordnungen Ihrer Verbindung basierend auf dem Verbindungsnamen und dem Namen der Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="a65ec-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="a65ec-110">Wenn das **Cmdlet "Get-AzVirtualNetworkGatewayConnection"** ohne Angabe des Parameters "-Name" ausgegeben wird, werden in der Ausgabe die IKE-Sicherheitszuordnungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a65ec-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="a65ec-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a65ec-111">EXAMPLES</span></span>

### <span data-ttu-id="a65ec-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a65ec-112">Example 1</span></span>
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

<span data-ttu-id="a65ec-113">Gibt die IKE-Sicherheitszuordnungen für die virtuelle Netzwerkgatewayverbindung mit dem Namen "myTyp" in der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="a65ec-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="a65ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a65ec-114">PARAMETERS</span></span>

### <span data-ttu-id="a65ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a65ec-115">-AsJob</span></span>
<span data-ttu-id="a65ec-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="a65ec-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a65ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65ec-117">-DefaultProfile</span></span>
<span data-ttu-id="a65ec-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a65ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a65ec-119">-InputObject</span></span>
<span data-ttu-id="a65ec-120">Das Verbindungsobjekt des virtuellen Netzwerkgateways, für das IKE SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a65ec-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="a65ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a65ec-121">-Name</span></span>
<span data-ttu-id="a65ec-122">Der Name der virtuellen Netzwerkgateway-Verbindung, für die IKE SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a65ec-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="a65ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="a65ec-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a65ec-124">The resource group name.</span></span>

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

### <span data-ttu-id="a65ec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a65ec-125">-ResourceId</span></span>
<span data-ttu-id="a65ec-126">Die Azure-Ressourcen-ID der Virtuellen Netzwerkgatewayverbindung, für die IKE SAs abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a65ec-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="a65ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65ec-127">CommonParameters</span></span>
<span data-ttu-id="a65ec-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65ec-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a65ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65ec-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a65ec-130">INPUTS</span></span>

### <span data-ttu-id="a65ec-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a65ec-131">System.String</span></span>

## <span data-ttu-id="a65ec-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a65ec-132">OUTPUTS</span></span>

### <span data-ttu-id="a65ec-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="a65ec-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="a65ec-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a65ec-134">NOTES</span></span>

## <span data-ttu-id="a65ec-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a65ec-135">RELATED LINKS</span></span>
