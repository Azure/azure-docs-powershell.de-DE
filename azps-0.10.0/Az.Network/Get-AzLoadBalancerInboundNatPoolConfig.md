---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d3dcdabc84eca5efa7e52e61f4beafd23eb67b05
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841635"
---
# <span data-ttu-id="966ec-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="966ec-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="966ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="966ec-102">SYNOPSIS</span></span>

## <span data-ttu-id="966ec-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="966ec-103">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="966ec-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="966ec-104">DESCRIPTION</span></span>

## <span data-ttu-id="966ec-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="966ec-105">EXAMPLES</span></span>

### <span data-ttu-id="966ec-106">1:</span><span class="sxs-lookup"><span data-stu-id="966ec-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="966ec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="966ec-107">PARAMETERS</span></span>

### <span data-ttu-id="966ec-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966ec-108">-DefaultProfile</span></span>
<span data-ttu-id="966ec-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="966ec-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966ec-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="966ec-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="966ec-111">-Name</span><span class="sxs-lookup"><span data-stu-id="966ec-111">-Name</span></span>
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

### <span data-ttu-id="966ec-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966ec-112">CommonParameters</span></span>
<span data-ttu-id="966ec-113">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966ec-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966ec-114">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="966ec-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966ec-115">Eingaben</span><span class="sxs-lookup"><span data-stu-id="966ec-115">INPUTS</span></span>

### <span data-ttu-id="966ec-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="966ec-116">PSLoadBalancer</span></span>
<span data-ttu-id="966ec-117">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="966ec-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="966ec-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="966ec-118">OUTPUTS</span></span>

### <span data-ttu-id="966ec-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="966ec-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="966ec-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="966ec-120">NOTES</span></span>

## <span data-ttu-id="966ec-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="966ec-121">RELATED LINKS</span></span>

