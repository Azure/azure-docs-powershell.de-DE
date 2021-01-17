---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459107"
---
# <span data-ttu-id="4a729-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a729-101">New-AzLogicApp</span></span>

## <span data-ttu-id="4a729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a729-102">SYNOPSIS</span></span>
<span data-ttu-id="4a729-103">Erstellt eine Logik-App in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a729-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="4a729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a729-104">SYNTAX</span></span>

### <span data-ttu-id="4a729-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a729-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a729-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a729-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a729-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a729-107">DESCRIPTION</span></span>
<span data-ttu-id="4a729-108">Das **Cmdlet "New-AzLogicApp"** erstellt mithilfe des Features "Logik-Apps" eine Logik-App.</span><span class="sxs-lookup"><span data-stu-id="4a729-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="4a729-109">Eine Logik-App ist eine Sammlung von Aktionen oder Triggern, die in der Definition von Logic App definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4a729-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="4a729-110">Dieses Cmdlet gibt ein **Workflowobjekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="4a729-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="4a729-111">Sie können eine Logik-App erstellen, indem Sie einen Namen, einen Ort, eine Definition der Logik-App, eine Ressourcengruppe und einen Plan angeben.</span><span class="sxs-lookup"><span data-stu-id="4a729-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="4a729-112">Eine Definition und Parameter einer Logik-App werden in JavaScript Object Notation (JSON) formatiert.</span><span class="sxs-lookup"><span data-stu-id="4a729-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="4a729-113">Sie können eine Logik-App als Vorlage für Definitionen und Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a729-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="4a729-114">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4a729-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4a729-115">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4a729-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4a729-116">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4a729-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4a729-117">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4a729-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="4a729-118">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="4a729-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="4a729-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a729-119">EXAMPLES</span></span>

### <span data-ttu-id="4a729-120">Beispiel 1: Erstellen einer Logik-App mithilfe von Dateipfaden für Definitionen und Parameter</span><span class="sxs-lookup"><span data-stu-id="4a729-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
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

<span data-ttu-id="4a729-121">Mit diesem Befehl wird eine Logik-App in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a729-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="4a729-122">Die Logik-App enthält die Definition und parameter, die von Dateipfaden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a729-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4a729-123">Beispiel 2: Erstellen einer Logik-App mithilfe von Definitions- und Parameterobjekten</span><span class="sxs-lookup"><span data-stu-id="4a729-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
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

<span data-ttu-id="4a729-124">Mit diesem Befehl wird eine Logik-App in der angegebenen Ressourcengruppenressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a729-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="4a729-125">Beispiel 3: Erstellen einer Logik-App mithilfe der Pipeline zum Angeben der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4a729-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
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

<span data-ttu-id="4a729-126">Dieser Befehl ruft die Ressourcengruppe "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="4a729-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4a729-127">Der Befehl übergibt diese Ressourcengruppe mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a729-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4a729-128">Das aktuelle Cmdlet erstellt eine Logik-App in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a729-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="4a729-129">Die Logik-App enthält die Definition und parameter, die von Dateipfaden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a729-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="4a729-130">Beispiel 4: Erstellen einer Logik-App, die auf einer vorhandenen Logik-App basiert</span><span class="sxs-lookup"><span data-stu-id="4a729-130">Example 4: Create a logic app based on an existing logic app</span></span>
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

<span data-ttu-id="4a729-131">Der erste Befehl ruft die Logik-App mit dem Namen "LogicApp03" mithilfe des Get-AzLogicApp ab.</span><span class="sxs-lookup"><span data-stu-id="4a729-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="4a729-132">Der Befehl speichert die Logik-App in der $Workflow Variable.</span><span class="sxs-lookup"><span data-stu-id="4a729-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="4a729-133">Der zweite Befehl erstellt eine neue Logik-App, die die Definition und Parameter der in der App gespeicherten Logik-App $Workflow.</span><span class="sxs-lookup"><span data-stu-id="4a729-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="4a729-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a729-134">PARAMETERS</span></span>

### <span data-ttu-id="4a729-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a729-135">-DefaultProfile</span></span>
<span data-ttu-id="4a729-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4a729-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a729-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="4a729-137">-Definition</span></span>
<span data-ttu-id="4a729-138">Gibt die Definition für Ihre Logik-App als Objekt oder Zeichenfolge im JavaScript Object Notation (JSON)-Format an.</span><span class="sxs-lookup"><span data-stu-id="4a729-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="4a729-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="4a729-139">-DefinitionFilePath</span></span>
<span data-ttu-id="4a729-140">Gibt die Definition einer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="4a729-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="4a729-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="4a729-141">-IntegrationAccountId</span></span>
<span data-ttu-id="4a729-142">Gibt eine Integrationskonto-ID für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4a729-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="4a729-143">-Location</span><span class="sxs-lookup"><span data-stu-id="4a729-143">-Location</span></span>
<span data-ttu-id="4a729-144">Gibt die Position der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4a729-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="4a729-145">Geben Sie einen Standort im Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="4a729-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="4a729-146">Sie können eine Logik-App an einer beliebigen Stelle platzieren.</span><span class="sxs-lookup"><span data-stu-id="4a729-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="4a729-147">-Name</span><span class="sxs-lookup"><span data-stu-id="4a729-147">-Name</span></span>
<span data-ttu-id="4a729-148">Gibt den Namen für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4a729-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="4a729-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="4a729-149">-ParameterFilePath</span></span>
<span data-ttu-id="4a729-150">Gibt den Pfad einer im JSON-Format formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="4a729-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="4a729-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4a729-151">-Parameters</span></span>
<span data-ttu-id="4a729-152">Gibt ein Parametersammlungsobjekt für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4a729-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="4a729-153">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="4a729-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="4a729-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a729-154">-ResourceGroupName</span></span>
<span data-ttu-id="4a729-155">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4a729-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4a729-156">-State</span><span class="sxs-lookup"><span data-stu-id="4a729-156">-State</span></span>
<span data-ttu-id="4a729-157">Gibt den Zustand der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4a729-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="4a729-158">Die zulässigen Werte für diesen Parameter sind: "Enabled" und "Disabled".</span><span class="sxs-lookup"><span data-stu-id="4a729-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="4a729-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a729-159">-Confirm</span></span>
<span data-ttu-id="4a729-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a729-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a729-161">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a729-161">-WhatIf</span></span>
<span data-ttu-id="4a729-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a729-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a729-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a729-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a729-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a729-164">CommonParameters</span></span>
<span data-ttu-id="4a729-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a729-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a729-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a729-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a729-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a729-167">INPUTS</span></span>

### <span data-ttu-id="4a729-168">System.String</span><span class="sxs-lookup"><span data-stu-id="4a729-168">System.String</span></span>

## <span data-ttu-id="4a729-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a729-169">OUTPUTS</span></span>

### <span data-ttu-id="4a729-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="4a729-170">System.Object</span></span>

## <span data-ttu-id="4a729-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a729-171">NOTES</span></span>

## <span data-ttu-id="4a729-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a729-172">RELATED LINKS</span></span>

[<span data-ttu-id="4a729-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a729-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="4a729-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a729-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="4a729-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a729-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="4a729-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a729-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


