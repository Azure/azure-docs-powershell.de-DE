---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: bacdca3f26e18f3dc41ac19990e48f9e6bb63c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927859"
---
# <span data-ttu-id="6b4d1-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="6b4d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4d1-103">Erstellt ein vertrauenswürdiges Stammzertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="6b4d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b4d1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b4d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="6b4d1-106">Das **Cmdlet New-AzApplicationGatewayTrustedRootCertificate** erstellt ein vertrauenswürdiges Stammzertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="6b4d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b4d1-107">EXAMPLES</span></span>

### <span data-ttu-id="6b4d1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b4d1-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="6b4d1-109">Dieser Befehl erstellt ein vertrauenswürdiges Stammzertifikat mit dem Namen List "trc1" und speichert das Ergebnis in der Variablen namens $trc.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="6b4d1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b4d1-110">PARAMETERS</span></span>

### <span data-ttu-id="6b4d1-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6b4d1-111">-CertificateFile</span></span>
<span data-ttu-id="6b4d1-112">Pfad der Zertifikat-CER-Datei</span><span class="sxs-lookup"><span data-stu-id="6b4d1-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="6b4d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4d1-113">-DefaultProfile</span></span>
<span data-ttu-id="6b4d1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b4d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6b4d1-115">-Name</span></span>
<span data-ttu-id="6b4d1-116">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6b4d1-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="6b4d1-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b4d1-117">-Confirm</span></span>
<span data-ttu-id="6b4d1-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b4d1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b4d1-119">-WhatIf</span></span>
<span data-ttu-id="6b4d1-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b4d1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b4d1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4d1-122">CommonParameters</span></span>
<span data-ttu-id="6b4d1-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b4d1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4d1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b4d1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4d1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b4d1-125">INPUTS</span></span>

### <span data-ttu-id="6b4d1-126">Keine</span><span class="sxs-lookup"><span data-stu-id="6b4d1-126">None</span></span>

## <span data-ttu-id="6b4d1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b4d1-127">OUTPUTS</span></span>

### <span data-ttu-id="6b4d1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="6b4d1-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b4d1-129">NOTES</span></span>

## <span data-ttu-id="6b4d1-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b4d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b4d1-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6b4d1-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6b4d1-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="6b4d1-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b4d1-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
