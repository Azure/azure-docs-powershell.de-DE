---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 51bb8ff46613080d3fa62a2b4953419348cb99bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499958"
---
# <span data-ttu-id="f6dc3-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f6dc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dc3-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6dc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6dc3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6dc3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f6dc3-106">Das Cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** erstellt ein Authentifizierungszertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f6dc3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6dc3-107">EXAMPLES</span></span>

## <span data-ttu-id="f6dc3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6dc3-108">PARAMETERS</span></span>

### <span data-ttu-id="f6dc3-109">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="f6dc3-109">-CertificateFile</span></span>
<span data-ttu-id="f6dc3-110">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="f6dc3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f6dc3-111">-Name</span></span>
<span data-ttu-id="f6dc3-112">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-112">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="f6dc3-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6dc3-113">-Confirm</span></span>
<span data-ttu-id="f6dc3-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6dc3-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6dc3-115">-WhatIf</span></span>
<span data-ttu-id="f6dc3-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6dc3-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6dc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6dc3-118">-DefaultProfile</span></span>
<span data-ttu-id="f6dc3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6dc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dc3-120">CommonParameters</span></span>
<span data-ttu-id="f6dc3-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6dc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dc3-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6dc3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dc3-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6dc3-123">INPUTS</span></span>

### <span data-ttu-id="f6dc3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f6dc3-124">System.String</span></span>

## <span data-ttu-id="f6dc3-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6dc3-125">OUTPUTS</span></span>

### <span data-ttu-id="f6dc3-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f6dc3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6dc3-127">NOTES</span></span>
* <span data-ttu-id="f6dc3-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f6dc3-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f6dc3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6dc3-129">RELATED LINKS</span></span>

[<span data-ttu-id="f6dc3-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6dc3-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6dc3-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f6dc3-133">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6dc3-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


