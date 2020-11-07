---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: b6035e991b585ba296a9fdc591ccbdb44dd1b089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820027"
---
# <span data-ttu-id="f9b61-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f9b61-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="f9b61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9b61-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b61-103">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f9b61-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f9b61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b61-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9b61-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9b61-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b61-106">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f9b61-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f9b61-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9b61-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b61-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9b61-108">Example 1</span></span>
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

<span data-ttu-id="f9b61-109">Erstellen eines ManagedRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="f9b61-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="f9b61-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9b61-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b61-111">-DefaultProfile</span></span>
<span data-ttu-id="f9b61-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9b61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b61-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f9b61-113">-RuleGroupOverride</span></span>
<span data-ttu-id="f9b61-114">Liste der Überschreibung der Azure Managed Provider-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b61-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="f9b61-115">-Typ</span><span class="sxs-lookup"><span data-stu-id="f9b61-115">-Type</span></span>
<span data-ttu-id="f9b61-116">Der Typ des RuleSet</span><span class="sxs-lookup"><span data-stu-id="f9b61-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="f9b61-117">-Version</span><span class="sxs-lookup"><span data-stu-id="f9b61-117">-Version</span></span>
<span data-ttu-id="f9b61-118">Version des RuleSet</span><span class="sxs-lookup"><span data-stu-id="f9b61-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="f9b61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b61-119">CommonParameters</span></span>
<span data-ttu-id="f9b61-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b61-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b61-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b61-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9b61-122">INPUTS</span></span>

### <span data-ttu-id="f9b61-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f9b61-123">None</span></span>

## <span data-ttu-id="f9b61-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9b61-124">OUTPUTS</span></span>

### <span data-ttu-id="f9b61-125">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="f9b61-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="f9b61-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9b61-126">NOTES</span></span>

## <span data-ttu-id="f9b61-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9b61-127">RELATED LINKS</span></span>

<span data-ttu-id="f9b61-128">[Neu – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Satz-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Neu – AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="f9b61-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
