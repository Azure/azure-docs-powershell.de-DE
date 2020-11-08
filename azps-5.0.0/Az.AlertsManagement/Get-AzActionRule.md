---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177149"
---
# <span data-ttu-id="802ad-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="802ad-101">Get-AzActionRule</span></span>

## <span data-ttu-id="802ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="802ad-102">SYNOPSIS</span></span>
<span data-ttu-id="802ad-103">Abrufen von Informationen zu Aktionsregeln</span><span class="sxs-lookup"><span data-stu-id="802ad-103">Get Action Rules Information</span></span>

## <span data-ttu-id="802ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="802ad-104">SYNTAX</span></span>

### <span data-ttu-id="802ad-105">ListActionRules (Standard)</span><span class="sxs-lookup"><span data-stu-id="802ad-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="802ad-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="802ad-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="802ad-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="802ad-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="802ad-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="802ad-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="802ad-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="802ad-109">DESCRIPTION</span></span>
<span data-ttu-id="802ad-110">Das Cmdlet " **Get-AzActionRule** " ruft Aktionsregeln konfiguriert ab.</span><span class="sxs-lookup"><span data-stu-id="802ad-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="802ad-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="802ad-111">EXAMPLES</span></span>

### <span data-ttu-id="802ad-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="802ad-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="802ad-113">Listen Sie alle Aktionsregeln auf, die in der Ressourcengruppen Test-RG-Filterung nach Sev2 Severity und Platform Monitor Service konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="802ad-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="802ad-114">Verwenden Sie Format-List, um die Details jeder Aktionsregel in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="802ad-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="802ad-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="802ad-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="802ad-116">Rufen Sie die Aktionsregel mit dem Namen Test-Aktion-Regel in Test-RG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="802ad-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="802ad-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="802ad-117">PARAMETERS</span></span>

### <span data-ttu-id="802ad-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="802ad-118">-ActionGroup</span></span>
<span data-ttu-id="802ad-119">Gruppe ' Aktion '</span><span class="sxs-lookup"><span data-stu-id="802ad-119">Action group</span></span>

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

### <span data-ttu-id="802ad-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="802ad-120">-AlertRuleId</span></span>
<span data-ttu-id="802ad-121">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="802ad-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="802ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802ad-122">-DefaultProfile</span></span>
<span data-ttu-id="802ad-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="802ad-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802ad-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="802ad-124">-Description</span></span>
<span data-ttu-id="802ad-125">Filtern aller Warnungen mit der intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="802ad-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="802ad-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="802ad-126">-ImpactedScope</span></span>
<span data-ttu-id="802ad-127">Filtern nach betroffenem Bereich</span><span class="sxs-lookup"><span data-stu-id="802ad-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="802ad-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="802ad-128">-MonitorService</span></span>
<span data-ttu-id="802ad-129">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="802ad-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="802ad-130">-Name</span><span class="sxs-lookup"><span data-stu-id="802ad-130">-Name</span></span>
<span data-ttu-id="802ad-131">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="802ad-131">Name of action rule.</span></span>

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

### <span data-ttu-id="802ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="802ad-133">Ressourcengruppen Name, in dem sich die Aktionsregel befindet.</span><span class="sxs-lookup"><span data-stu-id="802ad-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="802ad-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="802ad-134">-ResourceId</span></span>
<span data-ttu-id="802ad-135">Abrufen einer Aktionsregel nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="802ad-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="802ad-136">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="802ad-136">-Severity</span></span>
<span data-ttu-id="802ad-137">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="802ad-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="802ad-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="802ad-138">-TargetResourceGroup</span></span>
<span data-ttu-id="802ad-139">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="802ad-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="802ad-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="802ad-140">-TargetResourceId</span></span>
<span data-ttu-id="802ad-141">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="802ad-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="802ad-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="802ad-142">-TargetResourceType</span></span>
<span data-ttu-id="802ad-143">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="802ad-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="802ad-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802ad-144">CommonParameters</span></span>
<span data-ttu-id="802ad-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802ad-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802ad-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="802ad-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802ad-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="802ad-147">INPUTS</span></span>

### <span data-ttu-id="802ad-148">Keine</span><span class="sxs-lookup"><span data-stu-id="802ad-148">None</span></span>

## <span data-ttu-id="802ad-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="802ad-149">OUTPUTS</span></span>

### <span data-ttu-id="802ad-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="802ad-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="802ad-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="802ad-151">NOTES</span></span>

## <span data-ttu-id="802ad-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="802ad-152">RELATED LINKS</span></span>
