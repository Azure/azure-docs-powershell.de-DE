---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472188"
---
# <span data-ttu-id="65833-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65833-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="65833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65833-102">SYNOPSIS</span></span>
<span data-ttu-id="65833-103">Ändert die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="65833-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="65833-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65833-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65833-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65833-105">DESCRIPTION</span></span>
<span data-ttu-id="65833-106">Das **Cmdlet "Set-AzApplicationGatewayTrustedClientCertificate"** ändert die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="65833-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="65833-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65833-107">EXAMPLES</span></span>

### <span data-ttu-id="65833-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65833-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="65833-109">In den obigen Beispielszenarien wird veranschaulicht, wie ein vorhandenes Zertifikatkettenobjekt der Client-CA aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="65833-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="65833-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="65833-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="65833-111">Der zweite Befehl ändert das vorhandene Zertifikatkettenobjekt der Zertifizierungsstelle für vertrauenswürdige Client-Zertifizierungsstellen mit einer neuen Zertifizierungsstellenzertifikatskettedatei.</span><span class="sxs-lookup"><span data-stu-id="65833-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="65833-112">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="65833-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="65833-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65833-113">PARAMETERS</span></span>

### <span data-ttu-id="65833-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65833-114">-ApplicationGateway</span></span>
<span data-ttu-id="65833-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65833-115">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65833-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="65833-116">-CertificateFile</span></span>
<span data-ttu-id="65833-117">Pfad der Zertifikatkettendatei der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="65833-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="65833-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65833-118">-DefaultProfile</span></span>
<span data-ttu-id="65833-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65833-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65833-120">-Name</span><span class="sxs-lookup"><span data-stu-id="65833-120">-Name</span></span>
<span data-ttu-id="65833-121">Der Name der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="65833-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="65833-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65833-122">-Confirm</span></span>
<span data-ttu-id="65833-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65833-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65833-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="65833-124">-WhatIf</span></span>
<span data-ttu-id="65833-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65833-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65833-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65833-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65833-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65833-127">CommonParameters</span></span>
<span data-ttu-id="65833-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65833-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65833-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65833-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65833-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65833-130">INPUTS</span></span>

### <span data-ttu-id="65833-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65833-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65833-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65833-132">OUTPUTS</span></span>

### <span data-ttu-id="65833-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65833-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65833-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65833-134">NOTES</span></span>

## <span data-ttu-id="65833-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65833-135">RELATED LINKS</span></span>

[<span data-ttu-id="65833-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65833-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65833-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65833-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65833-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65833-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65833-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65833-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)