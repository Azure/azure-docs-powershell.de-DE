---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505353"
---
# <span data-ttu-id="eaebd-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="eaebd-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="eaebd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eaebd-102">SYNOPSIS</span></span>
<span data-ttu-id="eaebd-103">Erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="eaebd-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaebd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaebd-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaebd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaebd-105">DESCRIPTION</span></span>
<span data-ttu-id="eaebd-106">Das Cmdlet **New-AzureRmApplicationGatewaySslPolicy** erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="eaebd-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="eaebd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaebd-107">EXAMPLES</span></span>

### <span data-ttu-id="eaebd-108">1:</span><span class="sxs-lookup"><span data-stu-id="eaebd-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="eaebd-109">Mit diesem Befehl wird eine benutzerdefinierte Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="eaebd-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="eaebd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaebd-110">PARAMETERS</span></span>

### <span data-ttu-id="eaebd-111">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="eaebd-111">-CipherSuite</span></span>
<span data-ttu-id="eaebd-112">SSL-Verschlüsselungs Pakete werden in der angegebenen Reihenfolge für Application Gateway aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eaebd-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaebd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaebd-113">-DefaultProfile</span></span>
<span data-ttu-id="eaebd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eaebd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaebd-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="eaebd-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="eaebd-116">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="eaebd-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="eaebd-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eaebd-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eaebd-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="eaebd-118">TLSv1_0</span></span> 
- <span data-ttu-id="eaebd-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="eaebd-119">TLSv1_1</span></span> 
- <span data-ttu-id="eaebd-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="eaebd-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaebd-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="eaebd-121">-MinProtocolVersion</span></span>
<span data-ttu-id="eaebd-122">Minimale Version des SSL-Protokolls, das auf dem Anwendungs-Gateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="eaebd-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="eaebd-123">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="eaebd-123">-PolicyName</span></span>
<span data-ttu-id="eaebd-124">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="eaebd-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="eaebd-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="eaebd-125">-PolicyType</span></span>
<span data-ttu-id="eaebd-126">Art der SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="eaebd-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="eaebd-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eaebd-127">-Confirm</span></span>
<span data-ttu-id="eaebd-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eaebd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaebd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaebd-129">-WhatIf</span></span>
<span data-ttu-id="eaebd-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaebd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaebd-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eaebd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaebd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaebd-132">CommonParameters</span></span>
<span data-ttu-id="eaebd-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaebd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaebd-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaebd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaebd-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eaebd-135">INPUTS</span></span>

### <span data-ttu-id="eaebd-136">Keine</span><span class="sxs-lookup"><span data-stu-id="eaebd-136">None</span></span>

## <span data-ttu-id="eaebd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eaebd-137">OUTPUTS</span></span>

### <span data-ttu-id="eaebd-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="eaebd-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="eaebd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="eaebd-139">NOTES</span></span>
* <span data-ttu-id="eaebd-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="eaebd-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eaebd-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eaebd-141">RELATED LINKS</span></span>

[<span data-ttu-id="eaebd-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="eaebd-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="eaebd-143">Satz-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="eaebd-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


