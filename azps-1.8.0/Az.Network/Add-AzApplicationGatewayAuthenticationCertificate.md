---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1a1d484d3b8d23633393c0f300f84091b06c1d0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660962"
---
# <span data-ttu-id="2b1b9-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1b9-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="2b1b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1b9-103">Fügt ein Authentifizierungszertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="2b1b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b1b9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b1b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1b9-106">Mit dem Cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** wird ein Authentifizierungszertifikat zu einem Azure Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="2b1b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="2b1b9-108">Beispiel 1: Hinzufügen eines Authentifizierungszertifikats zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2b1b9-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2b1b9-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen appGwName ab und speichert es in $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="2b1b9-110">Mit dem zweiten Befehl wird dem Anwendungsgateway ein Authentifizierungszertifikat mit dem Namen cert01 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="2b1b9-111">Der dritte Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="2b1b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b1b9-112">PARAMETERS</span></span>

### <span data-ttu-id="2b1b9-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b1b9-113">-ApplicationGateway</span></span>
<span data-ttu-id="2b1b9-114">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="2b1b9-115">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="2b1b9-115">-CertificateFile</span></span>
<span data-ttu-id="2b1b9-116">Gibt den Pfad des vom Cmdlet hinzugefügten Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="2b1b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1b9-117">-DefaultProfile</span></span>
<span data-ttu-id="2b1b9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b1b9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2b1b9-119">-Name</span></span>
<span data-ttu-id="2b1b9-120">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="2b1b9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b1b9-121">-Confirm</span></span>
<span data-ttu-id="2b1b9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b1b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b1b9-123">-WhatIf</span></span>
<span data-ttu-id="2b1b9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b1b9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b1b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1b9-126">CommonParameters</span></span>
<span data-ttu-id="2b1b9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1b9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1b9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b1b9-129">INPUTS</span></span>

### <span data-ttu-id="2b1b9-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b1b9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b1b9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b1b9-131">OUTPUTS</span></span>

### <span data-ttu-id="2b1b9-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b1b9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b1b9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b1b9-133">NOTES</span></span>
* <span data-ttu-id="2b1b9-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="2b1b9-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2b1b9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b1b9-135">RELATED LINKS</span></span>

[<span data-ttu-id="2b1b9-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1b9-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2b1b9-137">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1b9-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2b1b9-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1b9-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="2b1b9-139">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1b9-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


