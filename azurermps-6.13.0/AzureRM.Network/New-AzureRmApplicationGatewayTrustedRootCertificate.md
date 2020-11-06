---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505350"
---
# <span data-ttu-id="5e4e4-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e4e4-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="5e4e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4e4-103">Erstellt ein vertrauenswürdiges Stammzertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e4e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e4e4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e4e4-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4e4-106">Das Cmdlet **New-AzureRmApplicationGatewayTrustedRootCertificate** erstellt ein vertrauenswürdiges Stammzertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5e4e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e4e4-107">EXAMPLES</span></span>

### <span data-ttu-id="5e4e4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e4e4-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="5e4e4-109">Dieser Befehl erstellt ein vertrauenswürdiges Stammzertifikat mit dem Namen "trc1" und speichert das Ergebnis in der Variablen mit dem Namen $TRC.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="5e4e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e4e4-110">PARAMETERS</span></span>

### <span data-ttu-id="5e4e4-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="5e4e4-111">-CertificateFile</span></span>
<span data-ttu-id="5e4e4-112">Pfad der Zertifikat CER-Datei</span><span class="sxs-lookup"><span data-stu-id="5e4e4-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="5e4e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4e4-113">-DefaultProfile</span></span>
<span data-ttu-id="5e4e4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4e4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5e4e4-115">-Name</span></span>
<span data-ttu-id="5e4e4-116">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="5e4e4-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="5e4e4-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e4e4-117">-Confirm</span></span>
<span data-ttu-id="5e4e4-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4e4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4e4-119">-WhatIf</span></span>
<span data-ttu-id="5e4e4-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4e4-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4e4-122">CommonParameters</span></span>
<span data-ttu-id="5e4e4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4e4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4e4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4e4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e4e4-125">INPUTS</span></span>

### <span data-ttu-id="5e4e4-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5e4e4-126">None</span></span>

## <span data-ttu-id="5e4e4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e4e4-127">OUTPUTS</span></span>

### <span data-ttu-id="5e4e4-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e4e4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="5e4e4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e4e4-129">NOTES</span></span>

## <span data-ttu-id="5e4e4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e4e4-130">RELATED LINKS</span></span>
