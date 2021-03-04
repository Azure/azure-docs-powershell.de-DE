---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 88a89a17adc7a05e75865121d2133f723e534fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922763"
---
# <span data-ttu-id="ff0cb-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ff0cb-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="ff0cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0cb-103">Entfernt eine SSL-Richtlinie aus einem Azure-Anwendungsgateway-SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="ff0cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff0cb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff0cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff0cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0cb-106">Das Remove-AzApplicationGatewaySslProfilePolicy-Cmdlet entfernt eine SSL-Richtlinie aus einem AZURE-Anwendungsgateway-SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="ff0cb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff0cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ff0cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff0cb-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="ff0cb-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="ff0cb-110">Der zweite Befehl ruft das SSL-Profil mit dem Namen Profile01 für $AppGw ab und speichert es in der $profile Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="ff0cb-111">Mit dem letzten Befehl wird die SSL-Richtlinie des ssl-Profils entfernt, das in $profile.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="ff0cb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ff0cb-112">PARAMETERS</span></span>

### <span data-ttu-id="ff0cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0cb-113">-DefaultProfile</span></span>
<span data-ttu-id="ff0cb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0cb-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="ff0cb-115">-SslProfile</span></span>
<span data-ttu-id="ff0cb-116">Das applicationGateway SSL-Profil</span><span class="sxs-lookup"><span data-stu-id="ff0cb-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="ff0cb-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff0cb-117">-Confirm</span></span>
<span data-ttu-id="ff0cb-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0cb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0cb-119">-WhatIf</span></span>
<span data-ttu-id="ff0cb-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0cb-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0cb-122">CommonParameters</span></span>
<span data-ttu-id="ff0cb-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0cb-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff0cb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0cb-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff0cb-125">INPUTS</span></span>

### <span data-ttu-id="ff0cb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff0cb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ff0cb-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff0cb-127">OUTPUTS</span></span>

### <span data-ttu-id="ff0cb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff0cb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ff0cb-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ff0cb-129">NOTES</span></span>

## <span data-ttu-id="ff0cb-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ff0cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff0cb-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ff0cb-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ff0cb-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ff0cb-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ff0cb-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ff0cb-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ff0cb-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ff0cb-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)