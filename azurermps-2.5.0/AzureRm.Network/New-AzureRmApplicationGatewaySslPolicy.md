---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 6c28665f35a7422a731aefd4ccf1c4ecabc549d4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848428"
---
# <span data-ttu-id="6c645-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c645-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6c645-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c645-102">SYNOPSIS</span></span>
<span data-ttu-id="6c645-103">Erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6c645-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c645-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c645-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c645-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c645-105">DESCRIPTION</span></span>
<span data-ttu-id="6c645-106">Das Cmdlet **New-AzureRmApplicationGatewaySslPolicy** erstellt eine SSL-Richtlinie für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6c645-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="6c645-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c645-107">EXAMPLES</span></span>

### <span data-ttu-id="6c645-108">1:</span><span class="sxs-lookup"><span data-stu-id="6c645-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="6c645-109">Mit diesem Befehl wird eine benutzerdefinierte Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c645-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="6c645-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c645-110">PARAMETERS</span></span>

### <span data-ttu-id="6c645-111">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="6c645-111">-CipherSuite</span></span>
<span data-ttu-id="6c645-112">SSL-Verschlüsselungs Pakete werden in der angegebenen Reihenfolge für Application Gateway aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c645-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="6c645-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c645-113">-DefaultProfile</span></span>
<span data-ttu-id="6c645-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c645-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="6c645-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="6c645-116">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="6c645-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="6c645-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6c645-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c645-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="6c645-118">TLSv1_0</span></span> 
- <span data-ttu-id="6c645-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="6c645-119">TLSv1_1</span></span> 
- <span data-ttu-id="6c645-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="6c645-120">TLSv1_2</span></span>

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

### <span data-ttu-id="6c645-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="6c645-121">-MinProtocolVersion</span></span>
<span data-ttu-id="6c645-122">Minimale Version des SSL-Protokolls, das auf dem Anwendungs-Gateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="6c645-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-123">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="6c645-123">-PolicyName</span></span>
<span data-ttu-id="6c645-124">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6c645-124">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="6c645-125">-PolicyType</span></span>
<span data-ttu-id="6c645-126">Art der SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6c645-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c645-127">-Confirm</span></span>
<span data-ttu-id="6c645-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c645-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c645-129">-WhatIf</span></span>
<span data-ttu-id="6c645-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c645-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c645-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c645-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c645-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c645-132">CommonParameters</span></span>
<span data-ttu-id="6c645-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c645-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c645-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c645-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c645-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c645-135">INPUTS</span></span>

### <span data-ttu-id="6c645-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c645-136">System.String</span></span>

## <span data-ttu-id="6c645-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c645-137">OUTPUTS</span></span>

### <span data-ttu-id="6c645-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c645-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6c645-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c645-139">NOTES</span></span>
* <span data-ttu-id="6c645-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="6c645-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6c645-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c645-141">RELATED LINKS</span></span>

[<span data-ttu-id="6c645-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c645-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6c645-143">Satz-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c645-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


