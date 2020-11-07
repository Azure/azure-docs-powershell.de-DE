---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 9ad926a9dd9a3a13bff1f31cfa1ae7d689cadbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660932"
---
# <span data-ttu-id="b9fe2-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fe2-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b9fe2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fe2-103">Fügt ein vertrauenswürdiges Stammzertifikat zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="b9fe2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9fe2-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9fe2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fe2-106">Mit dem Cmdlet **Add-AzApplicationGatewayTrustedRootCertificate** wird ein vertrauenswürdiges Stammzertifikat zu einem Azure Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="b9fe2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="b9fe2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9fe2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b9fe2-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b9fe2-110">Der zweite Befehl Addes ein neues vertrauenswürdiges Stammzertifikat an das Anwendungs Gateway, wobei der Pfad des Stammzertifikats als Eingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="b9fe2-111">Der dritte Befehl erstellt eine neue Back-End-HTTP-Einstellung unter Verwendung des vertrauenswürdigen Stammzertifikats für die Validierung des Back-End-Serverzertifikats.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="b9fe2-112">Der vierten-Befehl aktualisiert das Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="b9fe2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9fe2-113">PARAMETERS</span></span>

### <span data-ttu-id="b9fe2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fe2-114">-ApplicationGateway</span></span>
<span data-ttu-id="b9fe2-115">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fe2-115">The applicationGateway</span></span>

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

### <span data-ttu-id="b9fe2-116">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="b9fe2-116">-CertificateFile</span></span>
<span data-ttu-id="b9fe2-117">Pfad der Zertifikat CER-Datei</span><span class="sxs-lookup"><span data-stu-id="b9fe2-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="b9fe2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fe2-118">-DefaultProfile</span></span>
<span data-ttu-id="b9fe2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fe2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9fe2-120">-Name</span></span>
<span data-ttu-id="b9fe2-121">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b9fe2-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="b9fe2-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9fe2-122">-Confirm</span></span>
<span data-ttu-id="b9fe2-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9fe2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9fe2-124">-WhatIf</span></span>
<span data-ttu-id="b9fe2-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9fe2-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9fe2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fe2-127">CommonParameters</span></span>
<span data-ttu-id="b9fe2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fe2-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fe2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fe2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9fe2-130">INPUTS</span></span>

### <span data-ttu-id="b9fe2-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fe2-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9fe2-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9fe2-132">OUTPUTS</span></span>

### <span data-ttu-id="b9fe2-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fe2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9fe2-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9fe2-134">NOTES</span></span>

## <span data-ttu-id="b9fe2-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9fe2-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9fe2-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fe2-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b9fe2-137">Neu – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fe2-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b9fe2-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fe2-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b9fe2-139">Satz-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fe2-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
