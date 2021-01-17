---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472186"
---
# <span data-ttu-id="1167c-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1167c-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="1167c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1167c-102">SYNOPSIS</span></span>
<span data-ttu-id="1167c-103">Aktualisiert ein vertrauenswürdiges Stammzertifikat eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1167c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="1167c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1167c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1167c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1167c-105">DESCRIPTION</span></span>
<span data-ttu-id="1167c-106">Das **Cmdlet "Set-AzApplicationGatewayTrustedRootCertificate"** ändert das vorhandene vertrauenswürdige Stammzertifikat eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1167c-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="1167c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1167c-107">EXAMPLES</span></span>

### <span data-ttu-id="1167c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1167c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1167c-109">In den Beispielszenarien oben wird gezeigt, wie ein vorhandenes vertrauenswürdiges Stammzertifikat aktualisiert wird, wenn ein Stammzertifikat rollt.</span><span class="sxs-lookup"><span data-stu-id="1167c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="1167c-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="1167c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="1167c-111">Der zweite Befehl ändert das vorhandene vertrauenswürdige Stammzertifikat mit einem neuen Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="1167c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="1167c-112">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1167c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="1167c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1167c-113">PARAMETERS</span></span>

### <span data-ttu-id="1167c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1167c-114">-ApplicationGateway</span></span>
<span data-ttu-id="1167c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1167c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="1167c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1167c-116">-CertificateFile</span></span>
<span data-ttu-id="1167c-117">Pfad der Zertifikat-CER-Datei</span><span class="sxs-lookup"><span data-stu-id="1167c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="1167c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1167c-118">-DefaultProfile</span></span>
<span data-ttu-id="1167c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1167c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1167c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1167c-120">-Name</span></span>
<span data-ttu-id="1167c-121">Der Name des Zertifikats "TrustedRoot"</span><span class="sxs-lookup"><span data-stu-id="1167c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="1167c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1167c-122">-Confirm</span></span>
<span data-ttu-id="1167c-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1167c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1167c-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1167c-124">-WhatIf</span></span>
<span data-ttu-id="1167c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1167c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1167c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1167c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1167c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1167c-127">CommonParameters</span></span>
<span data-ttu-id="1167c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1167c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1167c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1167c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1167c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1167c-130">INPUTS</span></span>

### <span data-ttu-id="1167c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1167c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1167c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1167c-132">OUTPUTS</span></span>

### <span data-ttu-id="1167c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1167c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1167c-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1167c-134">NOTES</span></span>

## <span data-ttu-id="1167c-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1167c-135">RELATED LINKS</span></span>

[<span data-ttu-id="1167c-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1167c-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1167c-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1167c-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1167c-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1167c-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1167c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1167c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
