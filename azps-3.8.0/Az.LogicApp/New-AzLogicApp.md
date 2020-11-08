---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996098"
---
# <span data-ttu-id="e1ff2-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ff2-101">New-AzLogicApp</span></span>

## <span data-ttu-id="e1ff2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ff2-103">Erstellt eine Logik-app in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="e1ff2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ff2-104">SYNTAX</span></span>

### <span data-ttu-id="e1ff2-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ff2-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ff2-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ff2-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ff2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1ff2-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ff2-108">Mit dem Cmdlet **New-AzLogicApp** wird mithilfe des Features Logik-apps eine Logik-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="e1ff2-109">Eine Logik-APP ist eine Sammlung von Aktionen oder Triggern, die in der Logik-App-Definition definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="e1ff2-110">Dieses Cmdlet gibt ein **Workflow** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="e1ff2-111">Sie können eine Logik-app erstellen, indem Sie einen Namen, einen Speicherort, eine Logik-App-Definition, eine Ressourcengruppe und einen Plan angeben.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="e1ff2-112">Eine Logik-App-Definition und-Parameter werden in JSON (JavaScript Object Notation) formatiert.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="e1ff2-113">Sie können eine Logik-App als Vorlage für Definition und Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="e1ff2-114">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e1ff2-115">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e1ff2-116">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e1ff2-117">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e1ff2-118">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="e1ff2-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ff2-119">EXAMPLES</span></span>

### <span data-ttu-id="e1ff2-120">Beispiel 1: Erstellen einer Logik-App mithilfe von Definitions-und Parameterdatei Pfaden</span><span class="sxs-lookup"><span data-stu-id="e1ff2-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="e1ff2-121">Mit diesem Befehl wird eine Logik-app in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="e1ff2-122">Die Logik-app enthält die Definition und die Parameter, die von Dateipfaden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e1ff2-123">Beispiel 2: Erstellen einer Logik-App mithilfe von Definitions-und Parameterobjekten</span><span class="sxs-lookup"><span data-stu-id="e1ff2-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="e1ff2-124">Mit diesem Befehl wird eine Logik-app in der angegebenen Ressourcengruppen-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="e1ff2-125">Beispiel 3: Erstellen einer Logik-App mithilfe der Pipeline zum Angeben der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e1ff2-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="e1ff2-126">Dieser Befehl ruft die Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e1ff2-127">Der Befehl übergibt diese Ressourcengruppe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e1ff2-128">Das aktuelle Cmdlet erstellt eine Logik-app in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="e1ff2-129">Die Logik-app enthält die Definition und die Parameter, die von Dateipfaden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e1ff2-130">Beispiel 4: Erstellen einer Logik-App basierend auf einer vorhandenen Logik-App</span><span class="sxs-lookup"><span data-stu-id="e1ff2-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="e1ff2-131">Der erste Befehl ruft die Logik-App mit dem Namen LogicApp03 mithilfe des Get-AzLogicApp-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="e1ff2-132">Der Befehl speichert die Logik-app in der $Workflow-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="e1ff2-133">Mit dem zweiten Befehl wird eine neue Logik-App erstellt, die die Definition und die Parameter der in $Workflow gespeicherten Logik-App verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="e1ff2-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ff2-134">PARAMETERS</span></span>

### <span data-ttu-id="e1ff2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ff2-135">-DefaultProfile</span></span>
<span data-ttu-id="e1ff2-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e1ff2-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1ff2-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="e1ff2-137">-Definition</span></span>
<span data-ttu-id="e1ff2-138">Gibt die Definition für Ihre Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="e1ff2-139">-DefinitionFilePath</span></span>
<span data-ttu-id="e1ff2-140">Gibt die Definition einer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="e1ff2-141">-IntegrationAccountId</span></span>
<span data-ttu-id="e1ff2-142">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="e1ff2-143">-Standort</span><span class="sxs-lookup"><span data-stu-id="e1ff2-143">-Location</span></span>
<span data-ttu-id="e1ff2-144">Gibt den Speicherort der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="e1ff2-145">Geben Sie einen Azure Data Center-Standort ein, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="e1ff2-146">Sie können eine Logik-APP an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-146">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-147">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ff2-147">-Name</span></span>
<span data-ttu-id="e1ff2-148">Gibt den Namen für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="e1ff2-149">-ParameterFilePath</span></span>
<span data-ttu-id="e1ff2-150">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="e1ff2-151">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ff2-151">-Parameters</span></span>
<span data-ttu-id="e1ff2-152">Gibt ein Parameter-Auflistungsobjekt für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="e1ff2-153">Geben Sie eine Hashtabelle, eine Wörterbuch \< Zeichenfolge \> oder eine Wörterbuch \< Zeichenfolge, Workflowparameter, an \> .</span><span class="sxs-lookup"><span data-stu-id="e1ff2-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ff2-154">-ResourceGroupName</span></span>
<span data-ttu-id="e1ff2-155">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-155">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-156">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="e1ff2-156">-State</span></span>
<span data-ttu-id="e1ff2-157">Gibt den Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="e1ff2-158">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1ff2-159">-Confirm</span></span>
<span data-ttu-id="e1ff2-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ff2-161">-WhatIf</span></span>
<span data-ttu-id="e1ff2-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ff2-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ff2-164">CommonParameters</span></span>
<span data-ttu-id="e1ff2-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ff2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ff2-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ff2-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ff2-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1ff2-167">INPUTS</span></span>

### <span data-ttu-id="e1ff2-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ff2-168">System.String</span></span>

## <span data-ttu-id="e1ff2-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1ff2-169">OUTPUTS</span></span>

### <span data-ttu-id="e1ff2-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="e1ff2-170">System.Object</span></span>

## <span data-ttu-id="e1ff2-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1ff2-171">NOTES</span></span>

## <span data-ttu-id="e1ff2-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1ff2-172">RELATED LINKS</span></span>

[<span data-ttu-id="e1ff2-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ff2-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="e1ff2-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ff2-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="e1ff2-175">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ff2-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="e1ff2-176">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e1ff2-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


