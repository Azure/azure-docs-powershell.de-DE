---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291665"
---
# <span data-ttu-id="f299c-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f299c-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="f299c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f299c-102">SYNOPSIS</span></span>
<span data-ttu-id="f299c-103">Entfernt eine "SSL-Richtlinie" aus einem Azure-Anwendungsgateway-SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="f299c-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f299c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f299c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f299c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f299c-105">DESCRIPTION</span></span>
<span data-ttu-id="f299c-106">Das Remove-AzApplicationGatewaySslProfilePolicy entfernt eine "SSL-Richtlinie" aus einem Azure-Anwendungsgateway-SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="f299c-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f299c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f299c-107">EXAMPLES</span></span>

### <span data-ttu-id="f299c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f299c-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="f299c-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="f299c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="f299c-110">Der zweite Befehl ruft das "Profile01" für $AppGw und speichert es in der $profile Variable.</span><span class="sxs-lookup"><span data-stu-id="f299c-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="f299c-111">Mit dem letzten Befehl wird die "ssl"-Richtlinie des in der Datei gespeicherten $profile.</span><span class="sxs-lookup"><span data-stu-id="f299c-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="f299c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f299c-112">PARAMETERS</span></span>

### <span data-ttu-id="f299c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f299c-113">-DefaultProfile</span></span>
<span data-ttu-id="f299c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f299c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f299c-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f299c-115">-SslProfile</span></span>
<span data-ttu-id="f299c-116">Das applicationGateway -SSL-Profil</span><span class="sxs-lookup"><span data-stu-id="f299c-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="f299c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f299c-117">-Confirm</span></span>
<span data-ttu-id="f299c-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f299c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f299c-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f299c-119">-WhatIf</span></span>
<span data-ttu-id="f299c-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f299c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f299c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f299c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f299c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f299c-122">CommonParameters</span></span>
<span data-ttu-id="f299c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f299c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f299c-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f299c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f299c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f299c-125">INPUTS</span></span>

### <span data-ttu-id="f299c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f299c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f299c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f299c-127">OUTPUTS</span></span>

### <span data-ttu-id="f299c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f299c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f299c-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f299c-129">NOTES</span></span>

## <span data-ttu-id="f299c-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f299c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f299c-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f299c-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f299c-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f299c-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f299c-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f299c-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f299c-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f299c-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)