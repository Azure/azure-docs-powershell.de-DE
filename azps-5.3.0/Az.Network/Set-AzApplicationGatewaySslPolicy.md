---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 06b8f7bdaea4ebf11ff901fbe53be94f74c9bba7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472192"
---
# <span data-ttu-id="2fe3a-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2fe3a-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2fe3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe3a-103">Ändert die "SSL"-Richtlinie eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="2fe3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fe3a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fe3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fe3a-105">DESCRIPTION</span></span>
<span data-ttu-id="2fe3a-106">Das **Cmdlet "Set-AzApplicationGatewaySslPolicy"** ändert die "SSL"-Richtlinie eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="2fe3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fe3a-107">EXAMPLES</span></span>

### <span data-ttu-id="2fe3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fe3a-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="2fe3a-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2fe3a-110">Mit diesem zweiten Befehl wird die ssl-Richtlinie in den Richtlinientyp "Vordefinierte Richtlinie" und den Richtliniennamen "AppGwSslPolicy20170401" geändert.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="2fe3a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fe3a-111">PARAMETERS</span></span>

### <span data-ttu-id="2fe3a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fe3a-112">-ApplicationGateway</span></span>
<span data-ttu-id="2fe3a-113">Gibt das Anwendungsgateway der ssl-Richtlinie an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2fe3a-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="2fe3a-114">-CipherSuite</span></span>
<span data-ttu-id="2fe3a-115">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="2fe3a-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="2fe3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe3a-116">-DefaultProfile</span></span>
<span data-ttu-id="2fe3a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe3a-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="2fe3a-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="2fe3a-119">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="2fe3a-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="2fe3a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fe3a-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="2fe3a-121">TLSv1_0</span></span> 
- <span data-ttu-id="2fe3a-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="2fe3a-122">TLSv1_1</span></span> 
- <span data-ttu-id="2fe3a-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="2fe3a-123">TLSv1_2</span></span>

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

### <span data-ttu-id="2fe3a-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="2fe3a-124">-MinProtocolVersion</span></span>
<span data-ttu-id="2fe3a-125">Mindestversion des ssl-Protokolls, die auf dem Anwendungsgateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="2fe3a-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="2fe3a-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="2fe3a-126">-PolicyName</span></span>
<span data-ttu-id="2fe3a-127">Name der vordefinierten Richtlinie in Ssl</span><span class="sxs-lookup"><span data-stu-id="2fe3a-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="2fe3a-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="2fe3a-128">-PolicyType</span></span>
<span data-ttu-id="2fe3a-129">Typ der Ssl-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2fe3a-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="2fe3a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fe3a-130">-Confirm</span></span>
<span data-ttu-id="2fe3a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe3a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fe3a-132">-WhatIf</span></span>
<span data-ttu-id="2fe3a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe3a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe3a-135">CommonParameters</span></span>
<span data-ttu-id="2fe3a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe3a-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe3a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe3a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe3a-138">INPUTS</span></span>

### <span data-ttu-id="2fe3a-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fe3a-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fe3a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe3a-140">OUTPUTS</span></span>

### <span data-ttu-id="2fe3a-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fe3a-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fe3a-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fe3a-142">NOTES</span></span>
* <span data-ttu-id="2fe3a-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="2fe3a-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2fe3a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fe3a-144">RELATED LINKS</span></span>

[<span data-ttu-id="2fe3a-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2fe3a-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="2fe3a-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2fe3a-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


