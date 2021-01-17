---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291160"
---
# <span data-ttu-id="a9dba-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a9dba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9dba-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dba-103">Ruft die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="a9dba-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="a9dba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9dba-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9dba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9dba-105">DESCRIPTION</span></span>
<span data-ttu-id="a9dba-106">Das **Cmdlet "Get-AzApplicationGatewayClientAuthConfiguration"** ruft die Clientauthentifizierungskonfiguration eines SSL-Profilobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="a9dba-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="a9dba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9dba-107">EXAMPLES</span></span>

### <span data-ttu-id="a9dba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9dba-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="a9dba-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="a9dba-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="a9dba-110">Der zweite Befehl ruft das "SslProfile01"-Profil für $AppGw und speichert es $SslProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="a9dba-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="a9dba-111">Der letzte Befehl ruft die Clientauthentifizierungskonfiguration aus dem $SslProfile A0 ab und speichert sie in $ClientAuthConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="a9dba-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="a9dba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9dba-112">PARAMETERS</span></span>

### <span data-ttu-id="a9dba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dba-113">-DefaultProfile</span></span>
<span data-ttu-id="a9dba-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9dba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9dba-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="a9dba-115">-SslProfile</span></span>
<span data-ttu-id="a9dba-116">Das Ssl-Profil</span><span class="sxs-lookup"><span data-stu-id="a9dba-116">The ssl profile</span></span>

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

### <span data-ttu-id="a9dba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dba-117">CommonParameters</span></span>
<span data-ttu-id="a9dba-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dba-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9dba-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dba-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9dba-120">INPUTS</span></span>

### <span data-ttu-id="a9dba-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a9dba-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a9dba-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9dba-122">OUTPUTS</span></span>

### <span data-ttu-id="a9dba-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a9dba-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9dba-124">NOTES</span></span>

## <span data-ttu-id="a9dba-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9dba-125">RELATED LINKS</span></span>

[<span data-ttu-id="a9dba-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a9dba-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a9dba-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a9dba-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9dba-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)