---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302219"
---
# <span data-ttu-id="0d09c-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d09c-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="0d09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d09c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d09c-103">Fügt einem Anwendungsgateway eine Zertifikatkette einer vertrauenswürdigen Client-Zertifizierungsstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d09c-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="0d09c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d09c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d09c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d09c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d09c-106">Das **Cmdlet "Add-AzApplicationGatewayTrustedClientCertificate"** fügt einem Azure-Anwendungsgateway eine Zertifikatkette einer vertrauenswürdigen Client-Zertifizierungsstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d09c-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="0d09c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d09c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d09c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d09c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0d09c-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="0d09c-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="0d09c-110">Mit dem zweiten Befehl wird eine Zertifikatkette für eine neue vertrauenswürdige Client-Zertifizierungsstelle erstellt, die den Pfad des Zertifikats der Client-Zertifizierungsstelle als Eingabe übernimmt.</span><span class="sxs-lookup"><span data-stu-id="0d09c-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="0d09c-111">Der dritte Befehl erstellt mithilfe eines vertrauenswürdigen Clientzertifikats ein SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="0d09c-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="0d09c-112">Mit dem vierten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0d09c-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="0d09c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d09c-113">PARAMETERS</span></span>

### <span data-ttu-id="0d09c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d09c-114">-ApplicationGateway</span></span>
<span data-ttu-id="0d09c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d09c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="0d09c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0d09c-116">-CertificateFile</span></span>
<span data-ttu-id="0d09c-117">Pfad der Zertifikatkettendatei der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="0d09c-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="0d09c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d09c-118">-DefaultProfile</span></span>
<span data-ttu-id="0d09c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d09c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d09c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d09c-120">-Name</span></span>
<span data-ttu-id="0d09c-121">Der Name der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="0d09c-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="0d09c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d09c-122">-Confirm</span></span>
<span data-ttu-id="0d09c-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d09c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d09c-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0d09c-124">-WhatIf</span></span>
<span data-ttu-id="0d09c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d09c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d09c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d09c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d09c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d09c-127">CommonParameters</span></span>
<span data-ttu-id="0d09c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d09c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d09c-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d09c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d09c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d09c-130">INPUTS</span></span>

### <span data-ttu-id="0d09c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d09c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d09c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d09c-132">OUTPUTS</span></span>

### <span data-ttu-id="0d09c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d09c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d09c-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d09c-134">NOTES</span></span>

## <span data-ttu-id="0d09c-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d09c-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d09c-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d09c-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0d09c-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d09c-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0d09c-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d09c-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0d09c-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d09c-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)