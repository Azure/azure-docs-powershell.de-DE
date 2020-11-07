---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841688"
---
# <span data-ttu-id="9d624-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="9d624-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="9d624-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d624-102">SYNOPSIS</span></span>
<span data-ttu-id="9d624-103">Ruft vordefinierte SSL-Richtlinien von Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="9d624-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="9d624-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d624-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d624-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d624-105">DESCRIPTION</span></span>
<span data-ttu-id="9d624-106">Das Cmdlet " **Get-AzApplicationGatewaySslPredefinedPolicy** " erhält vordefinierte SSL-Richtlinien, die von Application Gateway bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9d624-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="9d624-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d624-107">EXAMPLES</span></span>

### <span data-ttu-id="9d624-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d624-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="9d624-109">Diese Befehle gibt alle vordefinierten SSL-Richtlinien zurück.</span><span class="sxs-lookup"><span data-stu-id="9d624-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="9d624-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d624-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="9d624-111">Diese Befehle gibt eine vordefinierte Richtlinie mit dem Namen AppGwSslPolicy20170401 zurück.</span><span class="sxs-lookup"><span data-stu-id="9d624-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="9d624-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d624-112">PARAMETERS</span></span>

### <span data-ttu-id="9d624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d624-113">-DefaultProfile</span></span>
<span data-ttu-id="9d624-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d624-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9d624-115">-Name</span></span>
<span data-ttu-id="9d624-116">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9d624-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="9d624-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d624-117">CommonParameters</span></span>
<span data-ttu-id="9d624-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d624-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d624-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d624-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d624-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d624-120">INPUTS</span></span>

### <span data-ttu-id="9d624-121">Keine</span><span class="sxs-lookup"><span data-stu-id="9d624-121">None</span></span>

## <span data-ttu-id="9d624-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d624-122">OUTPUTS</span></span>

### <span data-ttu-id="9d624-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="9d624-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="9d624-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d624-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d624-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d624-125">NOTES</span></span>

## <span data-ttu-id="9d624-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d624-126">RELATED LINKS</span></span>

