---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: e0999a5dc61574d600daf113e1641483c8a8bd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504066"
---
# <span data-ttu-id="50f40-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50f40-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="50f40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50f40-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f40-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="50f40-103">SYNTAX</span></span>

### <span data-ttu-id="50f40-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="50f40-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50f40-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="50f40-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f40-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50f40-106">DESCRIPTION</span></span>

## <span data-ttu-id="50f40-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50f40-107">EXAMPLES</span></span>

### <span data-ttu-id="50f40-108">1:</span><span class="sxs-lookup"><span data-stu-id="50f40-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="50f40-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50f40-109">PARAMETERS</span></span>

### <span data-ttu-id="50f40-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="50f40-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-111">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="50f40-111">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-112">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="50f40-112">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="50f40-113">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="50f40-113">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-114">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="50f40-114">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50f40-115">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-116">-Name</span><span class="sxs-lookup"><span data-stu-id="50f40-116">-Name</span></span>
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

### <span data-ttu-id="50f40-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="50f40-117">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f40-118">-DefaultProfile</span></span>
<span data-ttu-id="50f40-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50f40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f40-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f40-120">CommonParameters</span></span>
<span data-ttu-id="50f40-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f40-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f40-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f40-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f40-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50f40-123">INPUTS</span></span>

### <span data-ttu-id="50f40-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50f40-124">PSLoadBalancer</span></span>
<span data-ttu-id="50f40-125">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="50f40-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="50f40-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50f40-126">OUTPUTS</span></span>

### <span data-ttu-id="50f40-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50f40-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="50f40-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="50f40-128">NOTES</span></span>

## <span data-ttu-id="50f40-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50f40-129">RELATED LINKS</span></span>

