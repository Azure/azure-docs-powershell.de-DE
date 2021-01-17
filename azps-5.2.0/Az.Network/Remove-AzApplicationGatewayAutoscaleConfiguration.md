---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292607"
---
# <span data-ttu-id="6dfc5-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dfc5-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6dfc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfc5-103">Entfernt die Konfiguration der automatischen Skala von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="6dfc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dfc5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dfc5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dfc5-105">DESCRIPTION</span></span>
<span data-ttu-id="6dfc5-106">Das **Cmdlet "Remove-AzApplicationGatewayAutoscaleConfiguration"** entfernt die Autoskalenkonfiguration aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="6dfc5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6dfc5-107">EXAMPLES</span></span>

### <span data-ttu-id="6dfc5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6dfc5-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6dfc5-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="6dfc5-110">Mit dem zweiten Befehl wird die Konfiguration der automatischen Skala vom Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="6dfc5-111">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6dfc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dfc5-112">PARAMETERS</span></span>

### <span data-ttu-id="6dfc5-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfc5-113">-ApplicationGateway</span></span>
<span data-ttu-id="6dfc5-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfc5-114">The applicationGateway</span></span>

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

### <span data-ttu-id="6dfc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfc5-115">-DefaultProfile</span></span>
<span data-ttu-id="6dfc5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfc5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6dfc5-117">-Force</span></span>
<span data-ttu-id="6dfc5-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6dfc5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dfc5-119">-Confirm</span></span>
<span data-ttu-id="6dfc5-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dfc5-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6dfc5-121">-WhatIf</span></span>
<span data-ttu-id="6dfc5-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dfc5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dfc5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfc5-124">CommonParameters</span></span>
<span data-ttu-id="6dfc5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfc5-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dfc5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfc5-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6dfc5-127">INPUTS</span></span>

### <span data-ttu-id="6dfc5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfc5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dfc5-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6dfc5-129">OUTPUTS</span></span>

### <span data-ttu-id="6dfc5-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfc5-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dfc5-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6dfc5-131">NOTES</span></span>

## <span data-ttu-id="6dfc5-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6dfc5-132">RELATED LINKS</span></span>

[<span data-ttu-id="6dfc5-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dfc5-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6dfc5-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dfc5-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6dfc5-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dfc5-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
