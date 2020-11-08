---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174314"
---
# <span data-ttu-id="1e518-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1e518-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1e518-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e518-102">SYNOPSIS</span></span>
<span data-ttu-id="1e518-103">Entfernt eine Identität aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1e518-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="1e518-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e518-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e518-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e518-105">DESCRIPTION</span></span>
<span data-ttu-id="1e518-106">**Remove-AzApplicationGatewayIdentity-** Cmdlet entfernt die Identität aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1e518-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="1e518-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e518-107">EXAMPLES</span></span>

### <span data-ttu-id="1e518-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e518-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="1e518-109">In diesem Beispiel wird die Identität eines vorhandenen Anwendungs Gateways entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e518-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="1e518-110">Hinweis: Wenn das Gateway auf ein keyvault-Geheimnis verweist, ist es auch wichtig, diese SSL-Zertifikat Verweise entlang dieses Vorgangs zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1e518-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="1e518-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e518-111">PARAMETERS</span></span>

### <span data-ttu-id="1e518-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e518-112">-ApplicationGateway</span></span>
<span data-ttu-id="1e518-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e518-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1e518-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e518-114">-DefaultProfile</span></span>
<span data-ttu-id="1e518-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e518-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e518-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e518-116">-Confirm</span></span>
<span data-ttu-id="1e518-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e518-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e518-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e518-118">-WhatIf</span></span>
<span data-ttu-id="1e518-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e518-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e518-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e518-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e518-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e518-121">CommonParameters</span></span>
<span data-ttu-id="1e518-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e518-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e518-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e518-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e518-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e518-124">INPUTS</span></span>

### <span data-ttu-id="1e518-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e518-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e518-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e518-126">OUTPUTS</span></span>

### <span data-ttu-id="1e518-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e518-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e518-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e518-128">NOTES</span></span>

## <span data-ttu-id="1e518-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e518-129">RELATED LINKS</span></span>
