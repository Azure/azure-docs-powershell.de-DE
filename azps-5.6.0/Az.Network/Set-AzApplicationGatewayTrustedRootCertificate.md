---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 839f2a647c4a06ddd1bdebe9b95fac0fdbdd91dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941051"
---
# <span data-ttu-id="beabe-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="beabe-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="beabe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beabe-102">SYNOPSIS</span></span>
<span data-ttu-id="beabe-103">Aktualisiert ein vertrauenswürdiges Stammzertifikat eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="beabe-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="beabe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="beabe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beabe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="beabe-105">DESCRIPTION</span></span>
<span data-ttu-id="beabe-106">Das **Cmdlet Set-AzApplicationGatewayTrustedRootCertificate** ändert das vorhandene vertrauenswürdige Stammzertifikat eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="beabe-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="beabe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="beabe-107">EXAMPLES</span></span>

### <span data-ttu-id="beabe-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="beabe-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="beabe-109">In den obigen Beispielszenarien wird gezeigt, wie Ein vorhandenes vertrauenswürdiges Stammzertifikat aktualisiert wird, wenn ein Stammzertifikat rollt.</span><span class="sxs-lookup"><span data-stu-id="beabe-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="beabe-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="beabe-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="beabe-111">Mit dem zweiten Befehl wird das vorhandene vertrauenswürdige Stammzertifikat mit einem neuen Stammzertifikat geändert.</span><span class="sxs-lookup"><span data-stu-id="beabe-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="beabe-112">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="beabe-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="beabe-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="beabe-113">PARAMETERS</span></span>

### <span data-ttu-id="beabe-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beabe-114">-ApplicationGateway</span></span>
<span data-ttu-id="beabe-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beabe-115">The applicationGateway</span></span>

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

### <span data-ttu-id="beabe-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="beabe-116">-CertificateFile</span></span>
<span data-ttu-id="beabe-117">Pfad der Zertifikat-CER-Datei</span><span class="sxs-lookup"><span data-stu-id="beabe-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="beabe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beabe-118">-DefaultProfile</span></span>
<span data-ttu-id="beabe-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="beabe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beabe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="beabe-120">-Name</span></span>
<span data-ttu-id="beabe-121">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="beabe-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="beabe-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beabe-122">-Confirm</span></span>
<span data-ttu-id="beabe-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beabe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beabe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beabe-124">-WhatIf</span></span>
<span data-ttu-id="beabe-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beabe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beabe-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beabe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beabe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beabe-127">CommonParameters</span></span>
<span data-ttu-id="beabe-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beabe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beabe-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beabe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beabe-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="beabe-130">INPUTS</span></span>

### <span data-ttu-id="beabe-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beabe-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="beabe-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="beabe-132">OUTPUTS</span></span>

### <span data-ttu-id="beabe-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="beabe-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="beabe-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="beabe-134">NOTES</span></span>

## <span data-ttu-id="beabe-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="beabe-135">RELATED LINKS</span></span>

[<span data-ttu-id="beabe-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="beabe-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="beabe-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="beabe-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="beabe-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="beabe-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="beabe-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="beabe-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
