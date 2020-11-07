---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841232"
---
# <span data-ttu-id="d167a-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d167a-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d167a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d167a-102">SYNOPSIS</span></span>
<span data-ttu-id="d167a-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d167a-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="d167a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d167a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d167a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d167a-105">DESCRIPTION</span></span>
<span data-ttu-id="d167a-106">Das Cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** entfernt ein Authentifizierungszertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d167a-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="d167a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d167a-107">EXAMPLES</span></span>

### <span data-ttu-id="d167a-108">1:</span><span class="sxs-lookup"><span data-stu-id="d167a-108">1:</span></span>
```

```

## <span data-ttu-id="d167a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d167a-109">PARAMETERS</span></span>

### <span data-ttu-id="d167a-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d167a-110">-ApplicationGateway</span></span>
<span data-ttu-id="d167a-111">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="d167a-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="d167a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d167a-112">-DefaultProfile</span></span>
<span data-ttu-id="d167a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d167a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d167a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d167a-114">-Name</span></span>
<span data-ttu-id="d167a-115">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d167a-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d167a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d167a-116">-Confirm</span></span>
<span data-ttu-id="d167a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d167a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d167a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d167a-118">-WhatIf</span></span>
<span data-ttu-id="d167a-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d167a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d167a-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d167a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d167a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d167a-121">CommonParameters</span></span>
<span data-ttu-id="d167a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d167a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d167a-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d167a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d167a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d167a-124">INPUTS</span></span>

### <span data-ttu-id="d167a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d167a-125">System.String</span></span>

## <span data-ttu-id="d167a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d167a-126">OUTPUTS</span></span>

### <span data-ttu-id="d167a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d167a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d167a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d167a-128">NOTES</span></span>
* <span data-ttu-id="d167a-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d167a-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d167a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d167a-130">RELATED LINKS</span></span>

[<span data-ttu-id="d167a-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d167a-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d167a-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d167a-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d167a-133">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d167a-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d167a-134">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d167a-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


