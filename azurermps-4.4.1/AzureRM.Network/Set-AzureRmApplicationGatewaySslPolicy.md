---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 984556937e57d710b9f62d80f20f7f30955865ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481861"
---
# <span data-ttu-id="d06d1-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d06d1-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d06d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d06d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d06d1-103">Ändert die SSL-Richtlinie eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="d06d1-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d06d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d06d1-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d06d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d06d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d06d1-106">Das Cmdlet " **festlegen-AzureRmApplicationGatewaySslPolicy** " ändert die SSL-Richtlinie eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="d06d1-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="d06d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d06d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d06d1-108">1:</span><span class="sxs-lookup"><span data-stu-id="d06d1-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="d06d1-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d06d1-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="d06d1-110">Dieser zweite Befehl ändert die SSL-Richtlinie in einen vordefinierten Richtlinientypen und Richtliniennamen AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="d06d1-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="d06d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d06d1-111">PARAMETERS</span></span>

### <span data-ttu-id="d06d1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d06d1-112">-ApplicationGateway</span></span>
<span data-ttu-id="d06d1-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d06d1-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d06d1-114">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="d06d1-114">-CipherSuite</span></span>
<span data-ttu-id="d06d1-115">SSL-Verschlüsselungs Pakete werden in der angegebenen Reihenfolge für Application Gateway aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d06d1-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="d06d1-116">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="d06d1-116">-DisabledSslProtocols</span></span>
<span data-ttu-id="d06d1-117">Gibt an, welche Protokolle deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d06d1-117">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="d06d1-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d06d1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d06d1-119">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="d06d1-119">TLSv1_0</span></span> 
- <span data-ttu-id="d06d1-120">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="d06d1-120">TLSv1_1</span></span> 
- <span data-ttu-id="d06d1-121">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="d06d1-121">TLSv1_2</span></span>

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

### <span data-ttu-id="d06d1-122">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="d06d1-122">-MinProtocolVersion</span></span>
<span data-ttu-id="d06d1-123">Minimale Version des SSL-Protokolls, das auf dem Anwendungs-Gateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="d06d1-123">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="d06d1-124">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="d06d1-124">-PolicyName</span></span>
<span data-ttu-id="d06d1-125">Name der vordefinierten SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d06d1-125">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="d06d1-126">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="d06d1-126">-PolicyType</span></span>
<span data-ttu-id="d06d1-127">Art der SSL-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d06d1-127">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="d06d1-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d06d1-128">-Confirm</span></span>
<span data-ttu-id="d06d1-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d06d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06d1-130">-WhatIf</span></span>
<span data-ttu-id="d06d1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d06d1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06d1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d06d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06d1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06d1-133">-DefaultProfile</span></span>
<span data-ttu-id="d06d1-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d06d1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06d1-135">CommonParameters</span></span>
<span data-ttu-id="d06d1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06d1-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06d1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06d1-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d06d1-138">INPUTS</span></span>

### <span data-ttu-id="d06d1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d06d1-139">System.String</span></span>

## <span data-ttu-id="d06d1-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d06d1-140">OUTPUTS</span></span>

### <span data-ttu-id="d06d1-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d06d1-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d06d1-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d06d1-142">NOTES</span></span>
* <span data-ttu-id="d06d1-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d06d1-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d06d1-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d06d1-144">RELATED LINKS</span></span>

[<span data-ttu-id="d06d1-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d06d1-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="d06d1-146">Neu – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d06d1-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


