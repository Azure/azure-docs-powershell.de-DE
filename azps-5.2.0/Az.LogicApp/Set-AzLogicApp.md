---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368359"
---
# <span data-ttu-id="4f480-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f480-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="4f480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f480-102">SYNOPSIS</span></span>
<span data-ttu-id="4f480-103">Ändert eine Logik-App in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f480-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="4f480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f480-104">SYNTAX</span></span>

### <span data-ttu-id="4f480-105">Verbrauch (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f480-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f480-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="4f480-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f480-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f480-107">DESCRIPTION</span></span>
<span data-ttu-id="4f480-108">Das **Cmdlet "Set-AzLogicApp"** ändert eine Logik-App mithilfe des Features "Logik-Apps".</span><span class="sxs-lookup"><span data-stu-id="4f480-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="4f480-109">Eine Logik-App ist eine Sammlung von Aktionen oder Triggern, die in der Definition von Logic App definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4f480-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="4f480-110">Dieses Cmdlet gibt ein **Workflowobjekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="4f480-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="4f480-111">Sie können eine Logik-App ändern, indem Sie einen Namen, einen Ort, eine Definition der Logik-App, eine Ressourcengruppe und einen Plan angeben.</span><span class="sxs-lookup"><span data-stu-id="4f480-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="4f480-112">Eine Definition und Parameter einer Logik-App werden in JavaScript Object Notation (JSON) formatiert.</span><span class="sxs-lookup"><span data-stu-id="4f480-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="4f480-113">Sie können eine Logik-App als Vorlage für Definitionen und Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f480-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="4f480-114">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f480-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f480-115">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4f480-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f480-116">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4f480-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f480-117">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4f480-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="4f480-118">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="4f480-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="4f480-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f480-119">EXAMPLES</span></span>

### <span data-ttu-id="4f480-120">Beispiel 1: Ändern einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="4f480-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="4f480-121">Mit diesem Befehl wird eine Logik-App geändert.</span><span class="sxs-lookup"><span data-stu-id="4f480-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="4f480-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f480-122">PARAMETERS</span></span>

### <span data-ttu-id="4f480-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4f480-123">-AppServicePlan</span></span>
<span data-ttu-id="4f480-124">Gibt den Namen eines Plans an.</span><span class="sxs-lookup"><span data-stu-id="4f480-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f480-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f480-125">-DefaultProfile</span></span>
<span data-ttu-id="4f480-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f480-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f480-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="4f480-127">-Definition</span></span>
<span data-ttu-id="4f480-128">Gibt die Definition einer Logik-App als Objekt oder Zeichenfolge im JavaScript Object Notation (JSON)-Format an.</span><span class="sxs-lookup"><span data-stu-id="4f480-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="4f480-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="4f480-129">-DefinitionFilePath</span></span>
<span data-ttu-id="4f480-130">Gibt die Definition einer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="4f480-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="4f480-131">-Force</span><span class="sxs-lookup"><span data-stu-id="4f480-131">-Force</span></span>
<span data-ttu-id="4f480-132">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4f480-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f480-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="4f480-133">-IntegrationAccountId</span></span>
<span data-ttu-id="4f480-134">Gibt eine Integrationskonto-ID für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4f480-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="4f480-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4f480-135">-Name</span></span>
<span data-ttu-id="4f480-136">Gibt den Namen einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4f480-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="4f480-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="4f480-137">-ParameterFilePath</span></span>
<span data-ttu-id="4f480-138">Gibt den Pfad einer im JSON-Format formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="4f480-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="4f480-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4f480-139">-Parameters</span></span>
<span data-ttu-id="4f480-140">Gibt ein Parametersammlungsobjekt für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4f480-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="4f480-141">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="4f480-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="4f480-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f480-142">-ResourceGroupName</span></span>
<span data-ttu-id="4f480-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4f480-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f480-144">-State</span><span class="sxs-lookup"><span data-stu-id="4f480-144">-State</span></span>
<span data-ttu-id="4f480-145">Gibt den Zustand der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4f480-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="4f480-146">Die zulässigen Werte für diesen Parameter sind: "Enabled" und "Disabled".</span><span class="sxs-lookup"><span data-stu-id="4f480-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="4f480-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="4f480-147">-UseConsumptionModel</span></span>
<span data-ttu-id="4f480-148">Gibt an, dass für die Abrechnung der Logik der App das verbrauchsbasierte Modell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f480-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f480-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f480-149">-Confirm</span></span>
<span data-ttu-id="4f480-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f480-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f480-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f480-151">-WhatIf</span></span>
<span data-ttu-id="4f480-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f480-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f480-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f480-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f480-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f480-154">CommonParameters</span></span>
<span data-ttu-id="4f480-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f480-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f480-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f480-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f480-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f480-157">INPUTS</span></span>

### <span data-ttu-id="4f480-158">System.String</span><span class="sxs-lookup"><span data-stu-id="4f480-158">System.String</span></span>

## <span data-ttu-id="4f480-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f480-159">OUTPUTS</span></span>

### <span data-ttu-id="4f480-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f480-160">System.Object</span></span>

## <span data-ttu-id="4f480-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f480-161">NOTES</span></span>

## <span data-ttu-id="4f480-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f480-162">RELATED LINKS</span></span>

[<span data-ttu-id="4f480-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f480-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="4f480-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f480-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="4f480-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f480-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="4f480-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f480-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


