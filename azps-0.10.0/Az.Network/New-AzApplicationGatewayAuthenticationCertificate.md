---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841447"
---
# <span data-ttu-id="25b27-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="25b27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25b27-102">SYNOPSIS</span></span>
<span data-ttu-id="25b27-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="25b27-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="25b27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25b27-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b27-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25b27-105">DESCRIPTION</span></span>
<span data-ttu-id="25b27-106">Das Cmdlet **New-AzApplicationGatewayAuthenticationCertificate** erstellt ein Authentifizierungszertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="25b27-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="25b27-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25b27-107">EXAMPLES</span></span>

### <span data-ttu-id="25b27-108">1:</span><span class="sxs-lookup"><span data-stu-id="25b27-108">1:</span></span>
```

```

## <span data-ttu-id="25b27-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b27-109">PARAMETERS</span></span>

### <span data-ttu-id="25b27-110">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="25b27-110">-CertificateFile</span></span>
<span data-ttu-id="25b27-111">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="25b27-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="25b27-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b27-112">-DefaultProfile</span></span>
<span data-ttu-id="25b27-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25b27-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b27-114">-Name</span><span class="sxs-lookup"><span data-stu-id="25b27-114">-Name</span></span>
<span data-ttu-id="25b27-115">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="25b27-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="25b27-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25b27-116">-Confirm</span></span>
<span data-ttu-id="25b27-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25b27-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b27-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b27-118">-WhatIf</span></span>
<span data-ttu-id="25b27-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25b27-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b27-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25b27-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b27-121">CommonParameters</span></span>
<span data-ttu-id="25b27-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b27-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b27-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b27-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25b27-124">INPUTS</span></span>

### <span data-ttu-id="25b27-125">System. String</span><span class="sxs-lookup"><span data-stu-id="25b27-125">System.String</span></span>

## <span data-ttu-id="25b27-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25b27-126">OUTPUTS</span></span>

### <span data-ttu-id="25b27-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="25b27-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="25b27-128">NOTES</span></span>
* <span data-ttu-id="25b27-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="25b27-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="25b27-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25b27-130">RELATED LINKS</span></span>

[<span data-ttu-id="25b27-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="25b27-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="25b27-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="25b27-134">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b27-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


