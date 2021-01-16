---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468111"
---
# <span data-ttu-id="40ef6-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="40ef6-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="40ef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="40ef6-103">Erstellt eine Übereinstimmungsvariable für die Firewallbedingung.</span><span class="sxs-lookup"><span data-stu-id="40ef6-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="40ef6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40ef6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ef6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="40ef6-106">**"New-AzApplicationGatewayFirewallMatchVariable"** erstellt eine Übereinstimmungsvariable für die Firewallbedingung.</span><span class="sxs-lookup"><span data-stu-id="40ef6-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="40ef6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="40ef6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40ef6-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="40ef6-109">Der Befehl erstellt eine neue Übereinstimmungsvariable mit dem Namen der Anforderungskopfzeilen, und die Auswahl ist das Feld "Inhaltslänge".</span><span class="sxs-lookup"><span data-stu-id="40ef6-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="40ef6-110">Die neue Übereinstimmungsvariable wird in $variable.</span><span class="sxs-lookup"><span data-stu-id="40ef6-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="40ef6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ef6-111">PARAMETERS</span></span>

### <span data-ttu-id="40ef6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ef6-112">-DefaultProfile</span></span>
<span data-ttu-id="40ef6-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40ef6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ef6-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="40ef6-114">-Selector</span></span>
<span data-ttu-id="40ef6-115">Beschreibt das Feld der Sammlung "matchVariable".</span><span class="sxs-lookup"><span data-stu-id="40ef6-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="40ef6-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="40ef6-116">-VariableName</span></span>
<span data-ttu-id="40ef6-117">"Variable variabel" aus.</span><span class="sxs-lookup"><span data-stu-id="40ef6-117">Match Variable.</span></span>

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

### <span data-ttu-id="40ef6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ef6-118">CommonParameters</span></span>
<span data-ttu-id="40ef6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ef6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ef6-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ef6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ef6-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40ef6-121">INPUTS</span></span>

### <span data-ttu-id="40ef6-122">Keine</span><span class="sxs-lookup"><span data-stu-id="40ef6-122">None</span></span>

## <span data-ttu-id="40ef6-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40ef6-123">OUTPUTS</span></span>

### <span data-ttu-id="40ef6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="40ef6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="40ef6-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40ef6-125">NOTES</span></span>

## <span data-ttu-id="40ef6-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40ef6-126">RELATED LINKS</span></span>
