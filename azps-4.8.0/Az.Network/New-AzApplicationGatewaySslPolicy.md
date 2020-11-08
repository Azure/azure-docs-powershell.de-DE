---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009110"
---
# <span data-ttu-id="00685-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="00685-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="00685-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00685-102">SYNOPSIS</span></span>
<span data-ttu-id="00685-103">Erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="00685-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="00685-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00685-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00685-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00685-105">DESCRIPTION</span></span>
<span data-ttu-id="00685-106">Das Cmdlet **New-AzApplicationGatewaySslPolicy** erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="00685-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="00685-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00685-107">EXAMPLES</span></span>

### <span data-ttu-id="00685-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00685-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="00685-109">Mit diesem Befehl wird eine benutzerdefinierte Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="00685-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="00685-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00685-110">PARAMETERS</span></span>

### <span data-ttu-id="00685-111">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="00685-111">-CipherSuite</span></span>
<span data-ttu-id="00685-112">SSL-Verschlüsselungs Pakete werden in der angegebenen Reihenfolge für Application Gateway aktiviert.</span><span class="sxs-lookup"><span data-stu-id="00685-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="00685-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00685-113">-DefaultProfile</span></span>
<span data-ttu-id="00685-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00685-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00685-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="00685-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="00685-116">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="00685-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="00685-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="00685-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00685-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="00685-118">TLSv1_0</span></span> 
- <span data-ttu-id="00685-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="00685-119">TLSv1_1</span></span> 
- <span data-ttu-id="00685-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="00685-120">TLSv1_2</span></span>

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

### <span data-ttu-id="00685-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="00685-121">-MinProtocolVersion</span></span>
<span data-ttu-id="00685-122">Minimale Version des SSL-Protokolls, das auf dem Anwendungs-Gateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="00685-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="00685-123">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="00685-123">-PolicyName</span></span>
<span data-ttu-id="00685-124">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="00685-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="00685-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="00685-125">-PolicyType</span></span>
<span data-ttu-id="00685-126">Art der SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="00685-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="00685-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00685-127">-Confirm</span></span>
<span data-ttu-id="00685-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00685-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00685-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00685-129">-WhatIf</span></span>
<span data-ttu-id="00685-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00685-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00685-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00685-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00685-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00685-132">CommonParameters</span></span>
<span data-ttu-id="00685-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00685-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00685-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00685-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00685-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00685-135">INPUTS</span></span>

### <span data-ttu-id="00685-136">Keine</span><span class="sxs-lookup"><span data-stu-id="00685-136">None</span></span>

## <span data-ttu-id="00685-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00685-137">OUTPUTS</span></span>

### <span data-ttu-id="00685-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="00685-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="00685-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="00685-139">NOTES</span></span>
* <span data-ttu-id="00685-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="00685-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="00685-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00685-141">RELATED LINKS</span></span>

[<span data-ttu-id="00685-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="00685-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="00685-143">Satz-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="00685-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


