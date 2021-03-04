---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928040"
---
# <span data-ttu-id="dd79d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="dd79d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="dd79d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd79d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd79d-103">Erstellen eines Überschreibungsobjekts für verwaltete Regeln</span><span class="sxs-lookup"><span data-stu-id="dd79d-103">Create managed rule override object</span></span>

## <span data-ttu-id="dd79d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd79d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd79d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd79d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd79d-106">Erstellen Sie PSAzureManagedRuleOverride-Objekt für verwaltete WAF-Regelgruppenüberschreiben der Objekterstellung.</span><span class="sxs-lookup"><span data-stu-id="dd79d-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="dd79d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd79d-107">EXAMPLES</span></span>

### <span data-ttu-id="dd79d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd79d-108">Example 1</span></span>
<span data-ttu-id="dd79d-109">Erstellen Sie ein verwaltetes Regelüberschreibungsobjekt für Regel 942250 (das sich in der SQLI-Gruppe befindet).</span><span class="sxs-lookup"><span data-stu-id="dd79d-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="dd79d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd79d-110">PARAMETERS</span></span>

### <span data-ttu-id="dd79d-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="dd79d-111">-Action</span></span>
<span data-ttu-id="dd79d-112">Aktion außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="dd79d-112">Override Action</span></span>

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

### <span data-ttu-id="dd79d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd79d-113">-DefaultProfile</span></span>
<span data-ttu-id="dd79d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd79d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd79d-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="dd79d-115">-Disabled</span></span>
<span data-ttu-id="dd79d-116">Status "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="dd79d-116">Disabled state</span></span>

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

### <span data-ttu-id="dd79d-117">-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="dd79d-117">-Exclusion</span></span>
<span data-ttu-id="dd79d-118">Ausschluss</span><span class="sxs-lookup"><span data-stu-id="dd79d-118">Exclusion</span></span>

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

### <span data-ttu-id="dd79d-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="dd79d-119">-RuleId</span></span>
<span data-ttu-id="dd79d-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="dd79d-120">Rule ID</span></span>

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

### <span data-ttu-id="dd79d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd79d-121">CommonParameters</span></span>
<span data-ttu-id="dd79d-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd79d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd79d-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd79d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd79d-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd79d-124">INPUTS</span></span>

### <span data-ttu-id="dd79d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="dd79d-125">None</span></span>

## <span data-ttu-id="dd79d-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd79d-126">OUTPUTS</span></span>

### <span data-ttu-id="dd79d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="dd79d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="dd79d-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd79d-128">NOTES</span></span>

## <span data-ttu-id="dd79d-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd79d-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd79d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="dd79d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)