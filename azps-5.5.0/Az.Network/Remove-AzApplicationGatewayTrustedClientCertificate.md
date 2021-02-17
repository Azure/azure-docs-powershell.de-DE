---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154217"
---
# <span data-ttu-id="0fe04-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0fe04-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="0fe04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe04-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe04-103">Entfernt das Zertifikatkettenobjekt der vertrauenswürdigen Client-Zertifizierungsstelle aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0fe04-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="0fe04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fe04-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe04-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fe04-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe04-106">Das **Cmdlet "Remove-AzApplicationGatewayTrustedClientCertificate"** entfernt das Zertifikatkettenobjekt der vertrauenswürdigen Client-Zertifizierungsstelle aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0fe04-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="0fe04-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fe04-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe04-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fe04-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="0fe04-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="0fe04-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="0fe04-110">Mit dem zweiten Befehl wird die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit dem Namen "TrustedClientCertificate01" aus dem Anwendungsgateway entfernt, das im $gw.</span><span class="sxs-lookup"><span data-stu-id="0fe04-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="0fe04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fe04-111">PARAMETERS</span></span>

### <span data-ttu-id="0fe04-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe04-112">-ApplicationGateway</span></span>
<span data-ttu-id="0fe04-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe04-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0fe04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe04-114">-DefaultProfile</span></span>
<span data-ttu-id="0fe04-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fe04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe04-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0fe04-116">-Name</span></span>
<span data-ttu-id="0fe04-117">Der Name der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="0fe04-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="0fe04-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fe04-118">-Confirm</span></span>
<span data-ttu-id="0fe04-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fe04-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe04-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0fe04-120">-WhatIf</span></span>
<span data-ttu-id="0fe04-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fe04-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe04-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fe04-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe04-123">CommonParameters</span></span>
<span data-ttu-id="0fe04-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe04-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fe04-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe04-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fe04-126">INPUTS</span></span>

### <span data-ttu-id="0fe04-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe04-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fe04-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fe04-128">OUTPUTS</span></span>

### <span data-ttu-id="0fe04-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe04-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fe04-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fe04-130">NOTES</span></span>

## <span data-ttu-id="0fe04-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fe04-131">RELATED LINKS</span></span>

[<span data-ttu-id="0fe04-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0fe04-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0fe04-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0fe04-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0fe04-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0fe04-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0fe04-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0fe04-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)