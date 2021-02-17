---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: c72573f467377a4ea16fd487a8cee5f0055a5cee
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401452"
---
# <span data-ttu-id="7e962-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7e962-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="7e962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e962-102">SYNOPSIS</span></span>
<span data-ttu-id="7e962-103">Create ManagedRule Object for WAF policy creation</span><span class="sxs-lookup"><span data-stu-id="7e962-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="7e962-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e962-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e962-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e962-105">DESCRIPTION</span></span>
<span data-ttu-id="7e962-106">Create ManagedRule Object for WAF policy creation</span><span class="sxs-lookup"><span data-stu-id="7e962-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="7e962-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e962-107">EXAMPLES</span></span>

### <span data-ttu-id="7e962-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e962-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="7e962-109">Erstellen eines Objekts vomTyp "ManagedRule"</span><span class="sxs-lookup"><span data-stu-id="7e962-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="7e962-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e962-110">PARAMETERS</span></span>

### <span data-ttu-id="7e962-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e962-111">-DefaultProfile</span></span>
<span data-ttu-id="7e962-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e962-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e962-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7e962-113">-RuleGroupOverride</span></span>
<span data-ttu-id="7e962-114">Liste der Konfiguration zur Außerkraftsetzung eines azure-verwalteten Anbieters</span><span class="sxs-lookup"><span data-stu-id="7e962-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="7e962-115">-Type</span><span class="sxs-lookup"><span data-stu-id="7e962-115">-Type</span></span>
<span data-ttu-id="7e962-116">Regelsatztyp</span><span class="sxs-lookup"><span data-stu-id="7e962-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="7e962-117">-Version</span><span class="sxs-lookup"><span data-stu-id="7e962-117">-Version</span></span>
<span data-ttu-id="7e962-118">Version des Ruleset</span><span class="sxs-lookup"><span data-stu-id="7e962-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="7e962-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e962-119">CommonParameters</span></span>
<span data-ttu-id="7e962-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e962-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e962-121">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e962-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e962-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e962-122">INPUTS</span></span>

### <span data-ttu-id="7e962-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7e962-123">None</span></span>

## <span data-ttu-id="7e962-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e962-124">OUTPUTS</span></span>

### <span data-ttu-id="7e962-125">Microsoft.Azure.Commands.FrontDando.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="7e962-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="7e962-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7e962-126">NOTES</span></span>

## <span data-ttu-id="7e962-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7e962-127">RELATED LINKS</span></span>

<span data-ttu-id="7e962-128">[New-AzFrontD firewallWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontD firewallWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDuleRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="7e962-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
