---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504042"
---
# <span data-ttu-id="7e392-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7e392-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7e392-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e392-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e392-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e392-103">SYNTAX</span></span>

### <span data-ttu-id="7e392-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e392-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e392-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7e392-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e392-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e392-106">DESCRIPTION</span></span>

## <span data-ttu-id="7e392-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e392-107">EXAMPLES</span></span>

## <span data-ttu-id="7e392-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e392-108">PARAMETERS</span></span>

### <span data-ttu-id="7e392-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7e392-109">-BackendPort</span></span>
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

### <span data-ttu-id="7e392-110">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e392-110">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="7e392-111">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7e392-111">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="7e392-112">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7e392-112">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="7e392-113">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7e392-113">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="7e392-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7e392-114">-Name</span></span>
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

### <span data-ttu-id="7e392-115">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7e392-115">-Protocol</span></span>
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

### <span data-ttu-id="7e392-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e392-116">-DefaultProfile</span></span>
<span data-ttu-id="7e392-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e392-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e392-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e392-118">CommonParameters</span></span>
<span data-ttu-id="7e392-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e392-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e392-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e392-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e392-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e392-121">INPUTS</span></span>

## <span data-ttu-id="7e392-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e392-122">OUTPUTS</span></span>

### <span data-ttu-id="7e392-123">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="7e392-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="7e392-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e392-124">NOTES</span></span>

## <span data-ttu-id="7e392-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e392-125">RELATED LINKS</span></span>

