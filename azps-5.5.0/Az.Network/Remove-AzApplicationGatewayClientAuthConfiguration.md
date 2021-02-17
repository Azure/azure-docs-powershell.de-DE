---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407589"
---
# <span data-ttu-id="c1b55-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b55-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c1b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b55-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b55-103">Entfernt die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="c1b55-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c1b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1b55-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b55-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1b55-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b55-106">Das **Cmdlet "Remove-AzApplicationGatewayClientAuthConfiguration"** entfernt die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="c1b55-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c1b55-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1b55-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b55-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1b55-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="c1b55-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="c1b55-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c1b55-110">Der zweite Befehl ruft das "Profile01" für $AppGw und speichert es in der $profile Variable.</span><span class="sxs-lookup"><span data-stu-id="c1b55-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="c1b55-111">Mit dem letzten Befehl wird die Clientauthentifizierungskonfiguration des in der E-Mail gespeicherten $profile.</span><span class="sxs-lookup"><span data-stu-id="c1b55-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="c1b55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1b55-112">PARAMETERS</span></span>

### <span data-ttu-id="c1b55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b55-113">-DefaultProfile</span></span>
<span data-ttu-id="c1b55-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1b55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b55-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c1b55-115">-SslProfile</span></span>
<span data-ttu-id="c1b55-116">Das Ssl-Profil</span><span class="sxs-lookup"><span data-stu-id="c1b55-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b55-117">CommonParameters</span></span>
<span data-ttu-id="c1b55-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b55-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1b55-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b55-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1b55-120">INPUTS</span></span>

### <span data-ttu-id="c1b55-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c1b55-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c1b55-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1b55-122">OUTPUTS</span></span>

### <span data-ttu-id="c1b55-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c1b55-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c1b55-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1b55-124">NOTES</span></span>

## <span data-ttu-id="c1b55-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1b55-125">RELATED LINKS</span></span>

[<span data-ttu-id="c1b55-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b55-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="c1b55-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b55-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c1b55-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1b55-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
