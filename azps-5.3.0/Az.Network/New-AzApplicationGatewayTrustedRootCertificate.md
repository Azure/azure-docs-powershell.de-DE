---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379251"
---
# <span data-ttu-id="d952b-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d952b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d952b-102">SYNOPSIS</span></span>
<span data-ttu-id="d952b-103">Erstellt ein vertrauenswürdiges Stammzertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d952b-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="d952b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d952b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d952b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d952b-105">DESCRIPTION</span></span>
<span data-ttu-id="d952b-106">Das **Cmdlet "New-AzApplicationGatewayTrustedRootCertificate"** erstellt ein vertrauenswürdiges Stammzertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d952b-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d952b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d952b-107">EXAMPLES</span></span>

### <span data-ttu-id="d952b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d952b-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="d952b-109">Mit diesem Befehl wird ein vertrauenswürdiges Stammzertifikat namens "trc1" erstellt und das Ergebnis in der Variablen namens "$trc.</span><span class="sxs-lookup"><span data-stu-id="d952b-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="d952b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d952b-110">PARAMETERS</span></span>

### <span data-ttu-id="d952b-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d952b-111">-CertificateFile</span></span>
<span data-ttu-id="d952b-112">Pfad der Zertifikat-CER-Datei</span><span class="sxs-lookup"><span data-stu-id="d952b-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="d952b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d952b-113">-DefaultProfile</span></span>
<span data-ttu-id="d952b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d952b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d952b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d952b-115">-Name</span></span>
<span data-ttu-id="d952b-116">Der Name des Zertifikats "TrustedRoot"</span><span class="sxs-lookup"><span data-stu-id="d952b-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d952b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d952b-117">-Confirm</span></span>
<span data-ttu-id="d952b-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d952b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d952b-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d952b-119">-WhatIf</span></span>
<span data-ttu-id="d952b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d952b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d952b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d952b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d952b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d952b-122">CommonParameters</span></span>
<span data-ttu-id="d952b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d952b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d952b-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d952b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d952b-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d952b-125">INPUTS</span></span>

### <span data-ttu-id="d952b-126">Keine</span><span class="sxs-lookup"><span data-stu-id="d952b-126">None</span></span>

## <span data-ttu-id="d952b-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d952b-127">OUTPUTS</span></span>

### <span data-ttu-id="d952b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d952b-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d952b-129">NOTES</span></span>

## <span data-ttu-id="d952b-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d952b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d952b-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d952b-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d952b-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d952b-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d952b-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
