---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665364"
---
# <span data-ttu-id="b455f-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="b455f-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="b455f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b455f-102">SYNOPSIS</span></span>
<span data-ttu-id="b455f-103">Ruft vordefinierte SSL-Richtlinien von Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="b455f-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b455f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b455f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b455f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b455f-105">DESCRIPTION</span></span>
<span data-ttu-id="b455f-106">Das Cmdlet " **Get-AzureRmApplicationGatewaySslPredefinedPolicy** " erhält vordefinierte SSL-Richtlinien, die von Application Gateway bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b455f-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="b455f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b455f-107">EXAMPLES</span></span>

### <span data-ttu-id="b455f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b455f-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="b455f-109">Diese Befehle gibt alle vordefinierten SSL-Richtlinien zurück.</span><span class="sxs-lookup"><span data-stu-id="b455f-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="b455f-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b455f-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="b455f-111">Diese Befehle gibt eine vordefinierte Richtlinie mit dem Namen AppGwSslPolicy20170401 zurück.</span><span class="sxs-lookup"><span data-stu-id="b455f-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="b455f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b455f-112">PARAMETERS</span></span>

### <span data-ttu-id="b455f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b455f-113">-Name</span></span>
<span data-ttu-id="b455f-114">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b455f-114">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="b455f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b455f-115">-DefaultProfile</span></span>
<span data-ttu-id="b455f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b455f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b455f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b455f-117">CommonParameters</span></span>
<span data-ttu-id="b455f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b455f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b455f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b455f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b455f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b455f-120">INPUTS</span></span>

### <span data-ttu-id="b455f-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b455f-121">None</span></span>

## <span data-ttu-id="b455f-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b455f-122">OUTPUTS</span></span>

### <span data-ttu-id="b455f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="b455f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="b455f-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b455f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b455f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b455f-125">NOTES</span></span>

## <span data-ttu-id="b455f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b455f-126">RELATED LINKS</span></span>

