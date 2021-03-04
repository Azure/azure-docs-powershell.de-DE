---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950256"
---
# <span data-ttu-id="bdaef-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="bdaef-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="bdaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdaef-102">SYNOPSIS</span></span>
<span data-ttu-id="bdaef-103">Erstellen eines RuleGroupOverride-Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="bdaef-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="bdaef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdaef-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdaef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdaef-105">DESCRIPTION</span></span>
<span data-ttu-id="bdaef-106">Erstellen eines RuleGroupOverride-Objekts für die Erstellung einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="bdaef-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="bdaef-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdaef-107">EXAMPLES</span></span>

### <span data-ttu-id="bdaef-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdaef-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="bdaef-109">Erstellen eines RuleGroupOverride-Objekts</span><span class="sxs-lookup"><span data-stu-id="bdaef-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="bdaef-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bdaef-110">PARAMETERS</span></span>

### <span data-ttu-id="bdaef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdaef-111">-DefaultProfile</span></span>
<span data-ttu-id="bdaef-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdaef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdaef-113">-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="bdaef-113">-Exclusion</span></span>
<span data-ttu-id="bdaef-114">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="bdaef-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdaef-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bdaef-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="bdaef-116">Liste "Regelüberschreibung"</span><span class="sxs-lookup"><span data-stu-id="bdaef-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdaef-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="bdaef-117">-RuleGroupName</span></span>
<span data-ttu-id="bdaef-118">Regelgruppenname, für den diese Außerkraftsetzungen gelten</span><span class="sxs-lookup"><span data-stu-id="bdaef-118">Rule Group Name for which these overrides apply</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdaef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdaef-119">CommonParameters</span></span>
<span data-ttu-id="bdaef-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdaef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdaef-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdaef-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdaef-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdaef-122">INPUTS</span></span>

### <span data-ttu-id="bdaef-123">Keine</span><span class="sxs-lookup"><span data-stu-id="bdaef-123">None</span></span>

## <span data-ttu-id="bdaef-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdaef-124">OUTPUTS</span></span>

### <span data-ttu-id="bdaef-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bdaef-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="bdaef-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bdaef-126">NOTES</span></span>

## <span data-ttu-id="bdaef-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bdaef-127">RELATED LINKS</span></span>

[<span data-ttu-id="bdaef-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bdaef-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
