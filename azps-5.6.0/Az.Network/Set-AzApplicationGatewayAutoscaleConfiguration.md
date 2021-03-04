---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: bfa5cbfdb8ab734a8c6ca8b651808213b9b10f3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921672"
---
# <span data-ttu-id="95dd4-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="95dd4-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="95dd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="95dd4-103">Aktualisiert die Automatische Skalierungskonfiguration eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="95dd4-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="95dd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95dd4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95dd4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95dd4-105">DESCRIPTION</span></span>
<span data-ttu-id="95dd4-106">Das **Cmdlet Set-AzApplicationGatewayAutoscaleConfiguration** ändert die vorhandene Konfiguration der automatischen Skalierung eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="95dd4-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="95dd4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95dd4-107">EXAMPLES</span></span>

### <span data-ttu-id="95dd4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95dd4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="95dd4-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="95dd4-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="95dd4-110">Mit dem zweiten Befehl wird die Konfiguration der automatischen Skalierung über das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="95dd4-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="95dd4-111">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="95dd4-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="95dd4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95dd4-112">PARAMETERS</span></span>

### <span data-ttu-id="95dd4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95dd4-113">-ApplicationGateway</span></span>
<span data-ttu-id="95dd4-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95dd4-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dd4-115">-DefaultProfile</span></span>
<span data-ttu-id="95dd4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95dd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="95dd4-117">-MaxCapacity</span></span>
<span data-ttu-id="95dd4-118">Maximale Kapazität für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="95dd4-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="95dd4-119">-MinCapacity</span></span>
<span data-ttu-id="95dd4-120">Mindestkapazität für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="95dd4-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95dd4-121">-Confirm</span></span>
<span data-ttu-id="95dd4-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95dd4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95dd4-123">-WhatIf</span></span>
<span data-ttu-id="95dd4-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95dd4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95dd4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95dd4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95dd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dd4-126">CommonParameters</span></span>
<span data-ttu-id="95dd4-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95dd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dd4-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95dd4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dd4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95dd4-129">INPUTS</span></span>

### <span data-ttu-id="95dd4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95dd4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95dd4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95dd4-131">OUTPUTS</span></span>

### <span data-ttu-id="95dd4-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95dd4-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95dd4-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95dd4-133">NOTES</span></span>

## <span data-ttu-id="95dd4-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95dd4-134">RELATED LINKS</span></span>

[<span data-ttu-id="95dd4-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="95dd4-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="95dd4-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="95dd4-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="95dd4-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="95dd4-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
