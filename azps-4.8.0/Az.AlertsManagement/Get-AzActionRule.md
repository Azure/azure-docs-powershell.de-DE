---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009494"
---
# <span data-ttu-id="585d9-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="585d9-101">Get-AzActionRule</span></span>

## <span data-ttu-id="585d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="585d9-102">SYNOPSIS</span></span>
<span data-ttu-id="585d9-103">Abrufen von Informationen zu Aktionsregeln</span><span class="sxs-lookup"><span data-stu-id="585d9-103">Get Action Rules Information</span></span>

## <span data-ttu-id="585d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="585d9-104">SYNTAX</span></span>

### <span data-ttu-id="585d9-105">ListActionRules (Standard)</span><span class="sxs-lookup"><span data-stu-id="585d9-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="585d9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="585d9-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="585d9-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="585d9-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="585d9-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="585d9-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="585d9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="585d9-109">DESCRIPTION</span></span>
<span data-ttu-id="585d9-110">Das Cmdlet " **Get-AzActionRule** " ruft Aktionsregeln konfiguriert ab.</span><span class="sxs-lookup"><span data-stu-id="585d9-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="585d9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="585d9-111">EXAMPLES</span></span>

### <span data-ttu-id="585d9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="585d9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="585d9-113">Listen Sie alle Aktionsregeln auf, die in der Ressourcengruppen Test-RG-Filterung nach Sev2 Severity und Platform Monitor Service konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="585d9-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="585d9-114">Verwenden Sie Format-List, um die Details jeder Aktionsregel in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="585d9-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="585d9-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="585d9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="585d9-116">Rufen Sie die Aktionsregel mit dem Namen Test-Aktion-Regel in Test-RG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="585d9-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="585d9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="585d9-117">PARAMETERS</span></span>

### <span data-ttu-id="585d9-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="585d9-118">-ActionGroup</span></span>
<span data-ttu-id="585d9-119">Gruppe ' Aktion '</span><span class="sxs-lookup"><span data-stu-id="585d9-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="585d9-120">-AlertRuleId</span></span>
<span data-ttu-id="585d9-121">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="585d9-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585d9-122">-DefaultProfile</span></span>
<span data-ttu-id="585d9-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="585d9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585d9-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="585d9-124">-Description</span></span>
<span data-ttu-id="585d9-125">Filtern aller Warnungen mit der intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="585d9-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="585d9-126">-ImpactedScope</span></span>
<span data-ttu-id="585d9-127">Filtern nach betroffenem Bereich</span><span class="sxs-lookup"><span data-stu-id="585d9-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="585d9-128">-MonitorService</span></span>
<span data-ttu-id="585d9-129">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="585d9-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="585d9-130">-Name</span></span>
<span data-ttu-id="585d9-131">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="585d9-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585d9-132">-ResourceGroupName</span></span>
<span data-ttu-id="585d9-133">Ressourcengruppen Name, in dem sich die Aktionsregel befindet.</span><span class="sxs-lookup"><span data-stu-id="585d9-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="585d9-134">-ResourceId</span></span>
<span data-ttu-id="585d9-135">Abrufen einer Aktionsregel nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="585d9-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-136">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="585d9-136">-Severity</span></span>
<span data-ttu-id="585d9-137">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="585d9-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="585d9-138">-TargetResourceGroup</span></span>
<span data-ttu-id="585d9-139">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="585d9-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="585d9-140">-TargetResourceId</span></span>
<span data-ttu-id="585d9-141">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="585d9-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="585d9-142">-TargetResourceType</span></span>
<span data-ttu-id="585d9-143">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="585d9-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585d9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585d9-144">CommonParameters</span></span>
<span data-ttu-id="585d9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585d9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585d9-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="585d9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585d9-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="585d9-147">INPUTS</span></span>

### <span data-ttu-id="585d9-148">Keine</span><span class="sxs-lookup"><span data-stu-id="585d9-148">None</span></span>

## <span data-ttu-id="585d9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="585d9-149">OUTPUTS</span></span>

### <span data-ttu-id="585d9-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="585d9-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="585d9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="585d9-151">NOTES</span></span>

## <span data-ttu-id="585d9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="585d9-152">RELATED LINKS</span></span>
