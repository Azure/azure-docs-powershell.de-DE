---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173780"
---
# <span data-ttu-id="a9204-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a9204-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="a9204-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9204-102">SYNOPSIS</span></span>
<span data-ttu-id="a9204-103">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts</span><span class="sxs-lookup"><span data-stu-id="a9204-103">Create managed rule override object</span></span>

## <span data-ttu-id="a9204-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9204-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9204-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9204-105">DESCRIPTION</span></span>
<span data-ttu-id="a9204-106">Erstellen eines PSAzureManagedRuleOverride-Objekts für verwaltete WAF-Regelgruppe außer Kraft setzen der Objekterstellung.</span><span class="sxs-lookup"><span data-stu-id="a9204-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="a9204-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9204-107">EXAMPLES</span></span>

### <span data-ttu-id="a9204-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9204-108">Example 1</span></span>
<span data-ttu-id="a9204-109">Erstellen eines verwalteten Regel Außerkraftsetzungs Objekts für Regel 942250 (in der SQLI-Gruppe)</span><span class="sxs-lookup"><span data-stu-id="a9204-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="a9204-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9204-110">PARAMETERS</span></span>

### <span data-ttu-id="a9204-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="a9204-111">-Action</span></span>
<span data-ttu-id="a9204-112">Aktion überschreiben</span><span class="sxs-lookup"><span data-stu-id="a9204-112">Override Action</span></span>

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

### <span data-ttu-id="a9204-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9204-113">-DefaultProfile</span></span>
<span data-ttu-id="a9204-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9204-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9204-115">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="a9204-115">-Disabled</span></span>
<span data-ttu-id="a9204-116">Deaktivierter Zustand</span><span class="sxs-lookup"><span data-stu-id="a9204-116">Disabled state</span></span>

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

### <span data-ttu-id="a9204-117">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="a9204-117">-Exclusion</span></span>
<span data-ttu-id="a9204-118">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="a9204-118">Exclusion</span></span>

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

### <span data-ttu-id="a9204-119">-Lineal</span><span class="sxs-lookup"><span data-stu-id="a9204-119">-RuleId</span></span>
<span data-ttu-id="a9204-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="a9204-120">Rule ID</span></span>

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

### <span data-ttu-id="a9204-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9204-121">CommonParameters</span></span>
<span data-ttu-id="a9204-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9204-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9204-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9204-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9204-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9204-124">INPUTS</span></span>

### <span data-ttu-id="a9204-125">Keine</span><span class="sxs-lookup"><span data-stu-id="a9204-125">None</span></span>

## <span data-ttu-id="a9204-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9204-126">OUTPUTS</span></span>

### <span data-ttu-id="a9204-127">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a9204-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="a9204-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9204-128">NOTES</span></span>

## <span data-ttu-id="a9204-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9204-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9204-130">Neu – AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a9204-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)