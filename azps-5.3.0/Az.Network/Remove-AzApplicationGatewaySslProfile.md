---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459864"
---
# <span data-ttu-id="fcb1e-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="fcb1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb1e-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb1e-103">Entfernt das Ssl-Profil von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="fcb1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcb1e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcb1e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcb1e-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb1e-106">Das **Cmdlet "Remove-AzApplicationGatewaySslProfile"** entfernt das Ssl-Profil aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="fcb1e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcb1e-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb1e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcb1e-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="fcb1e-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="fcb1e-110">Mit dem zweiten Befehl wird das ssl-Profil mit dem Namen "SslProfile01" aus dem Anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fcb1e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcb1e-111">PARAMETERS</span></span>

### <span data-ttu-id="fcb1e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcb1e-112">-ApplicationGateway</span></span>
<span data-ttu-id="fcb1e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcb1e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fcb1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-114">-DefaultProfile</span></span>
<span data-ttu-id="fcb1e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb1e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fcb1e-116">-Name</span></span>
<span data-ttu-id="fcb1e-117">Der Name des Ssl-Profils</span><span class="sxs-lookup"><span data-stu-id="fcb1e-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb1e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb1e-118">CommonParameters</span></span>
<span data-ttu-id="fcb1e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb1e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb1e-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcb1e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb1e-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcb1e-121">INPUTS</span></span>

### <span data-ttu-id="fcb1e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcb1e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fcb1e-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcb1e-123">OUTPUTS</span></span>

### <span data-ttu-id="fcb1e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcb1e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fcb1e-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcb1e-125">NOTES</span></span>

## <span data-ttu-id="fcb1e-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcb1e-126">RELATED LINKS</span></span>

[<span data-ttu-id="fcb1e-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="fcb1e-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="fcb1e-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="fcb1e-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="fcb1e-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)