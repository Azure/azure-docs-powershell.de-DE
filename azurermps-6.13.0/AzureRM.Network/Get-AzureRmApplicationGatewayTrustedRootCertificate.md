---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663657"
---
# <span data-ttu-id="d145f-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d145f-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d145f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d145f-102">SYNOPSIS</span></span>
<span data-ttu-id="d145f-103">Ruft das vertrauenswürdige Stammzertifikat mit einem bestimmten Namen aus dem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="d145f-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d145f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d145f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d145f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d145f-105">DESCRIPTION</span></span>
<span data-ttu-id="d145f-106">Das Cmdlet " **Get-AzureRmApplicationGatewayTrustedRootCertificate** " Ruft ein vertrauenswürdiges Stammzertifikat mit einem bestimmten Namen vom Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="d145f-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="d145f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d145f-107">EXAMPLES</span></span>

### <span data-ttu-id="d145f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d145f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="d145f-109">Der erste Befehl ruft das Anwendungs Gateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="d145f-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d145f-110">Der zweite Befehl ruft das vertrauenswürdige Stammzertifikat mit einem angegebenen Namen aus dem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="d145f-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="d145f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d145f-111">PARAMETERS</span></span>

### <span data-ttu-id="d145f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d145f-112">-ApplicationGateway</span></span>
<span data-ttu-id="d145f-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d145f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d145f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d145f-114">-DefaultProfile</span></span>
<span data-ttu-id="d145f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d145f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d145f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d145f-116">-Name</span></span>
<span data-ttu-id="d145f-117">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d145f-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d145f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d145f-118">CommonParameters</span></span>
<span data-ttu-id="d145f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d145f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d145f-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d145f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d145f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d145f-121">INPUTS</span></span>

### <span data-ttu-id="d145f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d145f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d145f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d145f-123">OUTPUTS</span></span>

### <span data-ttu-id="d145f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d145f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d145f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d145f-125">NOTES</span></span>

## <span data-ttu-id="d145f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d145f-126">RELATED LINKS</span></span>
