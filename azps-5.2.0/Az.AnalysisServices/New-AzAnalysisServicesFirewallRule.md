---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294155"
---
# <span data-ttu-id="107d6-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107d6-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="107d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107d6-102">SYNOPSIS</span></span>
<span data-ttu-id="107d6-103">Erstellt eine neue Analysis Services-Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="107d6-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="107d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="107d6-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="107d6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="107d6-105">DESCRIPTION</span></span>
<span data-ttu-id="107d6-106">Der New-AzAnalysisServicesFirewallRule erstellt ein neues Firewallregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="107d6-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="107d6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="107d6-107">EXAMPLES</span></span>

### <span data-ttu-id="107d6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="107d6-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="107d6-109">Erstellt eine Firewallregel namens "Regel1" mit dem Startbereich 0.0.0.0 und dem Endbereich 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="107d6-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="107d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="107d6-110">PARAMETERS</span></span>

### <span data-ttu-id="107d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107d6-111">-DefaultProfile</span></span>
<span data-ttu-id="107d6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="107d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107d6-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="107d6-113">-FirewallRuleName</span></span>
<span data-ttu-id="107d6-114">Name der Firewallregel</span><span class="sxs-lookup"><span data-stu-id="107d6-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107d6-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="107d6-115">-RangeEnd</span></span>
<span data-ttu-id="107d6-116">Das Ende des Bereichs einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="107d6-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107d6-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="107d6-117">-RangeStart</span></span>
<span data-ttu-id="107d6-118">Startbereich einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="107d6-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107d6-119">CommonParameters</span></span>
<span data-ttu-id="107d6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107d6-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107d6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107d6-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="107d6-122">INPUTS</span></span>

### <span data-ttu-id="107d6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="107d6-123">System.String</span></span>

## <span data-ttu-id="107d6-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="107d6-124">OUTPUTS</span></span>

### <span data-ttu-id="107d6-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="107d6-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="107d6-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="107d6-126">NOTES</span></span>

## <span data-ttu-id="107d6-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="107d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="107d6-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="107d6-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)