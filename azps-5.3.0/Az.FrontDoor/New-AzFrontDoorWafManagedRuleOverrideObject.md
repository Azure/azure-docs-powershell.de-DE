---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458624"
---
# <span data-ttu-id="9385a-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="9385a-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="9385a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9385a-102">SYNOPSIS</span></span>
<span data-ttu-id="9385a-103">Objekt zum Außerkraftsetzungsobjekt für verwaltete Regeln erstellen</span><span class="sxs-lookup"><span data-stu-id="9385a-103">Create managed rule override object</span></span>

## <span data-ttu-id="9385a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9385a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9385a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9385a-105">DESCRIPTION</span></span>
<span data-ttu-id="9385a-106">Erstellen Sie ein PSAzureManagedRuleOverride-Objekt für verwaltete WAF-Regelgruppen, die die Objekterstellung überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9385a-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="9385a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9385a-107">EXAMPLES</span></span>

### <span data-ttu-id="9385a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9385a-108">Example 1</span></span>
<span data-ttu-id="9385a-109">Erstellen Sie ein Überschreibungsobjekt für verwaltete Regeln für Regel 942250 (in der SQLI-Gruppe).</span><span class="sxs-lookup"><span data-stu-id="9385a-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="9385a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9385a-110">PARAMETERS</span></span>

### <span data-ttu-id="9385a-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="9385a-111">-Action</span></span>
<span data-ttu-id="9385a-112">Aktion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="9385a-112">Override Action</span></span>

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

### <span data-ttu-id="9385a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9385a-113">-DefaultProfile</span></span>
<span data-ttu-id="9385a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9385a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9385a-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="9385a-115">-Disabled</span></span>
<span data-ttu-id="9385a-116">Status "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="9385a-116">Disabled state</span></span>

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

### <span data-ttu-id="9385a-117">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="9385a-117">-Exclusion</span></span>
<span data-ttu-id="9385a-118">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="9385a-118">Exclusion</span></span>

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

### <span data-ttu-id="9385a-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="9385a-119">-RuleId</span></span>
<span data-ttu-id="9385a-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="9385a-120">Rule ID</span></span>

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

### <span data-ttu-id="9385a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9385a-121">CommonParameters</span></span>
<span data-ttu-id="9385a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9385a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9385a-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9385a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9385a-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9385a-124">INPUTS</span></span>

### <span data-ttu-id="9385a-125">Keine</span><span class="sxs-lookup"><span data-stu-id="9385a-125">None</span></span>

## <span data-ttu-id="9385a-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9385a-126">OUTPUTS</span></span>

### <span data-ttu-id="9385a-127">Microsoft.Azure.Commands.FrontDando.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="9385a-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="9385a-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9385a-128">NOTES</span></span>

## <span data-ttu-id="9385a-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9385a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9385a-130">New-AzFrontD dannWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="9385a-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)