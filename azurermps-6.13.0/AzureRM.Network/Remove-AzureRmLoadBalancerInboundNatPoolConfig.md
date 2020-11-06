---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476037"
---
# <span data-ttu-id="0b085-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0b085-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0b085-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b085-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b085-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b085-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b085-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b085-104">DESCRIPTION</span></span>

## <span data-ttu-id="0b085-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b085-105">EXAMPLES</span></span>

### <span data-ttu-id="0b085-106">1: Entfernen</span><span class="sxs-lookup"><span data-stu-id="0b085-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="0b085-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b085-107">PARAMETERS</span></span>

### <span data-ttu-id="0b085-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b085-108">-DefaultProfile</span></span>
<span data-ttu-id="0b085-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b085-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b085-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b085-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b085-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0b085-111">-Name</span></span>
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

### <span data-ttu-id="0b085-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b085-112">-Confirm</span></span>
<span data-ttu-id="0b085-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b085-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b085-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b085-114">-WhatIf</span></span>
<span data-ttu-id="0b085-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b085-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b085-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b085-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b085-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b085-117">CommonParameters</span></span>
<span data-ttu-id="0b085-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b085-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b085-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b085-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b085-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b085-120">INPUTS</span></span>

### <span data-ttu-id="0b085-121">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b085-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="0b085-122">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b085-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="0b085-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b085-123">OUTPUTS</span></span>

### <span data-ttu-id="0b085-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b085-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0b085-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b085-125">NOTES</span></span>

## <span data-ttu-id="0b085-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b085-126">RELATED LINKS</span></span>
