---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395689"
---
# <span data-ttu-id="06df9-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="06df9-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="06df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06df9-102">SYNOPSIS</span></span>
<span data-ttu-id="06df9-103">Ändert die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="06df9-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="06df9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06df9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06df9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06df9-105">DESCRIPTION</span></span>
<span data-ttu-id="06df9-106">Das **Cmdlet "Set-AzApplicationGatewayClientAuthConfiguration"** ändert die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="06df9-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="06df9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06df9-107">EXAMPLES</span></span>

### <span data-ttu-id="06df9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06df9-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="06df9-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="06df9-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="06df9-110">Der zweite Befehl ruft das ssl-Profil "SslProfile01" für $AppGw und speichert die Einstellungen in der $profile Variable.</span><span class="sxs-lookup"><span data-stu-id="06df9-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="06df9-111">Mit dem letzten Befehl wird die Clientauthentifizierungskonfiguration des in der Datei gespeicherten $profile.</span><span class="sxs-lookup"><span data-stu-id="06df9-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="06df9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06df9-112">PARAMETERS</span></span>

### <span data-ttu-id="06df9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06df9-113">-DefaultProfile</span></span>
<span data-ttu-id="06df9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06df9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06df9-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="06df9-115">-SslProfile</span></span>
<span data-ttu-id="06df9-116">Das Ssl-Profil</span><span class="sxs-lookup"><span data-stu-id="06df9-116">The ssl profile</span></span>

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

### <span data-ttu-id="06df9-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="06df9-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="06df9-118">Überprüfen Sie den Ausstellernamen des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="06df9-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06df9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06df9-119">CommonParameters</span></span>
<span data-ttu-id="06df9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06df9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06df9-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06df9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06df9-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06df9-122">INPUTS</span></span>

### <span data-ttu-id="06df9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="06df9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="06df9-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06df9-124">OUTPUTS</span></span>

### <span data-ttu-id="06df9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="06df9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="06df9-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06df9-126">NOTES</span></span>

## <span data-ttu-id="06df9-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06df9-127">RELATED LINKS</span></span>


[<span data-ttu-id="06df9-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="06df9-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="06df9-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="06df9-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="06df9-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="06df9-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
