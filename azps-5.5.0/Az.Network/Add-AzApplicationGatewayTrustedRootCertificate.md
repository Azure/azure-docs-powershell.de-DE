---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159265"
---
# <span data-ttu-id="49ea9-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="49ea9-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="49ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="49ea9-103">Fügt einem Anwendungsgateway ein vertrauenswürdiges Stammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="49ea9-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="49ea9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49ea9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ea9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="49ea9-106">Das **Cmdlet "Add-AzApplicationGatewayTrustedRootCertificate"** fügt einem Azure-Anwendungsgateway ein vertrauenswürdiges Stammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="49ea9-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="49ea9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="49ea9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49ea9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="49ea9-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="49ea9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="49ea9-110">Der zweite Befehl fügt ein neues vertrauenswürdiges Stammzertifikat zum Anwendungsgateway hinzu, das den Pfad des Stammzertifikats als Eingabe einnimmt.</span><span class="sxs-lookup"><span data-stu-id="49ea9-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="49ea9-111">Der dritte Befehl erstellt eine neue Back-End-HTTP-Einstellung mit einem vertrauenswürdigen Stammzertifikat zum Überprüfen des Back-End-Server-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="49ea9-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="49ea9-112">Mit dem vierten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="49ea9-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="49ea9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49ea9-113">PARAMETERS</span></span>

### <span data-ttu-id="49ea9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ea9-114">-ApplicationGateway</span></span>
<span data-ttu-id="49ea9-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ea9-115">The applicationGateway</span></span>

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

### <span data-ttu-id="49ea9-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="49ea9-116">-CertificateFile</span></span>
<span data-ttu-id="49ea9-117">Pfad der Zertifikat-CER-Datei</span><span class="sxs-lookup"><span data-stu-id="49ea9-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="49ea9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ea9-118">-DefaultProfile</span></span>
<span data-ttu-id="49ea9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49ea9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ea9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49ea9-120">-Name</span></span>
<span data-ttu-id="49ea9-121">Der Name des Zertifikats "TrustedRoot"</span><span class="sxs-lookup"><span data-stu-id="49ea9-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="49ea9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49ea9-122">-Confirm</span></span>
<span data-ttu-id="49ea9-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49ea9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea9-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49ea9-124">-WhatIf</span></span>
<span data-ttu-id="49ea9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49ea9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ea9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49ea9-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ea9-127">CommonParameters</span></span>
<span data-ttu-id="49ea9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ea9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ea9-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ea9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ea9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49ea9-130">INPUTS</span></span>

### <span data-ttu-id="49ea9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ea9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49ea9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49ea9-132">OUTPUTS</span></span>

### <span data-ttu-id="49ea9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49ea9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49ea9-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49ea9-134">NOTES</span></span>

## <span data-ttu-id="49ea9-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49ea9-135">RELATED LINKS</span></span>

[<span data-ttu-id="49ea9-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="49ea9-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="49ea9-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="49ea9-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="49ea9-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="49ea9-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="49ea9-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="49ea9-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
