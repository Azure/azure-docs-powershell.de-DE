---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf99aba02bc4dee18ec6cfd2bdaf9fd83036e6d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843635"
---
# <span data-ttu-id="e67dd-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e67dd-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e67dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e67dd-102">SYNOPSIS</span></span>

## <span data-ttu-id="e67dd-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="e67dd-103">SYNTAX</span></span>

### <span data-ttu-id="e67dd-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e67dd-104">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e67dd-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e67dd-105">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e67dd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e67dd-106">DESCRIPTION</span></span>

## <span data-ttu-id="e67dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e67dd-107">EXAMPLES</span></span>

### <span data-ttu-id="e67dd-108">1:</span><span class="sxs-lookup"><span data-stu-id="e67dd-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e67dd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e67dd-109">PARAMETERS</span></span>

### <span data-ttu-id="e67dd-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="e67dd-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67dd-111">-DefaultProfile</span></span>
<span data-ttu-id="e67dd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e67dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e67dd-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e67dd-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e67dd-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="e67dd-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="e67dd-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="e67dd-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e67dd-117">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e67dd-118">-Name</span></span>
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

### <span data-ttu-id="e67dd-119">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e67dd-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67dd-120">CommonParameters</span></span>
<span data-ttu-id="e67dd-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67dd-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67dd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67dd-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e67dd-123">INPUTS</span></span>

### <span data-ttu-id="e67dd-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e67dd-124">PSLoadBalancer</span></span>
<span data-ttu-id="e67dd-125">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e67dd-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e67dd-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e67dd-126">OUTPUTS</span></span>

### <span data-ttu-id="e67dd-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e67dd-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e67dd-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e67dd-128">NOTES</span></span>

## <span data-ttu-id="e67dd-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e67dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="e67dd-130">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e67dd-130">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e67dd-131">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e67dd-131">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e67dd-132">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e67dd-132">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="e67dd-133">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e67dd-133">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)


