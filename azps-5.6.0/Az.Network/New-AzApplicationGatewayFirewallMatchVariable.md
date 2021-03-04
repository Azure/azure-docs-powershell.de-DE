---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950147"
---
# <span data-ttu-id="747f7-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="747f7-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="747f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="747f7-102">SYNOPSIS</span></span>
<span data-ttu-id="747f7-103">Erstellt eine Übereinstimmungsvariable für die Firewallbedingung.</span><span class="sxs-lookup"><span data-stu-id="747f7-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="747f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="747f7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="747f7-105">DESCRIPTION</span></span>
<span data-ttu-id="747f7-106">Die **New-AzApplicationGatewayFirewallMatchVariable** erstellt eine Übereinstimmungsvariable für die Firewallbedingung.</span><span class="sxs-lookup"><span data-stu-id="747f7-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="747f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="747f7-107">EXAMPLES</span></span>

### <span data-ttu-id="747f7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="747f7-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="747f7-109">Mit dem Befehl wird eine neue Übereinstimmungsvariable mit dem Namen der Anforderungsüberschriften erstellt, und die Auswahl ist das Feld Inhaltslänge.</span><span class="sxs-lookup"><span data-stu-id="747f7-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="747f7-110">Die neue Übereinstimmungsvariable wird in $variable.</span><span class="sxs-lookup"><span data-stu-id="747f7-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="747f7-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="747f7-111">PARAMETERS</span></span>

### <span data-ttu-id="747f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747f7-112">-DefaultProfile</span></span>
<span data-ttu-id="747f7-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="747f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="747f7-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="747f7-114">-Selector</span></span>
<span data-ttu-id="747f7-115">Beschreibt das Feld der matchVariable-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="747f7-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="747f7-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="747f7-116">-VariableName</span></span>
<span data-ttu-id="747f7-117">Variable übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="747f7-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="747f7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747f7-118">CommonParameters</span></span>
<span data-ttu-id="747f7-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747f7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747f7-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747f7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747f7-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="747f7-121">INPUTS</span></span>

### <span data-ttu-id="747f7-122">Keine</span><span class="sxs-lookup"><span data-stu-id="747f7-122">None</span></span>

## <span data-ttu-id="747f7-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="747f7-123">OUTPUTS</span></span>

### <span data-ttu-id="747f7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="747f7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="747f7-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="747f7-125">NOTES</span></span>

## <span data-ttu-id="747f7-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="747f7-126">RELATED LINKS</span></span>
