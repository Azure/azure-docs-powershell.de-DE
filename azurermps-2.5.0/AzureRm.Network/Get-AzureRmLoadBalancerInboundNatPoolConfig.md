---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 20837f96bc17d2cfd71abc359ff4114b44e6c062
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848795"
---
# <span data-ttu-id="d8b9f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d8b9f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d8b9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8b9f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b9f-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8b9f-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b9f-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8b9f-104">DESCRIPTION</span></span>

## <span data-ttu-id="d8b9f-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8b9f-105">EXAMPLES</span></span>

### <span data-ttu-id="d8b9f-106">1:</span><span class="sxs-lookup"><span data-stu-id="d8b9f-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d8b9f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8b9f-107">PARAMETERS</span></span>

### <span data-ttu-id="d8b9f-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b9f-108">-DefaultProfile</span></span>
<span data-ttu-id="d8b9f-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b9f-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8b9f-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="d8b9f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="d8b9f-111">-Name</span></span>
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

### <span data-ttu-id="d8b9f-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b9f-112">CommonParameters</span></span>
<span data-ttu-id="d8b9f-113">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b9f-114">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b9f-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b9f-115">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8b9f-115">INPUTS</span></span>

### <span data-ttu-id="d8b9f-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8b9f-116">PSLoadBalancer</span></span>
<span data-ttu-id="d8b9f-117">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d8b9f-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8b9f-118">OUTPUTS</span></span>

### <span data-ttu-id="d8b9f-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d8b9f-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d8b9f-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8b9f-120">NOTES</span></span>

## <span data-ttu-id="d8b9f-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8b9f-121">RELATED LINKS</span></span>

