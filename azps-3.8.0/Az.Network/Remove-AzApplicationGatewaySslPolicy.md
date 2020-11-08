---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995039"
---
# <span data-ttu-id="4172e-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4172e-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4172e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4172e-102">SYNOPSIS</span></span>
<span data-ttu-id="4172e-103">Entfernt eine SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4172e-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="4172e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4172e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4172e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4172e-105">DESCRIPTION</span></span>
<span data-ttu-id="4172e-106">Das Remove-AzApplicationGatewaySslPolicy-Cmdlet entfernt die SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4172e-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="4172e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4172e-107">EXAMPLES</span></span>

### <span data-ttu-id="4172e-108">Beispiel 1: Entfernen einer SSL-Richtlinie von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="4172e-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="4172e-109">Dieser Befehl entfernt die SSL-Richtlinie aus dem Anwendungsgateway mit dem Namen ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="4172e-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="4172e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4172e-110">PARAMETERS</span></span>

### <span data-ttu-id="4172e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4172e-111">-ApplicationGateway</span></span>
<span data-ttu-id="4172e-112">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die SSL-Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="4172e-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="4172e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4172e-113">-DefaultProfile</span></span>
<span data-ttu-id="4172e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4172e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4172e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4172e-115">-Force</span></span>
<span data-ttu-id="4172e-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4172e-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4172e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4172e-117">-Confirm</span></span>
<span data-ttu-id="4172e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4172e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4172e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4172e-119">-WhatIf</span></span>
<span data-ttu-id="4172e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4172e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4172e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4172e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4172e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4172e-122">CommonParameters</span></span>
<span data-ttu-id="4172e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4172e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4172e-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4172e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4172e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4172e-125">INPUTS</span></span>

### <span data-ttu-id="4172e-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4172e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4172e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4172e-127">OUTPUTS</span></span>

### <span data-ttu-id="4172e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4172e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4172e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4172e-129">NOTES</span></span>
<span data-ttu-id="4172e-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="4172e-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4172e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4172e-131">RELATED LINKS</span></span>

[<span data-ttu-id="4172e-132">Satz-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4172e-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4172e-133">Neu – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4172e-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4172e-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4172e-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

