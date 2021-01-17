---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379530"
---
# <span data-ttu-id="653cc-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="653cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="653cc-102">SYNOPSIS</span></span>
<span data-ttu-id="653cc-103">Erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="653cc-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="653cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="653cc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="653cc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="653cc-105">DESCRIPTION</span></span>
<span data-ttu-id="653cc-106">Das **Cmdlet "New-AzApplicationGatewayClientAuthConfiguration"** erstellt eine neue Clientauthentifizierungskonfiguration für das SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="653cc-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="653cc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="653cc-107">EXAMPLES</span></span>

### <span data-ttu-id="653cc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="653cc-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="653cc-109">Der Befehl erstellt eine neue Client-Authentifizierungskonfiguration und speichert sie in $clientAuthConfig A0 zur Verwendung in einem SSL-Profil.</span><span class="sxs-lookup"><span data-stu-id="653cc-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="653cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="653cc-110">PARAMETERS</span></span>

### <span data-ttu-id="653cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653cc-111">-DefaultProfile</span></span>
<span data-ttu-id="653cc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="653cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="653cc-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="653cc-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="653cc-114">Überprüfen Sie den Ausstellernamen des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="653cc-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="653cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653cc-115">CommonParameters</span></span>
<span data-ttu-id="653cc-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="653cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653cc-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="653cc-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653cc-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="653cc-118">INPUTS</span></span>

### <span data-ttu-id="653cc-119">Keine</span><span class="sxs-lookup"><span data-stu-id="653cc-119">None</span></span>

## <span data-ttu-id="653cc-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="653cc-120">OUTPUTS</span></span>

### <span data-ttu-id="653cc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="653cc-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="653cc-122">NOTES</span></span>

## <span data-ttu-id="653cc-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="653cc-123">RELATED LINKS</span></span>

[<span data-ttu-id="653cc-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="653cc-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="653cc-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="653cc-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="653cc-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)