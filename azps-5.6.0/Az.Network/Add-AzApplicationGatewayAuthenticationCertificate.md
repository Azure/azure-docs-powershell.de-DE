---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ba0d82ab04f8e0c990c7bbf15facb3ee725f7609
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926643"
---
# <span data-ttu-id="9b120-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b120-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9b120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b120-102">SYNOPSIS</span></span>
<span data-ttu-id="9b120-103">Fügt einem Anwendungsgateway ein Authentifizierungszertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b120-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="9b120-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b120-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b120-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b120-105">DESCRIPTION</span></span>
<span data-ttu-id="9b120-106">Das **Add-AzApplicationGatewayAuthenticationCertificate-Cmdlet** fügt einem Azure-Anwendungsgateway ein Authentifizierungszertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b120-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="9b120-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b120-107">EXAMPLES</span></span>

### <span data-ttu-id="9b120-108">Beispiel 1: Hinzufügen eines Authentifizierungszertifikats zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9b120-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9b120-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen "appGwName" ab und speichert es in $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="9b120-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="9b120-110">Der zweite Befehl fügt dem Anwendungsgateway das Authentifizierungszertifikat "cert01" hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b120-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="9b120-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9b120-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="9b120-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b120-112">PARAMETERS</span></span>

### <span data-ttu-id="9b120-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b120-113">-ApplicationGateway</span></span>
<span data-ttu-id="9b120-114">Gibt den Namen des Anwendungsgateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9b120-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="9b120-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9b120-115">-CertificateFile</span></span>
<span data-ttu-id="9b120-116">Gibt den Pfad des Authentifizierungszertifikats an, das von diesem Cmdlet addiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b120-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9b120-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b120-117">-DefaultProfile</span></span>
<span data-ttu-id="9b120-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b120-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b120-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9b120-119">-Name</span></span>
<span data-ttu-id="9b120-120">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9b120-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="9b120-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b120-121">-Confirm</span></span>
<span data-ttu-id="9b120-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b120-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b120-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b120-123">-WhatIf</span></span>
<span data-ttu-id="9b120-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b120-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b120-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b120-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b120-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b120-126">CommonParameters</span></span>
<span data-ttu-id="9b120-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b120-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b120-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b120-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b120-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b120-129">INPUTS</span></span>

### <span data-ttu-id="9b120-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b120-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b120-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b120-131">OUTPUTS</span></span>

### <span data-ttu-id="9b120-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b120-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b120-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9b120-133">NOTES</span></span>
* <span data-ttu-id="9b120-134">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="9b120-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9b120-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9b120-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b120-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b120-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b120-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b120-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b120-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b120-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b120-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b120-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


