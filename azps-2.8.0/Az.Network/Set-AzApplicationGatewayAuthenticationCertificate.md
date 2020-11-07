---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6e0194135b93898ea14998d92f8f23afd612f221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821280"
---
# <span data-ttu-id="354ed-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="354ed-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="354ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="354ed-102">SYNOPSIS</span></span>
<span data-ttu-id="354ed-103">Aktualisiert ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="354ed-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="354ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="354ed-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="354ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="354ed-105">DESCRIPTION</span></span>
<span data-ttu-id="354ed-106">Das Cmdlet " **Satz-AzApplicationGatewayAuthenticationCertificate** " aktualisiert ein Authentifizierungszertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="354ed-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="354ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="354ed-107">EXAMPLES</span></span>

### <span data-ttu-id="354ed-108">Beispiel 1: Aktualisieren eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="354ed-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="354ed-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen appGwName ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="354ed-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="354ed-110">Der zweite Befehl aktualisiert das Authentifizierungszertifikat mit dem Namen cert01 im Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="354ed-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="354ed-111">Der dritte Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="354ed-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="354ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="354ed-112">PARAMETERS</span></span>

### <span data-ttu-id="354ed-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="354ed-113">-ApplicationGateway</span></span>
<span data-ttu-id="354ed-114">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="354ed-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="354ed-115">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="354ed-115">-CertificateFile</span></span>
<span data-ttu-id="354ed-116">Gibt den Pfad der Authentifizierungszertifikatdatei an, mit der dieses Cmdlet das Zertifikat aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="354ed-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="354ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354ed-117">-DefaultProfile</span></span>
<span data-ttu-id="354ed-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="354ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="354ed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="354ed-119">-Name</span></span>
<span data-ttu-id="354ed-120">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="354ed-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="354ed-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="354ed-121">-Confirm</span></span>
<span data-ttu-id="354ed-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="354ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="354ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354ed-123">-WhatIf</span></span>
<span data-ttu-id="354ed-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="354ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354ed-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="354ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="354ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354ed-126">CommonParameters</span></span>
<span data-ttu-id="354ed-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354ed-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354ed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354ed-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="354ed-129">INPUTS</span></span>

### <span data-ttu-id="354ed-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="354ed-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="354ed-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="354ed-131">OUTPUTS</span></span>

### <span data-ttu-id="354ed-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="354ed-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="354ed-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="354ed-133">NOTES</span></span>
* <span data-ttu-id="354ed-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="354ed-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="354ed-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="354ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="354ed-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="354ed-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="354ed-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="354ed-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="354ed-138">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="354ed-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="354ed-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="354ed-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


