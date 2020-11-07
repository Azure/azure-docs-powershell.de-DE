---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7e1c5c301b13f37086f4b6fc96e7254230684d10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822219"
---
# <span data-ttu-id="4ec3e-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4ec3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ec3e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec3e-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="4ec3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ec3e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ec3e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec3e-106">Das Cmdlet **New-AzApplicationGatewayAuthenticationCertificate** erstellt ein Authentifizierungszertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="4ec3e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ec3e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec3e-108">Beispiel 1: Erstellen eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="4ec3e-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="4ec3e-109">Der erste Befehl erstellt das Authentifizierungszertifikat mit dem Namen cert01.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="4ec3e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ec3e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ec3e-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="4ec3e-111">-CertificateFile</span></span>
<span data-ttu-id="4ec3e-112">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="4ec3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec3e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ec3e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec3e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4ec3e-115">-Name</span></span>
<span data-ttu-id="4ec3e-116">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="4ec3e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ec3e-117">-Confirm</span></span>
<span data-ttu-id="4ec3e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec3e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec3e-119">-WhatIf</span></span>
<span data-ttu-id="4ec3e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec3e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec3e-122">CommonParameters</span></span>
<span data-ttu-id="4ec3e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec3e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec3e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ec3e-125">INPUTS</span></span>

### <span data-ttu-id="4ec3e-126">Keine</span><span class="sxs-lookup"><span data-stu-id="4ec3e-126">None</span></span>

## <span data-ttu-id="4ec3e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ec3e-127">OUTPUTS</span></span>

### <span data-ttu-id="4ec3e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="4ec3e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ec3e-129">NOTES</span></span>
* <span data-ttu-id="4ec3e-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="4ec3e-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4ec3e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ec3e-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ec3e-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ec3e-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ec3e-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="4ec3e-135">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec3e-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


