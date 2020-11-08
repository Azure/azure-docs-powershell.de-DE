---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174583"
---
# <span data-ttu-id="e4ae9-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e4ae9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ae9-103">Erstellt ein vertrauenswürdiges Stammzertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="e4ae9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ae9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ae9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4ae9-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ae9-106">Das Cmdlet **New-AzApplicationGatewayTrustedRootCertificate** erstellt ein vertrauenswürdiges Stammzertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e4ae9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4ae9-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ae9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4ae9-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="e4ae9-109">Dieser Befehl erstellt ein vertrauenswürdiges Stammzertifikat mit dem Namen "trc1" und speichert das Ergebnis in der Variablen mit dem Namen $TRC.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="e4ae9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4ae9-110">PARAMETERS</span></span>

### <span data-ttu-id="e4ae9-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="e4ae9-111">-CertificateFile</span></span>
<span data-ttu-id="e4ae9-112">Pfad der Zertifikat CER-Datei</span><span class="sxs-lookup"><span data-stu-id="e4ae9-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e4ae9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ae9-113">-DefaultProfile</span></span>
<span data-ttu-id="e4ae9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4ae9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e4ae9-115">-Name</span></span>
<span data-ttu-id="e4ae9-116">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="e4ae9-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e4ae9-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4ae9-117">-Confirm</span></span>
<span data-ttu-id="e4ae9-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ae9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ae9-119">-WhatIf</span></span>
<span data-ttu-id="e4ae9-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4ae9-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4ae9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ae9-122">CommonParameters</span></span>
<span data-ttu-id="e4ae9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ae9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ae9-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ae9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ae9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4ae9-125">INPUTS</span></span>

### <span data-ttu-id="e4ae9-126">Keine</span><span class="sxs-lookup"><span data-stu-id="e4ae9-126">None</span></span>

## <span data-ttu-id="e4ae9-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4ae9-127">OUTPUTS</span></span>

### <span data-ttu-id="e4ae9-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e4ae9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4ae9-129">NOTES</span></span>

## <span data-ttu-id="e4ae9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4ae9-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4ae9-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e4ae9-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e4ae9-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e4ae9-134">Satz-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e4ae9-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
