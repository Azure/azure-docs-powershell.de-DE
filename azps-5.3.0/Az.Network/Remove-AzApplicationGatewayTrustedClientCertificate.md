---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472208"
---
# <span data-ttu-id="3dd44-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd44-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="3dd44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd44-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd44-103">Entfernt das Zertifikatketteobjekt der vertrauenswürdigen Client-Zertifizierungsstelle aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3dd44-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="3dd44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dd44-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd44-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dd44-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd44-106">Das **Cmdlet "Remove-AzApplicationGatewayTrustedClientCertificate"** entfernt das Zertifikatkettenobjekt der vertrauenswürdigen Client-Zertifizierungsstelle aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3dd44-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="3dd44-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3dd44-107">EXAMPLES</span></span>

### <span data-ttu-id="3dd44-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dd44-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="3dd44-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="3dd44-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="3dd44-110">Mit dem zweiten Befehl wird die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle namens "TrustedClientCertificate01" aus dem Anwendungsgateway entfernt, das auf der $gw.</span><span class="sxs-lookup"><span data-stu-id="3dd44-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="3dd44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dd44-111">PARAMETERS</span></span>

### <span data-ttu-id="3dd44-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dd44-112">-ApplicationGateway</span></span>
<span data-ttu-id="3dd44-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dd44-113">The applicationGateway</span></span>

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

### <span data-ttu-id="3dd44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd44-114">-DefaultProfile</span></span>
<span data-ttu-id="3dd44-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dd44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd44-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3dd44-116">-Name</span></span>
<span data-ttu-id="3dd44-117">Der Name der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="3dd44-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="3dd44-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dd44-118">-Confirm</span></span>
<span data-ttu-id="3dd44-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3dd44-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd44-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3dd44-120">-WhatIf</span></span>
<span data-ttu-id="3dd44-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd44-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd44-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3dd44-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd44-123">CommonParameters</span></span>
<span data-ttu-id="3dd44-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd44-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dd44-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd44-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3dd44-126">INPUTS</span></span>

### <span data-ttu-id="3dd44-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dd44-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3dd44-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3dd44-128">OUTPUTS</span></span>

### <span data-ttu-id="3dd44-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dd44-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3dd44-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3dd44-130">NOTES</span></span>

## <span data-ttu-id="3dd44-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3dd44-131">RELATED LINKS</span></span>

[<span data-ttu-id="3dd44-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd44-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="3dd44-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd44-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="3dd44-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd44-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="3dd44-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd44-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)