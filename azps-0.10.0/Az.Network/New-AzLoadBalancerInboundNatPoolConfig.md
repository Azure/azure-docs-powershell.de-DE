---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841332"
---
# <span data-ttu-id="70ebf-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70ebf-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="70ebf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70ebf-102">SYNOPSIS</span></span>

## <span data-ttu-id="70ebf-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ebf-103">SYNTAX</span></span>

### <span data-ttu-id="70ebf-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="70ebf-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ebf-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="70ebf-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70ebf-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ebf-106">DESCRIPTION</span></span>

## <span data-ttu-id="70ebf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="70ebf-108">1:</span><span class="sxs-lookup"><span data-stu-id="70ebf-108">1:</span></span>
```

```

## <span data-ttu-id="70ebf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ebf-109">PARAMETERS</span></span>

### <span data-ttu-id="70ebf-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="70ebf-110">-BackendPort</span></span>
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

### <span data-ttu-id="70ebf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ebf-111">-DefaultProfile</span></span>
<span data-ttu-id="70ebf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70ebf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ebf-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ebf-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="70ebf-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="70ebf-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="70ebf-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="70ebf-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="70ebf-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="70ebf-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="70ebf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="70ebf-117">-Name</span></span>
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

### <span data-ttu-id="70ebf-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="70ebf-118">-Protocol</span></span>
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

### <span data-ttu-id="70ebf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ebf-119">CommonParameters</span></span>
<span data-ttu-id="70ebf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ebf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ebf-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ebf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ebf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70ebf-122">INPUTS</span></span>

## <span data-ttu-id="70ebf-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70ebf-123">OUTPUTS</span></span>

### <span data-ttu-id="70ebf-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="70ebf-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="70ebf-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="70ebf-125">NOTES</span></span>

## <span data-ttu-id="70ebf-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70ebf-126">RELATED LINKS</span></span>

