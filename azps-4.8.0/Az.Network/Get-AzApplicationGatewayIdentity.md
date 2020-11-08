---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167210"
---
# <span data-ttu-id="14b5a-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="14b5a-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="14b5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="14b5a-103">Abrufen der Identität, die dem Anwendungsgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="14b5a-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="14b5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b5a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="14b5a-106">Das Cmdlet " **Get-AzApplicationGatewayIdentity** " Ruft die Identität ab, die dem Anwendungsgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="14b5a-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="14b5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="14b5a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14b5a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="14b5a-109">In diesen Beispielen wird gezeigt, wie Sie Application Gateway Identity vom Application Gateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="14b5a-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="14b5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="14b5a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14b5a-111">-ApplicationGateway</span></span>
<span data-ttu-id="14b5a-112">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="14b5a-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="14b5a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14b5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b5a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b5a-115">CommonParameters</span></span>
<span data-ttu-id="14b5a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b5a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b5a-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14b5a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b5a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14b5a-118">INPUTS</span></span>

### <span data-ttu-id="14b5a-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14b5a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14b5a-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14b5a-120">OUTPUTS</span></span>

### <span data-ttu-id="14b5a-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="14b5a-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="14b5a-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="14b5a-122">NOTES</span></span>

## <span data-ttu-id="14b5a-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14b5a-123">RELATED LINKS</span></span>
