---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 31b9bd5e0db4f4fd17808ea46f1f3a3d6476c5e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821443"
---
# <span data-ttu-id="5024c-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5024c-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5024c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5024c-102">SYNOPSIS</span></span>
<span data-ttu-id="5024c-103">Entfernt die AutoScale-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5024c-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="5024c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5024c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5024c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5024c-105">DESCRIPTION</span></span>
<span data-ttu-id="5024c-106">Das Cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** entfernt die Konfiguration von AutoScale aus einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="5024c-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="5024c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5024c-107">EXAMPLES</span></span>

### <span data-ttu-id="5024c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5024c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="5024c-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="5024c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="5024c-110">Der zweite Befehl entfernt die AutoScale-Konfiguration aus dem Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5024c-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="5024c-111">Der dritte Befehl aktualisiert das Anwendungsgateway auf Azure.</span><span class="sxs-lookup"><span data-stu-id="5024c-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="5024c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5024c-112">PARAMETERS</span></span>

### <span data-ttu-id="5024c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5024c-113">-ApplicationGateway</span></span>
<span data-ttu-id="5024c-114">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5024c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="5024c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5024c-115">-DefaultProfile</span></span>
<span data-ttu-id="5024c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5024c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5024c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5024c-117">-Force</span></span>
<span data-ttu-id="5024c-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5024c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5024c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5024c-119">-Confirm</span></span>
<span data-ttu-id="5024c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5024c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5024c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5024c-121">-WhatIf</span></span>
<span data-ttu-id="5024c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5024c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5024c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5024c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5024c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5024c-124">CommonParameters</span></span>
<span data-ttu-id="5024c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5024c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5024c-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5024c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5024c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5024c-127">INPUTS</span></span>

### <span data-ttu-id="5024c-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5024c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5024c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5024c-129">OUTPUTS</span></span>

### <span data-ttu-id="5024c-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5024c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5024c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5024c-131">NOTES</span></span>

## <span data-ttu-id="5024c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5024c-132">RELATED LINKS</span></span>

[<span data-ttu-id="5024c-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5024c-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5024c-134">Neu – AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5024c-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5024c-135">Satz-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5024c-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
