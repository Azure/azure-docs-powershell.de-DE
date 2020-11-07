---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848767"
---
# <span data-ttu-id="b3e8f-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3e8f-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b3e8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e8f-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e8f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3e8f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e8f-106">Das Cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** entfernt ein Authentifizierungszertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b3e8f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e8f-108">1:</span><span class="sxs-lookup"><span data-stu-id="b3e8f-108">1:</span></span>
```

```

## <span data-ttu-id="b3e8f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3e8f-109">PARAMETERS</span></span>

### <span data-ttu-id="b3e8f-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3e8f-110">-ApplicationGateway</span></span>
<span data-ttu-id="b3e8f-111">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e8f-112">-DefaultProfile</span></span>
<span data-ttu-id="b3e8f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e8f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b3e8f-114">-Name</span></span>
<span data-ttu-id="b3e8f-115">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e8f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3e8f-116">-Confirm</span></span>
<span data-ttu-id="b3e8f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e8f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e8f-118">-WhatIf</span></span>
<span data-ttu-id="b3e8f-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e8f-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e8f-121">CommonParameters</span></span>
<span data-ttu-id="b3e8f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e8f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e8f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e8f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3e8f-124">INPUTS</span></span>

### <span data-ttu-id="b3e8f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e8f-125">System.String</span></span>

## <span data-ttu-id="b3e8f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3e8f-126">OUTPUTS</span></span>

### <span data-ttu-id="b3e8f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3e8f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b3e8f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3e8f-128">NOTES</span></span>
* <span data-ttu-id="b3e8f-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b3e8f-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b3e8f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3e8f-130">RELATED LINKS</span></span>

[<span data-ttu-id="b3e8f-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3e8f-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3e8f-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3e8f-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3e8f-133">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3e8f-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3e8f-134">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3e8f-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


