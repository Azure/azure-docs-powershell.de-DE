---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 3facee36f6862c02975566dee20d9e7fb8c8824f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479054"
---
# <span data-ttu-id="e9c24-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e9c24-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e9c24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9c24-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c24-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e9c24-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9c24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9c24-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9c24-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c24-106">Das Cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** entfernt ein Authentifizierungszertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e9c24-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e9c24-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9c24-107">EXAMPLES</span></span>

## <span data-ttu-id="e9c24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c24-108">PARAMETERS</span></span>

### <span data-ttu-id="e9c24-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9c24-109">-ApplicationGateway</span></span>
<span data-ttu-id="e9c24-110">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9c24-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="e9c24-111">-Name</span><span class="sxs-lookup"><span data-stu-id="e9c24-111">-Name</span></span>
<span data-ttu-id="e9c24-112">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c24-112">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c24-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9c24-113">-Confirm</span></span>
<span data-ttu-id="e9c24-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9c24-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c24-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c24-115">-WhatIf</span></span>
<span data-ttu-id="e9c24-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9c24-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c24-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9c24-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c24-118">-DefaultProfile</span></span>
<span data-ttu-id="e9c24-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9c24-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9c24-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c24-120">CommonParameters</span></span>
<span data-ttu-id="e9c24-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c24-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c24-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c24-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c24-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9c24-123">INPUTS</span></span>

### <span data-ttu-id="e9c24-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c24-124">System.String</span></span>

## <span data-ttu-id="e9c24-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9c24-125">OUTPUTS</span></span>

### <span data-ttu-id="e9c24-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9c24-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9c24-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9c24-127">NOTES</span></span>
* <span data-ttu-id="e9c24-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e9c24-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e9c24-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9c24-129">RELATED LINKS</span></span>

[<span data-ttu-id="e9c24-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e9c24-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e9c24-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e9c24-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e9c24-132">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e9c24-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e9c24-133">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e9c24-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


