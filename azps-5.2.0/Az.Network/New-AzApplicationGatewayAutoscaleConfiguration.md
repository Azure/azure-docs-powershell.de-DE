---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361050"
---
# <span data-ttu-id="76e81-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76e81-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="76e81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e81-102">SYNOPSIS</span></span>
<span data-ttu-id="76e81-103">Erstellt eine Konfiguration der automatischen Skala für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="76e81-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="76e81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76e81-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e81-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76e81-105">DESCRIPTION</span></span>
<span data-ttu-id="76e81-106">Das **Cmdlet "New-AzApplicationGatewayAutoscaleConfiguration"** erstellt die Autoskalenkonfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="76e81-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="76e81-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76e81-107">EXAMPLES</span></span>

### <span data-ttu-id="76e81-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76e81-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="76e81-109">Der erste Befehl erstellt eine Konfiguration der automatischen Skala mit einer Mindestkapazität von 3.</span><span class="sxs-lookup"><span data-stu-id="76e81-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="76e81-110">Der zweite Befehl erstellt ein Anwendungsgateway mit der Autoskalenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="76e81-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="76e81-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76e81-111">PARAMETERS</span></span>

### <span data-ttu-id="76e81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e81-112">-DefaultProfile</span></span>
<span data-ttu-id="76e81-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76e81-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76e81-114">-Max1</span><span class="sxs-lookup"><span data-stu-id="76e81-114">-MaxCapacity</span></span>
<span data-ttu-id="76e81-115">Maximale Kapazitätseinheiten, die für das Anwendungsgateway immer verfügbar [und in Rechnung gestellt] werden.</span><span class="sxs-lookup"><span data-stu-id="76e81-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="76e81-116">-Min1</span><span class="sxs-lookup"><span data-stu-id="76e81-116">-MinCapacity</span></span>
<span data-ttu-id="76e81-117">Minimale Kapazitätseinheiten, die für das Anwendungsgateway immer verfügbar [und in Rechnung gestellt] werden.</span><span class="sxs-lookup"><span data-stu-id="76e81-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="76e81-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76e81-118">-Confirm</span></span>
<span data-ttu-id="76e81-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76e81-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e81-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76e81-120">-WhatIf</span></span>
<span data-ttu-id="76e81-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76e81-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76e81-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76e81-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76e81-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e81-123">CommonParameters</span></span>
<span data-ttu-id="76e81-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e81-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e81-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e81-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e81-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76e81-126">INPUTS</span></span>

### <span data-ttu-id="76e81-127">Keine</span><span class="sxs-lookup"><span data-stu-id="76e81-127">None</span></span>

## <span data-ttu-id="76e81-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76e81-128">OUTPUTS</span></span>

### <span data-ttu-id="76e81-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76e81-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="76e81-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76e81-130">NOTES</span></span>

## <span data-ttu-id="76e81-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76e81-131">RELATED LINKS</span></span>

[<span data-ttu-id="76e81-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76e81-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="76e81-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76e81-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="76e81-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76e81-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
