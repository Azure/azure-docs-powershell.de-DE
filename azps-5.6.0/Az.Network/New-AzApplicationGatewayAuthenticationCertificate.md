---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947824"
---
# <span data-ttu-id="ffd20-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ffd20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffd20-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd20-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ffd20-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="ffd20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffd20-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd20-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffd20-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd20-106">Das **Cmdlet New-AzApplicationGatewayAuthenticationCertificate** erstellt ein Authentifizierungszertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ffd20-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ffd20-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffd20-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd20-108">Beispiel 1: Erstellen eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="ffd20-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="ffd20-109">Mit dem ersten Befehl wird ein Authentifizierungszertifikat mit dem Namen "cert01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ffd20-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="ffd20-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ffd20-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd20-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ffd20-111">-CertificateFile</span></span>
<span data-ttu-id="ffd20-112">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="ffd20-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="ffd20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd20-113">-DefaultProfile</span></span>
<span data-ttu-id="ffd20-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffd20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffd20-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ffd20-115">-Name</span></span>
<span data-ttu-id="ffd20-116">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="ffd20-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="ffd20-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffd20-117">-Confirm</span></span>
<span data-ttu-id="ffd20-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffd20-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd20-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd20-119">-WhatIf</span></span>
<span data-ttu-id="ffd20-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffd20-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd20-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffd20-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd20-122">CommonParameters</span></span>
<span data-ttu-id="ffd20-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd20-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd20-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd20-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffd20-125">INPUTS</span></span>

### <span data-ttu-id="ffd20-126">Keine</span><span class="sxs-lookup"><span data-stu-id="ffd20-126">None</span></span>

## <span data-ttu-id="ffd20-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffd20-127">OUTPUTS</span></span>

### <span data-ttu-id="ffd20-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ffd20-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ffd20-129">NOTES</span></span>
* <span data-ttu-id="ffd20-130">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="ffd20-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ffd20-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ffd20-131">RELATED LINKS</span></span>

[<span data-ttu-id="ffd20-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffd20-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffd20-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ffd20-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ffd20-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


