---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921088"
---
# <span data-ttu-id="88127-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="88127-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="88127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88127-102">SYNOPSIS</span></span>
<span data-ttu-id="88127-103">Ruft die verfügbaren Azure Firewall-Fqdn-Tags ab.</span><span class="sxs-lookup"><span data-stu-id="88127-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="88127-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88127-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88127-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88127-105">DESCRIPTION</span></span>
<span data-ttu-id="88127-106">Das **Cmdlet Get-AzFirewallFqdnTag** ruft die Liste der FQDN-Tags ab, die für #A0 verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="88127-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="88127-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88127-107">EXAMPLES</span></span>

### <span data-ttu-id="88127-108">1: Abrufen aller verfügbaren FQDN-Tags</span><span class="sxs-lookup"><span data-stu-id="88127-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="88127-109">In diesem Beispiel werden alle verfügbaren FQDN-Tags abgerufen.</span><span class="sxs-lookup"><span data-stu-id="88127-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="88127-110">2: Verwenden des ersten verfügbaren FQDN-Tags in einer Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="88127-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="88127-111">In diesem Beispiel wird eine Firewallanwendungsregel mit dem ersten verfügbaren FQDN-Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="88127-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="88127-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88127-112">PARAMETERS</span></span>

### <span data-ttu-id="88127-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88127-113">-DefaultProfile</span></span>
<span data-ttu-id="88127-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88127-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88127-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88127-115">CommonParameters</span></span>
<span data-ttu-id="88127-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88127-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88127-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88127-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88127-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88127-118">INPUTS</span></span>

### <span data-ttu-id="88127-119">Keine</span><span class="sxs-lookup"><span data-stu-id="88127-119">None</span></span>

## <span data-ttu-id="88127-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88127-120">OUTPUTS</span></span>

### <span data-ttu-id="88127-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="88127-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="88127-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="88127-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="88127-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88127-123">NOTES</span></span>

## <span data-ttu-id="88127-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88127-124">RELATED LINKS</span></span>

[<span data-ttu-id="88127-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="88127-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="88127-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="88127-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
