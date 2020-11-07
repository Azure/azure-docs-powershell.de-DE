---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849168"
---
# <span data-ttu-id="a9a7f-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a9a7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a7f-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9a7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9a7f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a7f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a7f-106">Das Cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** erstellt ein Authentifizierungszertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="a9a7f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9a7f-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a7f-108">1:</span><span class="sxs-lookup"><span data-stu-id="a9a7f-108">1:</span></span>
```

```

## <span data-ttu-id="a9a7f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9a7f-109">PARAMETERS</span></span>

### <span data-ttu-id="a9a7f-110">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="a9a7f-110">-CertificateFile</span></span>
<span data-ttu-id="a9a7f-111">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="a9a7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a7f-112">-DefaultProfile</span></span>
<span data-ttu-id="a9a7f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9a7f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a9a7f-114">-Name</span></span>
<span data-ttu-id="a9a7f-115">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="a9a7f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9a7f-116">-Confirm</span></span>
<span data-ttu-id="a9a7f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a7f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a7f-118">-WhatIf</span></span>
<span data-ttu-id="a9a7f-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a7f-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a7f-121">CommonParameters</span></span>
<span data-ttu-id="a9a7f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a7f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a7f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a7f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9a7f-124">INPUTS</span></span>

### <span data-ttu-id="a9a7f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a9a7f-125">System.String</span></span>

## <span data-ttu-id="a9a7f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9a7f-126">OUTPUTS</span></span>

### <span data-ttu-id="a9a7f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a9a7f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9a7f-128">NOTES</span></span>
* <span data-ttu-id="a9a7f-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="a9a7f-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a9a7f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9a7f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9a7f-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a9a7f-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a9a7f-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a9a7f-134">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a7f-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


