---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468199"
---
# <span data-ttu-id="7794b-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7794b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7794b-102">SYNOPSIS</span></span>
<span data-ttu-id="7794b-103">Ruft eine vorhandene Umleitungskonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="7794b-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7794b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7794b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7794b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7794b-105">DESCRIPTION</span></span>
<span data-ttu-id="7794b-106">Das **Cmdlet "Get-AzApplicationGatewayRedirectConfiguration"** ruft eine vorhandene Umleitungskonfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="7794b-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7794b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7794b-107">EXAMPLES</span></span>

### <span data-ttu-id="7794b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7794b-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="7794b-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7794b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7794b-110">Der zweite Befehl ruft die Umleitungskonfiguration namens Redirect01 vom Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7794b-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7794b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7794b-111">PARAMETERS</span></span>

### <span data-ttu-id="7794b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7794b-112">-ApplicationGateway</span></span>
<span data-ttu-id="7794b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7794b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7794b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7794b-114">-DefaultProfile</span></span>
<span data-ttu-id="7794b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7794b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7794b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7794b-116">-Name</span></span>
<span data-ttu-id="7794b-117">Der Name der Anforderungsroutingregel</span><span class="sxs-lookup"><span data-stu-id="7794b-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="7794b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7794b-118">CommonParameters</span></span>
<span data-ttu-id="7794b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7794b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7794b-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7794b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7794b-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7794b-121">INPUTS</span></span>

### <span data-ttu-id="7794b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7794b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7794b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7794b-123">OUTPUTS</span></span>

### <span data-ttu-id="7794b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7794b-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7794b-125">NOTES</span></span>

## <span data-ttu-id="7794b-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7794b-126">RELATED LINKS</span></span>

[<span data-ttu-id="7794b-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7794b-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7794b-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7794b-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7794b-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
