---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850735"
---
# <span data-ttu-id="035d0-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="035d0-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="035d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="035d0-102">SYNOPSIS</span></span>
<span data-ttu-id="035d0-103">Ruft vordefinierte SSL-Richtlinien von Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="035d0-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="035d0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="035d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="035d0-105">DESCRIPTION</span></span>
<span data-ttu-id="035d0-106">Das Cmdlet " **Get-AzureRmApplicationGatewaySslPredefinedPolicy** " erhält vordefinierte SSL-Richtlinien, die von Application Gateway bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="035d0-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="035d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="035d0-107">EXAMPLES</span></span>

### <span data-ttu-id="035d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="035d0-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="035d0-109">Diese Befehle gibt alle vordefinierten SSL-Richtlinien zurück.</span><span class="sxs-lookup"><span data-stu-id="035d0-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="035d0-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="035d0-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="035d0-111">Diese Befehle gibt eine vordefinierte Richtlinie mit dem Namen AppGwSslPolicy20170401 zurück.</span><span class="sxs-lookup"><span data-stu-id="035d0-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="035d0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="035d0-112">PARAMETERS</span></span>

### <span data-ttu-id="035d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035d0-113">-DefaultProfile</span></span>
<span data-ttu-id="035d0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="035d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="035d0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="035d0-115">-Name</span></span>
<span data-ttu-id="035d0-116">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="035d0-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="035d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035d0-117">CommonParameters</span></span>
<span data-ttu-id="035d0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035d0-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035d0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035d0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="035d0-120">INPUTS</span></span>

### <span data-ttu-id="035d0-121">Keine</span><span class="sxs-lookup"><span data-stu-id="035d0-121">None</span></span>

## <span data-ttu-id="035d0-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="035d0-122">OUTPUTS</span></span>

### <span data-ttu-id="035d0-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="035d0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="035d0-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="035d0-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="035d0-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="035d0-125">NOTES</span></span>

## <span data-ttu-id="035d0-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="035d0-126">RELATED LINKS</span></span>

