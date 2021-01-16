---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296219"
---
# <span data-ttu-id="a9974-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="a9974-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="a9974-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9974-102">SYNOPSIS</span></span>
<span data-ttu-id="a9974-103">Ruft die verfügbaren Fqdn-Tags für die Azure Firewall ab.</span><span class="sxs-lookup"><span data-stu-id="a9974-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="a9974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9974-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9974-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9974-105">DESCRIPTION</span></span>
<span data-ttu-id="a9974-106">Das **Cmdlet "Get-AzFirewallFqdnTag"** ruft die Liste der #A0 ab, die für #A1 verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a9974-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="a9974-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9974-107">EXAMPLES</span></span>

### <span data-ttu-id="a9974-108">1: Abrufen aller verfügbaren FQDN-Tags</span><span class="sxs-lookup"><span data-stu-id="a9974-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="a9974-109">In diesem Beispiel werden alle verfügbaren FQDN-Tags abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a9974-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="a9974-110">2: Verwenden des ersten verfügbaren FQDN-Tags in einer Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="a9974-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="a9974-111">In diesem Beispiel wird eine Firewallanwendungsregel mit dem ersten verfügbaren FQDN-Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9974-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="a9974-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9974-112">PARAMETERS</span></span>

### <span data-ttu-id="a9974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9974-113">-DefaultProfile</span></span>
<span data-ttu-id="a9974-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9974-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9974-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9974-115">CommonParameters</span></span>
<span data-ttu-id="a9974-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9974-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9974-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9974-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9974-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9974-118">INPUTS</span></span>

### <span data-ttu-id="a9974-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a9974-119">None</span></span>

## <span data-ttu-id="a9974-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9974-120">OUTPUTS</span></span>

### <span data-ttu-id="a9974-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="a9974-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="a9974-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a9974-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a9974-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9974-123">NOTES</span></span>

## <span data-ttu-id="a9974-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9974-124">RELATED LINKS</span></span>

[<span data-ttu-id="a9974-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="a9974-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="a9974-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a9974-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
