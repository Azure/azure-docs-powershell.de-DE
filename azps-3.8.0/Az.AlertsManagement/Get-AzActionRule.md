---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: e1eb623fcb4b77dda95fe3f849c86e20ad5d1601
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995910"
---
# <span data-ttu-id="22d09-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="22d09-101">Get-AzActionRule</span></span>

## <span data-ttu-id="22d09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22d09-102">SYNOPSIS</span></span>
<span data-ttu-id="22d09-103">Abrufen von Informationen zu Aktionsregeln</span><span class="sxs-lookup"><span data-stu-id="22d09-103">Get Action Rules Information</span></span>

## <span data-ttu-id="22d09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d09-104">SYNTAX</span></span>

### <span data-ttu-id="22d09-105">ListActionRules (Standard)</span><span class="sxs-lookup"><span data-stu-id="22d09-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d09-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22d09-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d09-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="22d09-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22d09-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22d09-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d09-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22d09-109">DESCRIPTION</span></span>
<span data-ttu-id="22d09-110">Das Cmdlet " **Get-AzActionRule** " ruft Aktionsregeln konfiguriert ab.</span><span class="sxs-lookup"><span data-stu-id="22d09-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="22d09-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22d09-111">EXAMPLES</span></span>

### <span data-ttu-id="22d09-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22d09-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="22d09-113">Listen Sie alle Aktionsregeln auf, die in der Ressourcengruppen Test-RG-Filterung nach Sev2 Severity und Platform Monitor Service konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="22d09-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="22d09-114">Verwenden Sie Format-List, um die Details jeder Aktionsregel in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="22d09-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="22d09-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="22d09-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="22d09-116">Rufen Sie die Aktionsregel mit dem Namen Test-Aktion-Regel in Test-RG-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="22d09-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="22d09-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="22d09-117">PARAMETERS</span></span>

### <span data-ttu-id="22d09-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="22d09-118">-ActionGroup</span></span>
<span data-ttu-id="22d09-119">Gruppe ' Aktion '</span><span class="sxs-lookup"><span data-stu-id="22d09-119">Action group</span></span>

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

### <span data-ttu-id="22d09-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="22d09-120">-AlertRuleId</span></span>
<span data-ttu-id="22d09-121">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="22d09-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="22d09-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d09-122">-DefaultProfile</span></span>
<span data-ttu-id="22d09-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22d09-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d09-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22d09-124">-Description</span></span>
<span data-ttu-id="22d09-125">Filtern aller Warnungen mit der intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="22d09-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="22d09-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="22d09-126">-ImpactedScope</span></span>
<span data-ttu-id="22d09-127">Filtern nach betroffenem Bereich</span><span class="sxs-lookup"><span data-stu-id="22d09-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="22d09-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="22d09-128">-MonitorService</span></span>
<span data-ttu-id="22d09-129">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="22d09-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="22d09-130">-Name</span><span class="sxs-lookup"><span data-stu-id="22d09-130">-Name</span></span>
<span data-ttu-id="22d09-131">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="22d09-131">Name of action rule.</span></span>

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

### <span data-ttu-id="22d09-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d09-132">-ResourceGroupName</span></span>
<span data-ttu-id="22d09-133">Ressourcengruppen Name, in dem sich die Aktionsregel befindet.</span><span class="sxs-lookup"><span data-stu-id="22d09-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="22d09-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="22d09-134">-ResourceId</span></span>
<span data-ttu-id="22d09-135">Abrufen einer Aktionsregel nach der Resoure-ID</span><span class="sxs-lookup"><span data-stu-id="22d09-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="22d09-136">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="22d09-136">-Severity</span></span>
<span data-ttu-id="22d09-137">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="22d09-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="22d09-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22d09-138">-TargetResourceGroup</span></span>
<span data-ttu-id="22d09-139">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="22d09-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="22d09-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22d09-140">-TargetResourceId</span></span>
<span data-ttu-id="22d09-141">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="22d09-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="22d09-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="22d09-142">-TargetResourceType</span></span>
<span data-ttu-id="22d09-143">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="22d09-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="22d09-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d09-144">CommonParameters</span></span>
<span data-ttu-id="22d09-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d09-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d09-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22d09-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d09-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22d09-147">INPUTS</span></span>

### <span data-ttu-id="22d09-148">Keine</span><span class="sxs-lookup"><span data-stu-id="22d09-148">None</span></span>

## <span data-ttu-id="22d09-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22d09-149">OUTPUTS</span></span>

### <span data-ttu-id="22d09-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="22d09-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="22d09-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="22d09-151">NOTES</span></span>

## <span data-ttu-id="22d09-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22d09-152">RELATED LINKS</span></span>
