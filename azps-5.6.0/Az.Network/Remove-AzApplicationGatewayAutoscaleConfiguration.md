---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e6321125958b872d15f60bbe433819c4c6f1d7ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950123"
---
# <span data-ttu-id="b70f9-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b70f9-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b70f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b70f9-103">Entfernt die Konfiguration der automatischen Skalierung aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b70f9-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="b70f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b70f9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b70f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b70f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b70f9-106">Das **Cmdlet Remove-AzApplicationGatewayAutoscaleConfiguration** entfernt die Konfiguration der automatischen Skalierung aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b70f9-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="b70f9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b70f9-107">EXAMPLES</span></span>

### <span data-ttu-id="b70f9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b70f9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b70f9-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b70f9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b70f9-110">Mit dem zweiten Befehl wird die Konfiguration der automatischen Skalierung aus dem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="b70f9-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="b70f9-111">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b70f9-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b70f9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b70f9-112">PARAMETERS</span></span>

### <span data-ttu-id="b70f9-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b70f9-113">-ApplicationGateway</span></span>
<span data-ttu-id="b70f9-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b70f9-114">The applicationGateway</span></span>

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

### <span data-ttu-id="b70f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70f9-115">-DefaultProfile</span></span>
<span data-ttu-id="b70f9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b70f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70f9-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b70f9-117">-Force</span></span>
<span data-ttu-id="b70f9-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="b70f9-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70f9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b70f9-119">-Confirm</span></span>
<span data-ttu-id="b70f9-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b70f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b70f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b70f9-121">-WhatIf</span></span>
<span data-ttu-id="b70f9-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b70f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b70f9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b70f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b70f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70f9-124">CommonParameters</span></span>
<span data-ttu-id="b70f9-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70f9-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70f9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b70f9-127">INPUTS</span></span>

### <span data-ttu-id="b70f9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b70f9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b70f9-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b70f9-129">OUTPUTS</span></span>

### <span data-ttu-id="b70f9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b70f9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b70f9-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b70f9-131">NOTES</span></span>

## <span data-ttu-id="b70f9-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b70f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b70f9-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b70f9-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="b70f9-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b70f9-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="b70f9-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b70f9-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
