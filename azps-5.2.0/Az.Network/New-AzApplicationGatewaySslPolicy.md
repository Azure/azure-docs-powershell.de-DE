---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305683"
---
# <span data-ttu-id="c220a-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c220a-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c220a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c220a-102">SYNOPSIS</span></span>
<span data-ttu-id="c220a-103">Erstellt eine "SSL"-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c220a-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c220a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c220a-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c220a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c220a-105">DESCRIPTION</span></span>
<span data-ttu-id="c220a-106">Das **Cmdlet "New-AzApplicationGatewaySslPolicy"** erstellt eine "SSL-Richtlinie" für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c220a-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c220a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c220a-107">EXAMPLES</span></span>

### <span data-ttu-id="c220a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c220a-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="c220a-109">Mit diesem Befehl wird eine benutzerdefinierte Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="c220a-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="c220a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c220a-110">PARAMETERS</span></span>

### <span data-ttu-id="c220a-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c220a-111">-CipherSuite</span></span>
<span data-ttu-id="c220a-112">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="c220a-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="c220a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c220a-113">-DefaultProfile</span></span>
<span data-ttu-id="c220a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c220a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c220a-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="c220a-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="c220a-116">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c220a-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="c220a-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="c220a-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c220a-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="c220a-118">TLSv1_0</span></span> 
- <span data-ttu-id="c220a-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="c220a-119">TLSv1_1</span></span> 
- <span data-ttu-id="c220a-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="c220a-120">TLSv1_2</span></span>

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

### <span data-ttu-id="c220a-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="c220a-121">-MinProtocolVersion</span></span>
<span data-ttu-id="c220a-122">Mindestversion des ssl-Protokolls, die auf dem Anwendungsgateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="c220a-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="c220a-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c220a-123">-PolicyName</span></span>
<span data-ttu-id="c220a-124">Name der vordefinierten Richtlinie in Ssl</span><span class="sxs-lookup"><span data-stu-id="c220a-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="c220a-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="c220a-125">-PolicyType</span></span>
<span data-ttu-id="c220a-126">Typ der Ssl-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c220a-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="c220a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c220a-127">-Confirm</span></span>
<span data-ttu-id="c220a-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c220a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c220a-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c220a-129">-WhatIf</span></span>
<span data-ttu-id="c220a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c220a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c220a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c220a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c220a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c220a-132">CommonParameters</span></span>
<span data-ttu-id="c220a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c220a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c220a-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c220a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c220a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c220a-135">INPUTS</span></span>

### <span data-ttu-id="c220a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="c220a-136">None</span></span>

## <span data-ttu-id="c220a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c220a-137">OUTPUTS</span></span>

### <span data-ttu-id="c220a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c220a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c220a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c220a-139">NOTES</span></span>
* <span data-ttu-id="c220a-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="c220a-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c220a-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c220a-141">RELATED LINKS</span></span>

[<span data-ttu-id="c220a-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c220a-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c220a-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c220a-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


