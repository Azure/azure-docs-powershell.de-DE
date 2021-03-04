---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 830f84b8f14e84693b6657fdea2542c2acf59b25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929443"
---
# <span data-ttu-id="1dbfa-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbfa-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1dbfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbfa-103">Entfernt die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1dbfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbfa-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbfa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbfa-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbfa-106">Das **Cmdlet Remove-AzApplicationGatewayClientAuthConfiguration** entfernt die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1dbfa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dbfa-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbfa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dbfa-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="1dbfa-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1dbfa-110">Der zweite Befehl ruft das SSL-Profil mit dem Namen Profile01 für $AppGw ab und speichert es in der $profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="1dbfa-111">Mit dem letzten Befehl wird die Clientauthentifizierungskonfiguration des ssl-Profils entfernt, das in $profile.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="1dbfa-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1dbfa-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbfa-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbfa-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbfa-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1dbfa-115">-SslProfile</span></span>
<span data-ttu-id="1dbfa-116">Das Ssl-Profil</span><span class="sxs-lookup"><span data-stu-id="1dbfa-116">The ssl profile</span></span>

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

### <span data-ttu-id="1dbfa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbfa-117">CommonParameters</span></span>
<span data-ttu-id="1dbfa-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbfa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbfa-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dbfa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbfa-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbfa-120">INPUTS</span></span>

### <span data-ttu-id="1dbfa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1dbfa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1dbfa-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbfa-122">OUTPUTS</span></span>

### <span data-ttu-id="1dbfa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1dbfa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1dbfa-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1dbfa-124">NOTES</span></span>

## <span data-ttu-id="1dbfa-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1dbfa-125">RELATED LINKS</span></span>

[<span data-ttu-id="1dbfa-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbfa-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1dbfa-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbfa-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1dbfa-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbfa-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1dbfa-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbfa-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)