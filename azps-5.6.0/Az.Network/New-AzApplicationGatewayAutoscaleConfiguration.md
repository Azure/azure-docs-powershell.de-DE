---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e849b109ba1f1fd43ca960d56581357729f5c344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947795"
---
# <span data-ttu-id="8b1df-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1df-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="8b1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b1df-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1df-103">Erstellt eine Konfiguration für die automatische Skalierung für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8b1df-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="8b1df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b1df-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b1df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b1df-105">DESCRIPTION</span></span>
<span data-ttu-id="8b1df-106">Das **Cmdlet New-AzApplicationGatewayAutoscaleConfiguration** erstellt die Konfiguration automatischer Skalierung für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8b1df-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="8b1df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b1df-107">EXAMPLES</span></span>

### <span data-ttu-id="8b1df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b1df-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="8b1df-109">Mit dem ersten Befehl wird eine Konfiguration für die automatische Skalierung mit einer Mindestkapazität von 3 erstellt.</span><span class="sxs-lookup"><span data-stu-id="8b1df-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="8b1df-110">Mit dem zweiten Befehl wird ein Anwendungsgateway mit der Konfiguration der automatischen Skalierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="8b1df-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="8b1df-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8b1df-111">PARAMETERS</span></span>

### <span data-ttu-id="8b1df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1df-112">-DefaultProfile</span></span>
<span data-ttu-id="8b1df-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b1df-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b1df-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="8b1df-114">-MaxCapacity</span></span>
<span data-ttu-id="8b1df-115">Maximale Kapazitätseinheiten, die für das Anwendungsgateway immer verfügbar [und in Rechnung gestellt] werden.</span><span class="sxs-lookup"><span data-stu-id="8b1df-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="8b1df-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="8b1df-116">-MinCapacity</span></span>
<span data-ttu-id="8b1df-117">Mindestkapazitätseinheiten, die immer für das Anwendungsgateway verfügbar [und in Rechnung gestellt] werden.</span><span class="sxs-lookup"><span data-stu-id="8b1df-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="8b1df-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b1df-118">-Confirm</span></span>
<span data-ttu-id="8b1df-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b1df-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b1df-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b1df-120">-WhatIf</span></span>
<span data-ttu-id="8b1df-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b1df-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b1df-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b1df-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b1df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1df-123">CommonParameters</span></span>
<span data-ttu-id="8b1df-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b1df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1df-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b1df-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1df-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b1df-126">INPUTS</span></span>

### <span data-ttu-id="8b1df-127">Keine</span><span class="sxs-lookup"><span data-stu-id="8b1df-127">None</span></span>

## <span data-ttu-id="8b1df-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b1df-128">OUTPUTS</span></span>

### <span data-ttu-id="8b1df-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1df-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="8b1df-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8b1df-130">NOTES</span></span>

## <span data-ttu-id="8b1df-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8b1df-131">RELATED LINKS</span></span>

[<span data-ttu-id="8b1df-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1df-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8b1df-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1df-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="8b1df-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1df-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
