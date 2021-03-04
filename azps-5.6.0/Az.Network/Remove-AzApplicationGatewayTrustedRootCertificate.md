---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 635ee4671a235506e7125d33f2f3a14917cc424a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941699"
---
# <span data-ttu-id="cfec3-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cfec3-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cfec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfec3-102">SYNOPSIS</span></span>
<span data-ttu-id="cfec3-103">Entfernt ein vertrauenswürdiges Stammzertifikat aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="cfec3-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="cfec3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfec3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfec3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfec3-105">DESCRIPTION</span></span>
<span data-ttu-id="cfec3-106">Das **Cmdlet Remove-AzApplicationGatewayTrustedRootCertificate** entfernt ein vertrauenswürdiges Stammzertifikat aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="cfec3-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="cfec3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cfec3-107">EXAMPLES</span></span>

### <span data-ttu-id="cfec3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfec3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="cfec3-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="cfec3-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="cfec3-110">Mit dem zweiten Befehl wird das vertrauenswürdige Stammzertifikat mit dem Namen myRootCA aus dem anwendungsgateway entfernt, das in $gw.</span><span class="sxs-lookup"><span data-stu-id="cfec3-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="cfec3-111">Mit dem dritten Befehl wird das Anwendungsgateway in Azure aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cfec3-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="cfec3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cfec3-112">PARAMETERS</span></span>

### <span data-ttu-id="cfec3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfec3-113">-ApplicationGateway</span></span>
<span data-ttu-id="cfec3-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfec3-114">The applicationGateway</span></span>

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

### <span data-ttu-id="cfec3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfec3-115">-DefaultProfile</span></span>
<span data-ttu-id="cfec3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfec3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfec3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cfec3-117">-Name</span></span>
<span data-ttu-id="cfec3-118">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="cfec3-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="cfec3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cfec3-119">-Confirm</span></span>
<span data-ttu-id="cfec3-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfec3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfec3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfec3-121">-WhatIf</span></span>
<span data-ttu-id="cfec3-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfec3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfec3-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfec3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfec3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfec3-124">CommonParameters</span></span>
<span data-ttu-id="cfec3-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfec3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfec3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfec3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfec3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cfec3-127">INPUTS</span></span>

### <span data-ttu-id="cfec3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfec3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfec3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cfec3-129">OUTPUTS</span></span>

### <span data-ttu-id="cfec3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfec3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfec3-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cfec3-131">NOTES</span></span>

## <span data-ttu-id="cfec3-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cfec3-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfec3-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cfec3-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cfec3-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cfec3-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cfec3-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cfec3-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="cfec3-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cfec3-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
