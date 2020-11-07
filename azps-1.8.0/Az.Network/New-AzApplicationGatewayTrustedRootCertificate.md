---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: fff1e9190edda9ca5de12da66a2a138aa481ac7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660580"
---
# <span data-ttu-id="408ce-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="408ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="408ce-102">SYNOPSIS</span></span>
<span data-ttu-id="408ce-103">Erstellt ein vertrauenswürdiges Stammzertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="408ce-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="408ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="408ce-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="408ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="408ce-105">DESCRIPTION</span></span>
<span data-ttu-id="408ce-106">Das Cmdlet **New-AzApplicationGatewayTrustedRootCertificate** erstellt ein vertrauenswürdiges Stammzertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="408ce-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="408ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="408ce-107">EXAMPLES</span></span>

### <span data-ttu-id="408ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="408ce-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="408ce-109">Dieser Befehl erstellt ein vertrauenswürdiges Stammzertifikat mit dem Namen "trc1" und speichert das Ergebnis in der Variablen mit dem Namen $TRC.</span><span class="sxs-lookup"><span data-stu-id="408ce-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="408ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="408ce-110">PARAMETERS</span></span>

### <span data-ttu-id="408ce-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="408ce-111">-CertificateFile</span></span>
<span data-ttu-id="408ce-112">Pfad der Zertifikat CER-Datei</span><span class="sxs-lookup"><span data-stu-id="408ce-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="408ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408ce-113">-DefaultProfile</span></span>
<span data-ttu-id="408ce-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="408ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408ce-115">-Name</span><span class="sxs-lookup"><span data-stu-id="408ce-115">-Name</span></span>
<span data-ttu-id="408ce-116">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="408ce-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="408ce-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="408ce-117">-Confirm</span></span>
<span data-ttu-id="408ce-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="408ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408ce-119">-WhatIf</span></span>
<span data-ttu-id="408ce-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="408ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408ce-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="408ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408ce-122">CommonParameters</span></span>
<span data-ttu-id="408ce-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408ce-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408ce-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="408ce-125">INPUTS</span></span>

### <span data-ttu-id="408ce-126">Keine</span><span class="sxs-lookup"><span data-stu-id="408ce-126">None</span></span>

## <span data-ttu-id="408ce-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="408ce-127">OUTPUTS</span></span>

### <span data-ttu-id="408ce-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="408ce-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="408ce-129">NOTES</span></span>

## <span data-ttu-id="408ce-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="408ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="408ce-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="408ce-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="408ce-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="408ce-134">Satz-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="408ce-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
