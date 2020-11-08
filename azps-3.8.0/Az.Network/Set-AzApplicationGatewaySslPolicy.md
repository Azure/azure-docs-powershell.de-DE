---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 00a12e5ad18bd3b8072d8393dd283a870f8b9435
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995605"
---
# <span data-ttu-id="998d5-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="998d5-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="998d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="998d5-102">SYNOPSIS</span></span>
<span data-ttu-id="998d5-103">Ändert die SSL-Richtlinie eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="998d5-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="998d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="998d5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="998d5-105">DESCRIPTION</span></span>
<span data-ttu-id="998d5-106">Das Cmdlet " **festlegen-AzApplicationGatewaySslPolicy** " ändert die SSL-Richtlinie eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="998d5-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="998d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="998d5-107">EXAMPLES</span></span>

### <span data-ttu-id="998d5-108">1:</span><span class="sxs-lookup"><span data-stu-id="998d5-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="998d5-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="998d5-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="998d5-110">Dieser zweite Befehl ändert die SSL-Richtlinie in einen vordefinierten Richtlinientypen und Richtliniennamen AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="998d5-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="998d5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="998d5-111">PARAMETERS</span></span>

### <span data-ttu-id="998d5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="998d5-112">-ApplicationGateway</span></span>
<span data-ttu-id="998d5-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="998d5-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="998d5-114">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="998d5-114">-CipherSuite</span></span>
<span data-ttu-id="998d5-115">SSL-Verschlüsselungs Pakete werden in der angegebenen Reihenfolge für Application Gateway aktiviert.</span><span class="sxs-lookup"><span data-stu-id="998d5-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998d5-116">-DefaultProfile</span></span>
<span data-ttu-id="998d5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="998d5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998d5-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="998d5-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="998d5-119">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="998d5-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="998d5-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="998d5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="998d5-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="998d5-121">TLSv1_0</span></span> 
- <span data-ttu-id="998d5-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="998d5-122">TLSv1_1</span></span> 
- <span data-ttu-id="998d5-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="998d5-123">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="998d5-124">-MinProtocolVersion</span></span>
<span data-ttu-id="998d5-125">Minimale Version des SSL-Protokolls, das auf dem Anwendungs-Gateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="998d5-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-126">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="998d5-126">-PolicyName</span></span>
<span data-ttu-id="998d5-127">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="998d5-127">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="998d5-128">-PolicyType</span></span>
<span data-ttu-id="998d5-129">Art der SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="998d5-129">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="998d5-130">-Confirm</span></span>
<span data-ttu-id="998d5-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="998d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998d5-132">-WhatIf</span></span>
<span data-ttu-id="998d5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="998d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998d5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="998d5-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998d5-135">CommonParameters</span></span>
<span data-ttu-id="998d5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998d5-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998d5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998d5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="998d5-138">INPUTS</span></span>

### <span data-ttu-id="998d5-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="998d5-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="998d5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="998d5-140">OUTPUTS</span></span>

### <span data-ttu-id="998d5-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="998d5-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="998d5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="998d5-142">NOTES</span></span>
* <span data-ttu-id="998d5-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="998d5-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="998d5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="998d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="998d5-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="998d5-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="998d5-146">Neu – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="998d5-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


