---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: d235a43e4b5f2bcec2e93a9dfda4860588647179
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841483"
---
# <span data-ttu-id="4d721-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="4d721-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="4d721-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d721-102">SYNOPSIS</span></span>
<span data-ttu-id="4d721-103">Listet von einem Azure Virtual Network Gateway gelernte Routen auf</span><span class="sxs-lookup"><span data-stu-id="4d721-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="4d721-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d721-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d721-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d721-105">DESCRIPTION</span></span>
<span data-ttu-id="4d721-106">Listet Routen auf, die von einem Azure Virtual Network Gateway aus verschiedenen Quellen erlernt wurden.</span><span class="sxs-lookup"><span data-stu-id="4d721-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="4d721-107">Dazu gehören Routen, die über BGP gelernt werden, sowie statische Routen.</span><span class="sxs-lookup"><span data-stu-id="4d721-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="4d721-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d721-108">EXAMPLES</span></span>

### <span data-ttu-id="4d721-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d721-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="4d721-110">Ruft für das Azure Virtual Network Gateway mit dem Namen "Gatewayname" in der Ressourcengruppe "ResourceGroup" die Routen ab, die das Azure-Gateway kennt.</span><span class="sxs-lookup"><span data-stu-id="4d721-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="4d721-111">Das Azure Virtual Network Gateway hat in diesem Fall zwei statische Routen (10.1.0.0/16 und 10.0.0.254/32) sowie eine Route, die über BGP (10.0.0.0/16) erlernt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d721-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="4d721-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d721-112">PARAMETERS</span></span>

### <span data-ttu-id="4d721-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d721-113">-AsJob</span></span>
<span data-ttu-id="4d721-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4d721-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d721-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d721-115">-DefaultProfile</span></span>
<span data-ttu-id="4d721-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d721-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d721-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d721-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d721-118">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="4d721-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="4d721-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4d721-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4d721-120">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="4d721-120">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d721-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d721-121">CommonParameters</span></span>
<span data-ttu-id="4d721-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d721-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d721-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d721-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d721-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d721-124">INPUTS</span></span>

### <span data-ttu-id="4d721-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d721-125">System.String</span></span>

## <span data-ttu-id="4d721-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d721-126">OUTPUTS</span></span>

### <span data-ttu-id="4d721-127">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="4d721-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="4d721-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d721-128">NOTES</span></span>

## <span data-ttu-id="4d721-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d721-129">RELATED LINKS</span></span>

