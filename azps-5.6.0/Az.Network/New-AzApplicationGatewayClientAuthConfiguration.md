---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925443"
---
# <span data-ttu-id="43d1d-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="43d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="43d1d-103">Erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="43d1d-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="43d1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43d1d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d1d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="43d1d-106">Das **Cmdlet New-AzApplicationGatewayClientAuthConfiguration** erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="43d1d-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="43d1d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="43d1d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43d1d-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="43d1d-109">Der Befehl erstellt eine neue Client-Authentifizierungskonfiguration und speichert sie in $clientAuthConfig, die in einem SSL-Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d1d-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="43d1d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="43d1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d1d-111">-DefaultProfile</span></span>
<span data-ttu-id="43d1d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43d1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d1d-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="43d1d-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="43d1d-114">Überprüfen Sie den Namen des Ausstellers des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="43d1d-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d1d-115">CommonParameters</span></span>
<span data-ttu-id="43d1d-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d1d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d1d-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43d1d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d1d-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43d1d-118">INPUTS</span></span>

### <span data-ttu-id="43d1d-119">Keine</span><span class="sxs-lookup"><span data-stu-id="43d1d-119">None</span></span>

## <span data-ttu-id="43d1d-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43d1d-120">OUTPUTS</span></span>

### <span data-ttu-id="43d1d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="43d1d-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43d1d-122">NOTES</span></span>

## <span data-ttu-id="43d1d-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43d1d-123">RELATED LINKS</span></span>

[<span data-ttu-id="43d1d-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="43d1d-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="43d1d-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="43d1d-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d1d-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)