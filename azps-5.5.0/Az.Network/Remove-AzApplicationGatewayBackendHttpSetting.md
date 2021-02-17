---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169757"
---
# <span data-ttu-id="c21fb-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c21fb-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="c21fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c21fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c21fb-103">Entfernt back-end-HTTP-Einstellungen aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c21fb-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="c21fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c21fb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c21fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c21fb-105">DESCRIPTION</span></span>
<span data-ttu-id="c21fb-106">Das Remove-AzApplicationGatewayBackendHttpSetting entfernt back-end Hypertext Transfer Protocol (HTTP)-Einstellungen von einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c21fb-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="c21fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c21fb-107">EXAMPLES</span></span>

### <span data-ttu-id="c21fb-108">Beispiel 1: Entfernen von Back-End-HTTP-Einstellungen von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="c21fb-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="c21fb-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="c21fb-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c21fb-110">Mit dem zweiten Befehl wird die Back-End-HTTP-Einstellung "BackEndSetting02" aus dem Anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c21fb-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c21fb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c21fb-111">PARAMETERS</span></span>

### <span data-ttu-id="c21fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c21fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="c21fb-113">Gibt das Anwendungsgateway an, aus dem dieses Cmdlet die Back-End-HTTP-Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="c21fb-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="c21fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21fb-114">-DefaultProfile</span></span>
<span data-ttu-id="c21fb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c21fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c21fb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c21fb-116">-Name</span></span>
<span data-ttu-id="c21fb-117">Gibt den Namen der Back-End-HTTP-Einstellungen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c21fb-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21fb-118">CommonParameters</span></span>
<span data-ttu-id="c21fb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21fb-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21fb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21fb-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c21fb-121">INPUTS</span></span>

### <span data-ttu-id="c21fb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c21fb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c21fb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c21fb-123">OUTPUTS</span></span>

### <span data-ttu-id="c21fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c21fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c21fb-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c21fb-125">NOTES</span></span>

## <span data-ttu-id="c21fb-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c21fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="c21fb-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c21fb-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c21fb-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c21fb-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c21fb-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c21fb-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c21fb-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c21fb-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

