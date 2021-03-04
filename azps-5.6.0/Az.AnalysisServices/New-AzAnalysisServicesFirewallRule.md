---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 4936571126a00d34fc91d2f7cbd85b232f18b4fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943176"
---
# <span data-ttu-id="9133d-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9133d-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="9133d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9133d-102">SYNOPSIS</span></span>
<span data-ttu-id="9133d-103">Erstellt eine neue Analysis Services-Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9133d-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="9133d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9133d-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9133d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9133d-105">DESCRIPTION</span></span>
<span data-ttu-id="9133d-106">Die New-AzAnalysisServicesFirewallRule erstellt ein neues Firewallregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="9133d-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="9133d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9133d-107">EXAMPLES</span></span>

### <span data-ttu-id="9133d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9133d-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="9133d-109">Erstellt eine Firewallregel namens Regel1 mit dem Startbereich 0.0.0.0 und dem Endbereich 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="9133d-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="9133d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9133d-110">PARAMETERS</span></span>

### <span data-ttu-id="9133d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9133d-111">-DefaultProfile</span></span>
<span data-ttu-id="9133d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9133d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9133d-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9133d-113">-FirewallRuleName</span></span>
<span data-ttu-id="9133d-114">Name der Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9133d-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="9133d-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="9133d-115">-RangeEnd</span></span>
<span data-ttu-id="9133d-116">Das Bereichsende einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9133d-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="9133d-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="9133d-117">-RangeStart</span></span>
<span data-ttu-id="9133d-118">Der Bereichsanfang einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9133d-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="9133d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9133d-119">CommonParameters</span></span>
<span data-ttu-id="9133d-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9133d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9133d-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9133d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9133d-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9133d-122">INPUTS</span></span>

### <span data-ttu-id="9133d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9133d-123">System.String</span></span>

## <span data-ttu-id="9133d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9133d-124">OUTPUTS</span></span>

### <span data-ttu-id="9133d-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9133d-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="9133d-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9133d-126">NOTES</span></span>

## <span data-ttu-id="9133d-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9133d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9133d-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9133d-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)