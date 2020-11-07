---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660849"
---
# <span data-ttu-id="cb3c9-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="cb3c9-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="cb3c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3c9-103">Abrufen der Identität, die dem Anwendungsgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cb3c9-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="cb3c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb3c9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb3c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="cb3c9-106">Das Cmdlet " **Get-AzApplicationGatewayIdentity** " Ruft die Identität ab, die dem Anwendungsgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cb3c9-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="cb3c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="cb3c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cb3c9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="cb3c9-109">In diesen Beispielen wird gezeigt, wie Sie Application Gateway Identity vom Application Gateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="cb3c9-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="cb3c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb3c9-110">PARAMETERS</span></span>

### <span data-ttu-id="cb3c9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb3c9-111">-ApplicationGateway</span></span>
<span data-ttu-id="cb3c9-112">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb3c9-112">The applicationGateway</span></span>

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

### <span data-ttu-id="cb3c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3c9-113">-DefaultProfile</span></span>
<span data-ttu-id="cb3c9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb3c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3c9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3c9-115">CommonParameters</span></span>
<span data-ttu-id="cb3c9-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb3c9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3c9-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb3c9-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3c9-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb3c9-118">INPUTS</span></span>

### <span data-ttu-id="cb3c9-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb3c9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb3c9-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb3c9-120">OUTPUTS</span></span>

### <span data-ttu-id="cb3c9-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cb3c9-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="cb3c9-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb3c9-122">NOTES</span></span>

## <span data-ttu-id="cb3c9-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb3c9-123">RELATED LINKS</span></span>
