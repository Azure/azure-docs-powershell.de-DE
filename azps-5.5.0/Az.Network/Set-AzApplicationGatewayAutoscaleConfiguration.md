---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146620"
---
# <span data-ttu-id="7ab35-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab35-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7ab35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab35-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab35-103">Aktualisiert die Autoskalierungskonfiguration eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="7ab35-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="7ab35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ab35-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab35-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ab35-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab35-106">Das **Cmdlet "Set-AzApplicationGatewayAutoscaleConfiguration"** ändert die vorhandene Autoskalenkonfiguration eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="7ab35-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="7ab35-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ab35-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab35-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ab35-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7ab35-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="7ab35-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7ab35-110">Mit dem zweiten Befehl wird die Konfiguration der Automatischskala vom Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ab35-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="7ab35-111">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ab35-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7ab35-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ab35-112">PARAMETERS</span></span>

### <span data-ttu-id="7ab35-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab35-113">-ApplicationGateway</span></span>
<span data-ttu-id="7ab35-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab35-114">The applicationGateway</span></span>

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

### <span data-ttu-id="7ab35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab35-115">-DefaultProfile</span></span>
<span data-ttu-id="7ab35-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ab35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab35-117">-Max1</span><span class="sxs-lookup"><span data-stu-id="7ab35-117">-MaxCapacity</span></span>
<span data-ttu-id="7ab35-118">Maximale Kapazität für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7ab35-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="7ab35-119">-Min1</span><span class="sxs-lookup"><span data-stu-id="7ab35-119">-MinCapacity</span></span>
<span data-ttu-id="7ab35-120">Mindestkapazität für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7ab35-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="7ab35-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ab35-121">-Confirm</span></span>
<span data-ttu-id="7ab35-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ab35-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab35-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7ab35-123">-WhatIf</span></span>
<span data-ttu-id="7ab35-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ab35-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab35-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ab35-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab35-126">CommonParameters</span></span>
<span data-ttu-id="7ab35-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab35-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab35-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab35-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ab35-129">INPUTS</span></span>

### <span data-ttu-id="7ab35-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab35-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ab35-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ab35-131">OUTPUTS</span></span>

### <span data-ttu-id="7ab35-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab35-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ab35-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ab35-133">NOTES</span></span>

## <span data-ttu-id="7ab35-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ab35-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ab35-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab35-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="7ab35-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab35-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="7ab35-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ab35-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
