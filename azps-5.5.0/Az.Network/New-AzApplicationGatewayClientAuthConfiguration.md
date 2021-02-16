---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 68ab3fbd87e5fe28fffdd0f6d769fb21d0ce9e6e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398086"
---
# <span data-ttu-id="8739a-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8739a-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="8739a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8739a-102">SYNOPSIS</span></span>
<span data-ttu-id="8739a-103">Erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="8739a-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="8739a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8739a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8739a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8739a-105">DESCRIPTION</span></span>
<span data-ttu-id="8739a-106">Das **Cmdlet "New-AzApplicationGatewayClientAuthConfiguration"** erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="8739a-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="8739a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8739a-107">EXAMPLES</span></span>

### <span data-ttu-id="8739a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8739a-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="8739a-109">Der Befehl erstellt eine neue Client-Authentifizierungskonfiguration und speichert sie in $clientAuthConfig A0 zur Verwendung in einem SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="8739a-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="8739a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8739a-110">PARAMETERS</span></span>

### <span data-ttu-id="8739a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8739a-111">-DefaultProfile</span></span>
<span data-ttu-id="8739a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8739a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8739a-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="8739a-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="8739a-114">Überprüfen Sie den Ausstellernamen des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="8739a-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="8739a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8739a-115">CommonParameters</span></span>
<span data-ttu-id="8739a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8739a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8739a-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8739a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8739a-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8739a-118">INPUTS</span></span>

### <span data-ttu-id="8739a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="8739a-119">None</span></span>

## <span data-ttu-id="8739a-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8739a-120">OUTPUTS</span></span>

### <span data-ttu-id="8739a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8739a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="8739a-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8739a-122">NOTES</span></span>

## <span data-ttu-id="8739a-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8739a-123">RELATED LINKS</span></span>


[<span data-ttu-id="8739a-124">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8739a-124">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8739a-125">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8739a-125">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8739a-126">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8739a-126">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
