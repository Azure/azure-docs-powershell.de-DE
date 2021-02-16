---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 44fe7da11f3a06d7938f084b0edf6a6a39bb30f5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412757"
---
# <span data-ttu-id="67d10-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="67d10-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="67d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d10-102">SYNOPSIS</span></span>
<span data-ttu-id="67d10-103">Create ManagedRule Object for WAF policy creation</span><span class="sxs-lookup"><span data-stu-id="67d10-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="67d10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67d10-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67d10-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67d10-105">DESCRIPTION</span></span>
<span data-ttu-id="67d10-106">Create ManagedRule Object for WAF policy creation</span><span class="sxs-lookup"><span data-stu-id="67d10-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="67d10-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67d10-107">EXAMPLES</span></span>

### <span data-ttu-id="67d10-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67d10-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="67d10-109">Erstellen eines Objekts vomTyp "ManagedRule"</span><span class="sxs-lookup"><span data-stu-id="67d10-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="67d10-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d10-110">PARAMETERS</span></span>

### <span data-ttu-id="67d10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d10-111">-DefaultProfile</span></span>
<span data-ttu-id="67d10-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67d10-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d10-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="67d10-113">-RuleGroupOverride</span></span>
<span data-ttu-id="67d10-114">Liste der Konfiguration zur Außerkraftsetzung eines azure-verwalteten Anbieters</span><span class="sxs-lookup"><span data-stu-id="67d10-114">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d10-115">-Type</span><span class="sxs-lookup"><span data-stu-id="67d10-115">-Type</span></span>
<span data-ttu-id="67d10-116">Regelsatztyp</span><span class="sxs-lookup"><span data-stu-id="67d10-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="67d10-117">-Version</span><span class="sxs-lookup"><span data-stu-id="67d10-117">-Version</span></span>
<span data-ttu-id="67d10-118">Version des Ruleset</span><span class="sxs-lookup"><span data-stu-id="67d10-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="67d10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d10-119">CommonParameters</span></span>
<span data-ttu-id="67d10-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d10-121">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d10-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d10-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67d10-122">INPUTS</span></span>

### <span data-ttu-id="67d10-123">Keine</span><span class="sxs-lookup"><span data-stu-id="67d10-123">None</span></span>

## <span data-ttu-id="67d10-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67d10-124">OUTPUTS</span></span>

### <span data-ttu-id="67d10-125">Microsoft.Azure.Commands.FrontDando.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="67d10-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="67d10-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67d10-126">NOTES</span></span>

## <span data-ttu-id="67d10-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67d10-127">RELATED LINKS</span></span>

<span data-ttu-id="67d10-128">[New-AzFrontDlicWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDullWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="67d10-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
