---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938035"
---
# <span data-ttu-id="16e01-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="16e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e01-102">SYNOPSIS</span></span>
<span data-ttu-id="16e01-103">Erstellt eine Zertifikatkette für vertrauenswürdige Client-Zertifizierungsstellen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="16e01-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="16e01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16e01-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e01-105">DESCRIPTION</span></span>
<span data-ttu-id="16e01-106">Das New-AzApplicationGatewayTrustedClientCertificate-Cmdlet erstellt eine Zertifikatkette für vertrauenswürdige Client-Zertifizierungsstellen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="16e01-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="16e01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16e01-107">EXAMPLES</span></span>

### <span data-ttu-id="16e01-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16e01-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="16e01-109">Der Befehl erstellt ein neues vertrauenswürdiges Client-CA-Zertifikatkette-Objekt, das den Pfad des Client-CA-Zertifikats als Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="16e01-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="16e01-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16e01-110">PARAMETERS</span></span>

### <span data-ttu-id="16e01-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="16e01-111">-CertificateFile</span></span>
<span data-ttu-id="16e01-112">Pfad der Zertifikatkette der vertrauenswürdigen Client-CA</span><span class="sxs-lookup"><span data-stu-id="16e01-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="16e01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e01-113">-DefaultProfile</span></span>
<span data-ttu-id="16e01-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16e01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e01-115">-Name</span><span class="sxs-lookup"><span data-stu-id="16e01-115">-Name</span></span>
<span data-ttu-id="16e01-116">Der Name der Zertifikatkette für vertrauenswürdige Client-Zertifizierungsstellen</span><span class="sxs-lookup"><span data-stu-id="16e01-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="16e01-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16e01-117">-Confirm</span></span>
<span data-ttu-id="16e01-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16e01-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e01-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e01-119">-WhatIf</span></span>
<span data-ttu-id="16e01-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16e01-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e01-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16e01-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e01-122">CommonParameters</span></span>
<span data-ttu-id="16e01-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e01-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16e01-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e01-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16e01-125">INPUTS</span></span>

### <span data-ttu-id="16e01-126">Keine</span><span class="sxs-lookup"><span data-stu-id="16e01-126">None</span></span>

## <span data-ttu-id="16e01-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16e01-127">OUTPUTS</span></span>

### <span data-ttu-id="16e01-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="16e01-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="16e01-129">NOTES</span></span>

## <span data-ttu-id="16e01-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="16e01-130">RELATED LINKS</span></span>

[<span data-ttu-id="16e01-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="16e01-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="16e01-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="16e01-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16e01-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)