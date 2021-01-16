---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468168"
---
# <span data-ttu-id="3ae89-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3ae89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae89-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae89-103">Ruft das "SSL"-Profil eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="3ae89-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="3ae89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ae89-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae89-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ae89-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae89-106">Das **Cmdlet "Get-AzApplicationGatewaySslProfile"** ruft das Profil eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="3ae89-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="3ae89-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ae89-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae89-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ae89-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="3ae89-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft das SSL-Profil SslProfile01 für $AppGw und speichert es in der $profile Variable.</span><span class="sxs-lookup"><span data-stu-id="3ae89-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="3ae89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae89-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae89-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ae89-111">-ApplicationGateway</span></span>
<span data-ttu-id="3ae89-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ae89-112">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ae89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-113">-DefaultProfile</span></span>
<span data-ttu-id="3ae89-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ae89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3ae89-115">-Name</span></span>
<span data-ttu-id="3ae89-116">Der Name des Ssl-Profils</span><span class="sxs-lookup"><span data-stu-id="3ae89-116">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae89-117">CommonParameters</span></span>
<span data-ttu-id="3ae89-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae89-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae89-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae89-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ae89-120">INPUTS</span></span>

### <span data-ttu-id="3ae89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ae89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ae89-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ae89-122">OUTPUTS</span></span>

### <span data-ttu-id="3ae89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3ae89-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ae89-124">NOTES</span></span>

## <span data-ttu-id="3ae89-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ae89-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ae89-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3ae89-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3ae89-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3ae89-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3ae89-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)