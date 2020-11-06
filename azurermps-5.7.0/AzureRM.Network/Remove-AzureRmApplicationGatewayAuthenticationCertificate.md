---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 013010e0b679c69a6fa5c6d8341879b95bd55692
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503714"
---
# <span data-ttu-id="f2b81-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f2b81-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f2b81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2b81-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b81-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f2b81-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2b81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2b81-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2b81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2b81-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b81-106">Das Cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** entfernt ein Authentifizierungszertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f2b81-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="f2b81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2b81-107">EXAMPLES</span></span>

## <span data-ttu-id="f2b81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2b81-108">PARAMETERS</span></span>

### <span data-ttu-id="f2b81-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2b81-109">-ApplicationGateway</span></span>
<span data-ttu-id="f2b81-110">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2b81-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="f2b81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b81-111">-DefaultProfile</span></span>
<span data-ttu-id="f2b81-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2b81-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b81-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f2b81-113">-Name</span></span>
<span data-ttu-id="f2b81-114">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b81-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2b81-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2b81-115">-Confirm</span></span>
<span data-ttu-id="f2b81-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2b81-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b81-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b81-117">-WhatIf</span></span>
<span data-ttu-id="f2b81-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b81-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b81-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2b81-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b81-120">CommonParameters</span></span>
<span data-ttu-id="f2b81-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b81-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b81-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2b81-123">INPUTS</span></span>

### <span data-ttu-id="f2b81-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f2b81-124">System.String</span></span>

## <span data-ttu-id="f2b81-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2b81-125">OUTPUTS</span></span>

### <span data-ttu-id="f2b81-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2b81-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2b81-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2b81-127">NOTES</span></span>
* <span data-ttu-id="f2b81-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f2b81-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f2b81-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2b81-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2b81-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f2b81-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f2b81-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f2b81-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f2b81-132">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f2b81-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f2b81-133">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f2b81-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


