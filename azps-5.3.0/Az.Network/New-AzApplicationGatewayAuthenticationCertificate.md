---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379545"
---
# <span data-ttu-id="bdd80-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bdd80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd80-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd80-103">Erstellt ein Authentifizierungszertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bdd80-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="bdd80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdd80-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd80-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdd80-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd80-106">Das **Cmdlet "New-AzApplicationGatewayAuthenticationCertificate"** erstellt ein Authentifizierungszertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bdd80-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bdd80-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdd80-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd80-108">Beispiel 1: Erstellen eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="bdd80-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="bdd80-109">Der erste Befehl erstellt ein Authentifizierungszertifikat namens "cert01".</span><span class="sxs-lookup"><span data-stu-id="bdd80-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="bdd80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdd80-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd80-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bdd80-111">-CertificateFile</span></span>
<span data-ttu-id="bdd80-112">Gibt den Pfad des Authentifizierungszertifikats an.</span><span class="sxs-lookup"><span data-stu-id="bdd80-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="bdd80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd80-113">-DefaultProfile</span></span>
<span data-ttu-id="bdd80-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdd80-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd80-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bdd80-115">-Name</span></span>
<span data-ttu-id="bdd80-116">Gibt einen Namen für das Authentifizierungszertifikat an.</span><span class="sxs-lookup"><span data-stu-id="bdd80-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="bdd80-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdd80-117">-Confirm</span></span>
<span data-ttu-id="bdd80-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdd80-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd80-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bdd80-119">-WhatIf</span></span>
<span data-ttu-id="bdd80-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdd80-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd80-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdd80-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd80-122">CommonParameters</span></span>
<span data-ttu-id="bdd80-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd80-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd80-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd80-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdd80-125">INPUTS</span></span>

### <span data-ttu-id="bdd80-126">Keine</span><span class="sxs-lookup"><span data-stu-id="bdd80-126">None</span></span>

## <span data-ttu-id="bdd80-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdd80-127">OUTPUTS</span></span>

### <span data-ttu-id="bdd80-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bdd80-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bdd80-129">NOTES</span></span>
* <span data-ttu-id="bdd80-130">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bdd80-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bdd80-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bdd80-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdd80-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bdd80-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bdd80-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bdd80-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd80-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


