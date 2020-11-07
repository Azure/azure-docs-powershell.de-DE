---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 689588e8b92b4b76c97f3972aa63c2f8cdc16535
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841919"
---
# <span data-ttu-id="5bc95-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5bc95-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="5bc95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bc95-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc95-103">Entfernt eine Protokoll Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="5bc95-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="5bc95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bc95-104">SYNTAX</span></span>

### <span data-ttu-id="5bc95-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bc95-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc95-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5bc95-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc95-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5bc95-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc95-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bc95-108">DESCRIPTION</span></span>
<span data-ttu-id="5bc95-109">Entfernt eine Protokoll Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="5bc95-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="5bc95-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bc95-110">EXAMPLES</span></span>

### <span data-ttu-id="5bc95-111">Beispiel 1: Entfernen nach Regelnamen</span><span class="sxs-lookup"><span data-stu-id="5bc95-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="5bc95-112">Beispiel 2 – entfernen nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5bc95-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="5bc95-113">Beispiel 3 – Entfernen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5bc95-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="5bc95-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bc95-114">PARAMETERS</span></span>

### <span data-ttu-id="5bc95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc95-115">-DefaultProfile</span></span>
<span data-ttu-id="5bc95-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5bc95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc95-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5bc95-117">-InputObject</span></span>
<span data-ttu-id="5bc95-118">Die geplante Abfrageregel Ressource</span><span class="sxs-lookup"><span data-stu-id="5bc95-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5bc95-119">-Name</span></span>
<span data-ttu-id="5bc95-120">Der Warnungsname</span><span class="sxs-lookup"><span data-stu-id="5bc95-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bc95-121">-PassThru</span></span>
<span data-ttu-id="5bc95-122">Gibt einen Wert zurück, der angibt, ob Erfolg oder Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5bc95-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="5bc95-123">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5bc95-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5bc95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc95-124">-ResourceGroupName</span></span>
<span data-ttu-id="5bc95-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5bc95-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5bc95-126">-ResourceId</span></span>
<span data-ttu-id="5bc95-127">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5bc95-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bc95-128">-Confirm</span></span>
<span data-ttu-id="5bc95-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bc95-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc95-130">-WhatIf</span></span>
<span data-ttu-id="5bc95-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bc95-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc95-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bc95-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc95-133">CommonParameters</span></span>
<span data-ttu-id="5bc95-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc95-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bc95-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc95-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bc95-136">INPUTS</span></span>

### <span data-ttu-id="5bc95-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="5bc95-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="5bc95-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5bc95-138">System.String</span></span>

## <span data-ttu-id="5bc95-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bc95-139">OUTPUTS</span></span>

### <span data-ttu-id="5bc95-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bc95-140">System.Boolean</span></span>

## <span data-ttu-id="5bc95-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bc95-141">NOTES</span></span>

## <span data-ttu-id="5bc95-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bc95-142">RELATED LINKS</span></span>
