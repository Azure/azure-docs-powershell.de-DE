---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 92e094576306707bb2a3c0533cb6863581163393
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940280"
---
# <span data-ttu-id="8a9e2-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="8a9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9e2-103">Ruft die SSL-Richtlinie eines Anwendungsgateways -SSL-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="8a9e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a9e2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a9e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9e2-106">Das **Get-AzApplicationGatewaySslProfilePolicy-Cmdlet** ruft die SSL-Richtlinie eines SSL-Profils für das Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="8a9e2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9e2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a9e2-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="8a9e2-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="8a9e2-110">Der zweite Befehl ruft das SSL-Profil mit dem Namen SslProfile01 für $AppGw ab und speichert es $SslProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="8a9e2-111">Der letzte Befehl ruft die SSL-Richtlinie aus der SSL-Profil-$SslProfile und speichert sie in der $sslpolicy-Variable.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="8a9e2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a9e2-112">PARAMETERS</span></span>

### <span data-ttu-id="8a9e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9e2-113">-DefaultProfile</span></span>
<span data-ttu-id="8a9e2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9e2-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="8a9e2-115">-SslProfile</span></span>
<span data-ttu-id="8a9e2-116">Das Anwendungsgateway-SSL-Profil</span><span class="sxs-lookup"><span data-stu-id="8a9e2-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="8a9e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9e2-117">CommonParameters</span></span>
<span data-ttu-id="8a9e2-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9e2-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a9e2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9e2-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a9e2-120">INPUTS</span></span>

### <span data-ttu-id="8a9e2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8a9e2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8a9e2-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a9e2-122">OUTPUTS</span></span>

### <span data-ttu-id="8a9e2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8a9e2-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a9e2-124">NOTES</span></span>

## <span data-ttu-id="8a9e2-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a9e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="8a9e2-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="8a9e2-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="8a9e2-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="8a9e2-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="8a9e2-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)