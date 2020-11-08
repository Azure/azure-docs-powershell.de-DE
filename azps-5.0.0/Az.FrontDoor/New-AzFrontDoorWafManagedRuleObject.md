---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177604"
---
# <span data-ttu-id="50c0f-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="50c0f-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="50c0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="50c0f-103">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="50c0f-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="50c0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c0f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="50c0f-106">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="50c0f-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="50c0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="50c0f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50c0f-108">Example 1</span></span>
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

<span data-ttu-id="50c0f-109">Erstellen eines ManagedRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="50c0f-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="50c0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50c0f-110">PARAMETERS</span></span>

### <span data-ttu-id="50c0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c0f-111">-DefaultProfile</span></span>
<span data-ttu-id="50c0f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50c0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50c0f-113">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="50c0f-113">-Exclusion</span></span>
<span data-ttu-id="50c0f-114">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="50c0f-114">Exclusion</span></span>

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

### <span data-ttu-id="50c0f-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="50c0f-115">-RuleGroupOverride</span></span>
<span data-ttu-id="50c0f-116">Liste der Überschreibung der Azure Managed Provider-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="50c0f-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="50c0f-117">-Typ</span><span class="sxs-lookup"><span data-stu-id="50c0f-117">-Type</span></span>
<span data-ttu-id="50c0f-118">Der Typ des RuleSet</span><span class="sxs-lookup"><span data-stu-id="50c0f-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="50c0f-119">-Version</span><span class="sxs-lookup"><span data-stu-id="50c0f-119">-Version</span></span>
<span data-ttu-id="50c0f-120">Version des RuleSet</span><span class="sxs-lookup"><span data-stu-id="50c0f-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="50c0f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c0f-121">CommonParameters</span></span>
<span data-ttu-id="50c0f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c0f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c0f-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50c0f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c0f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50c0f-124">INPUTS</span></span>

### <span data-ttu-id="50c0f-125">Keine</span><span class="sxs-lookup"><span data-stu-id="50c0f-125">None</span></span>

## <span data-ttu-id="50c0f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50c0f-126">OUTPUTS</span></span>

### <span data-ttu-id="50c0f-127">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="50c0f-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="50c0f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="50c0f-128">NOTES</span></span>

## <span data-ttu-id="50c0f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50c0f-129">RELATED LINKS</span></span>

<span data-ttu-id="50c0f-130">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Neu – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="50c0f-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
