---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170124"
---
# <span data-ttu-id="0780e-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0780e-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0780e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0780e-102">SYNOPSIS</span></span>
<span data-ttu-id="0780e-103">Fügt einem Anwendungsgateway ein Authentifizierungszertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="0780e-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="0780e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0780e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0780e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0780e-105">DESCRIPTION</span></span>
<span data-ttu-id="0780e-106">Das **Cmdlet "Add-AzApplicationGatewayAuthenticationCertificate"** fügt einem Azure-Anwendungsgateway ein Authentifizierungszertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="0780e-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="0780e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0780e-107">EXAMPLES</span></span>

### <span data-ttu-id="0780e-108">Beispiel 1: Hinzufügen eines Authentifizierungszertifikats zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0780e-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="0780e-109">Der erste Befehl ruft ein Anwendungsgateway namens "appGwName" ab und speichert es in $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="0780e-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="0780e-110">Der zweite Befehl fügt dem Anwendungsgateway das Authentifizierungszertifikat "cert01" hinzu.</span><span class="sxs-lookup"><span data-stu-id="0780e-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="0780e-111">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0780e-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="0780e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0780e-112">PARAMETERS</span></span>

### <span data-ttu-id="0780e-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0780e-113">-ApplicationGateway</span></span>
<span data-ttu-id="0780e-114">Gibt den Namen des Anwendungsgateways an, für das dieses Cmdlet ein Authentifizierungszertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0780e-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="0780e-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0780e-115">-CertificateFile</span></span>
<span data-ttu-id="0780e-116">Gibt den Pfad des Authentifizierungszertifikats an, das von diesem Cmdlet hinzufügt wird.</span><span class="sxs-lookup"><span data-stu-id="0780e-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0780e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0780e-117">-DefaultProfile</span></span>
<span data-ttu-id="0780e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0780e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0780e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0780e-119">-Name</span></span>
<span data-ttu-id="0780e-120">Gibt den Namen eines Zertifikats an, das dieses Cmdlet dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0780e-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="0780e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0780e-121">-Confirm</span></span>
<span data-ttu-id="0780e-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0780e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0780e-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0780e-123">-WhatIf</span></span>
<span data-ttu-id="0780e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0780e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0780e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0780e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0780e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0780e-126">CommonParameters</span></span>
<span data-ttu-id="0780e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0780e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0780e-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0780e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0780e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0780e-129">INPUTS</span></span>

### <span data-ttu-id="0780e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0780e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0780e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0780e-131">OUTPUTS</span></span>

### <span data-ttu-id="0780e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0780e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0780e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0780e-133">NOTES</span></span>
* <span data-ttu-id="0780e-134">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0780e-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0780e-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0780e-135">RELATED LINKS</span></span>

[<span data-ttu-id="0780e-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0780e-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0780e-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0780e-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0780e-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0780e-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0780e-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0780e-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


