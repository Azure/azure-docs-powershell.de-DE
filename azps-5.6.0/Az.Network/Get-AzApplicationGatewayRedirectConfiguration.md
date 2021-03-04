---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b2e62b0785cc01dfc9b26aeac7b267c06a4d24b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940352"
---
# <span data-ttu-id="c63de-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c63de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c63de-102">SYNOPSIS</span></span>
<span data-ttu-id="c63de-103">Ruft eine vorhandene Umleitungskonfiguration aus einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="c63de-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="c63de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c63de-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c63de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c63de-105">DESCRIPTION</span></span>
<span data-ttu-id="c63de-106">Das **Cmdlet Get-AzApplicationGatewayRedirectConfiguration** ruft eine vorhandene Umleitungskonfiguration aus einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="c63de-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="c63de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c63de-107">EXAMPLES</span></span>

### <span data-ttu-id="c63de-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c63de-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c63de-109">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c63de-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c63de-110">Der zweite Befehl ruft die Umleitungskonfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c63de-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c63de-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c63de-111">PARAMETERS</span></span>

### <span data-ttu-id="c63de-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63de-112">-ApplicationGateway</span></span>
<span data-ttu-id="c63de-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63de-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c63de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63de-114">-DefaultProfile</span></span>
<span data-ttu-id="c63de-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c63de-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c63de-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c63de-116">-Name</span></span>
<span data-ttu-id="c63de-117">Der Name der Anforderungsroutingregel</span><span class="sxs-lookup"><span data-stu-id="c63de-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="c63de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63de-118">CommonParameters</span></span>
<span data-ttu-id="c63de-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63de-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c63de-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63de-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c63de-121">INPUTS</span></span>

### <span data-ttu-id="c63de-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63de-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c63de-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c63de-123">OUTPUTS</span></span>

### <span data-ttu-id="c63de-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c63de-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c63de-125">NOTES</span></span>

## <span data-ttu-id="c63de-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c63de-126">RELATED LINKS</span></span>

[<span data-ttu-id="c63de-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c63de-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c63de-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c63de-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63de-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
