---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296680"
---
# <span data-ttu-id="38762-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="38762-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="38762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38762-102">SYNOPSIS</span></span>
<span data-ttu-id="38762-103">Ruft die "SSL-Richtlinie" eines Anwendungsgateways -SSL-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="38762-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="38762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38762-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38762-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38762-105">DESCRIPTION</span></span>
<span data-ttu-id="38762-106">Das **Cmdlet "Get-AzApplicationGatewaySslProfilePolicy"** ruft die "SSL-Richtlinie" eines Anwendungsgateways-SSL-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="38762-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="38762-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38762-107">EXAMPLES</span></span>

### <span data-ttu-id="38762-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38762-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="38762-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="38762-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="38762-110">Der zweite Befehl ruft das "SslProfile01"-Profil für $AppGw und speichert es $SslProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="38762-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="38762-111">Der letzte Befehl ruft die "SSL"-Richtlinie aus dem $SslProfile und speichert sie in der $sslpolicy Variable.</span><span class="sxs-lookup"><span data-stu-id="38762-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="38762-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38762-112">PARAMETERS</span></span>

### <span data-ttu-id="38762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38762-113">-DefaultProfile</span></span>
<span data-ttu-id="38762-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38762-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38762-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="38762-115">-SslProfile</span></span>
<span data-ttu-id="38762-116">Das Anwendungsgateway-SSL-Profil</span><span class="sxs-lookup"><span data-stu-id="38762-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="38762-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38762-117">CommonParameters</span></span>
<span data-ttu-id="38762-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38762-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38762-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38762-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38762-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38762-120">INPUTS</span></span>

### <span data-ttu-id="38762-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="38762-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="38762-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38762-122">OUTPUTS</span></span>

### <span data-ttu-id="38762-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="38762-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="38762-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38762-124">NOTES</span></span>

## <span data-ttu-id="38762-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38762-125">RELATED LINKS</span></span>

[<span data-ttu-id="38762-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="38762-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="38762-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="38762-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="38762-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="38762-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="38762-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="38762-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)