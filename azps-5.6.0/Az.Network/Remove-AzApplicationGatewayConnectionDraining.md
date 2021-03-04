---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ddcec36e8561196b31dd94eb15d99a7e2a92a378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924656"
---
# <span data-ttu-id="ef983-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef983-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ef983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef983-102">SYNOPSIS</span></span>
<span data-ttu-id="ef983-103">Entfernt die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="ef983-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ef983-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef983-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef983-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef983-105">DESCRIPTION</span></span>
<span data-ttu-id="ef983-106">Das **Cmdlet Remove-AzApplicationGatewayConnectionDraining** entfernt die Verbindungsablaufkonfiguration eines Back-End-HTTP-Einstellungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="ef983-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ef983-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef983-107">EXAMPLES</span></span>

### <span data-ttu-id="ef983-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef983-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ef983-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef983-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef983-110">Der zweite Befehl ruft die Back-End-HTTP-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef983-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ef983-111">Mit dem letzten Befehl wird die Verbindungsablaufkonfiguration der in der Datei gespeicherten Back-End-HTTP-Einstellungen $Settings.</span><span class="sxs-lookup"><span data-stu-id="ef983-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="ef983-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ef983-112">PARAMETERS</span></span>

### <span data-ttu-id="ef983-113">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef983-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ef983-114">Die Back-End-Http-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ef983-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef983-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef983-115">-DefaultProfile</span></span>
<span data-ttu-id="ef983-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef983-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef983-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef983-117">CommonParameters</span></span>
<span data-ttu-id="ef983-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef983-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef983-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef983-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef983-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef983-120">INPUTS</span></span>

### <span data-ttu-id="ef983-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef983-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ef983-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef983-122">OUTPUTS</span></span>

### <span data-ttu-id="ef983-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef983-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ef983-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ef983-124">NOTES</span></span>

## <span data-ttu-id="ef983-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ef983-125">RELATED LINKS</span></span>

[<span data-ttu-id="ef983-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef983-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ef983-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ef983-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ef983-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef983-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ef983-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef983-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ef983-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ef983-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

