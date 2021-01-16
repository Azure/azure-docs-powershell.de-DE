---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295282"
---
# <span data-ttu-id="e4f67-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="e4f67-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="e4f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f67-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f67-103">Objekt zum Außerkraftsetzungsobjekt für verwaltete Regeln erstellen</span><span class="sxs-lookup"><span data-stu-id="e4f67-103">Create managed rule override object</span></span>

## <span data-ttu-id="e4f67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4f67-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4f67-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f67-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f67-106">Erstellen Sie ein PSAzureManagedRuleOverride-Objekt für verwaltete WAF-Regelgruppen, die die Objekterstellung außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="e4f67-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="e4f67-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4f67-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f67-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4f67-108">Example 1</span></span>
<span data-ttu-id="e4f67-109">Erstellen Sie ein Überschreibungsobjekt für verwaltete Regeln für Regel 942250 (in der SQLI-Gruppe).</span><span class="sxs-lookup"><span data-stu-id="e4f67-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="e4f67-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4f67-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f67-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="e4f67-111">-Action</span></span>
<span data-ttu-id="e4f67-112">Aktion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="e4f67-112">Override Action</span></span>

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

### <span data-ttu-id="e4f67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f67-113">-DefaultProfile</span></span>
<span data-ttu-id="e4f67-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4f67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f67-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="e4f67-115">-Disabled</span></span>
<span data-ttu-id="e4f67-116">Status "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="e4f67-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f67-117">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="e4f67-117">-Exclusion</span></span>
<span data-ttu-id="e4f67-118">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="e4f67-118">Exclusion</span></span>

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

### <span data-ttu-id="e4f67-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="e4f67-119">-RuleId</span></span>
<span data-ttu-id="e4f67-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="e4f67-120">Rule ID</span></span>

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

### <span data-ttu-id="e4f67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f67-121">CommonParameters</span></span>
<span data-ttu-id="e4f67-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f67-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4f67-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f67-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4f67-124">INPUTS</span></span>

### <span data-ttu-id="e4f67-125">Keine</span><span class="sxs-lookup"><span data-stu-id="e4f67-125">None</span></span>

## <span data-ttu-id="e4f67-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4f67-126">OUTPUTS</span></span>

### <span data-ttu-id="e4f67-127">Microsoft.Azure.Commands.FrontDando.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e4f67-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="e4f67-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4f67-128">NOTES</span></span>

## <span data-ttu-id="e4f67-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4f67-129">RELATED LINKS</span></span>

[<span data-ttu-id="e4f67-130">New-AzFrontDullWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="e4f67-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)