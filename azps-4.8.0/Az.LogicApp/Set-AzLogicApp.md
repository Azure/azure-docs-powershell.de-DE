---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009767"
---
# <span data-ttu-id="de760-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="de760-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="de760-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de760-102">SYNOPSIS</span></span>
<span data-ttu-id="de760-103">Ändert eine Logik-app in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="de760-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="de760-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de760-104">SYNTAX</span></span>

### <span data-ttu-id="de760-105">Verbrauch (Standard)</span><span class="sxs-lookup"><span data-stu-id="de760-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de760-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="de760-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de760-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de760-107">DESCRIPTION</span></span>
<span data-ttu-id="de760-108">Das Cmdlet " **Satz-AzLogicApp** " ändert eine Logik-App mithilfe des Features "Logik-Apps".</span><span class="sxs-lookup"><span data-stu-id="de760-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="de760-109">Eine Logik-APP ist eine Sammlung von Aktionen oder Triggern, die in der Logik-App-Definition definiert sind.</span><span class="sxs-lookup"><span data-stu-id="de760-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="de760-110">Dieses Cmdlet gibt ein **Workflow** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="de760-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="de760-111">Sie können eine Logik-App ändern, indem Sie einen Namen, einen Speicherort, eine Logik-App-Definition, eine Ressourcengruppe und einen Plan angeben.</span><span class="sxs-lookup"><span data-stu-id="de760-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="de760-112">Eine Logik-App-Definition und-Parameter werden in JSON (JavaScript Object Notation) formatiert.</span><span class="sxs-lookup"><span data-stu-id="de760-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="de760-113">Sie können eine Logik-App als Vorlage für Definition und Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="de760-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="de760-114">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="de760-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="de760-115">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="de760-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="de760-116">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="de760-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="de760-117">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="de760-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="de760-118">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="de760-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="de760-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de760-119">EXAMPLES</span></span>

### <span data-ttu-id="de760-120">Beispiel 1: Ändern einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="de760-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="de760-121">Dieser Befehl ändert eine Logik-app.</span><span class="sxs-lookup"><span data-stu-id="de760-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="de760-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="de760-122">PARAMETERS</span></span>

### <span data-ttu-id="de760-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de760-123">-AppServicePlan</span></span>
<span data-ttu-id="de760-124">Gibt den Namen eines Plans an.</span><span class="sxs-lookup"><span data-stu-id="de760-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="de760-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de760-125">-DefaultProfile</span></span>
<span data-ttu-id="de760-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="de760-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de760-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="de760-127">-Definition</span></span>
<span data-ttu-id="de760-128">Gibt die Definition einer Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="de760-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="de760-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="de760-129">-DefinitionFilePath</span></span>
<span data-ttu-id="de760-130">Gibt die Definition einer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="de760-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="de760-131">-Force</span><span class="sxs-lookup"><span data-stu-id="de760-131">-Force</span></span>
<span data-ttu-id="de760-132">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="de760-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de760-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="de760-133">-IntegrationAccountId</span></span>
<span data-ttu-id="de760-134">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="de760-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="de760-135">-Name</span><span class="sxs-lookup"><span data-stu-id="de760-135">-Name</span></span>
<span data-ttu-id="de760-136">Gibt den Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="de760-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="de760-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="de760-137">-ParameterFilePath</span></span>
<span data-ttu-id="de760-138">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="de760-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="de760-139">-Parameter</span><span class="sxs-lookup"><span data-stu-id="de760-139">-Parameters</span></span>
<span data-ttu-id="de760-140">Gibt ein Parameter-Auflistungsobjekt für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="de760-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="de760-141">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="de760-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="de760-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de760-142">-ResourceGroupName</span></span>
<span data-ttu-id="de760-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="de760-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="de760-144">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="de760-144">-State</span></span>
<span data-ttu-id="de760-145">Gibt den Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="de760-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="de760-146">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="de760-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="de760-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="de760-147">-UseConsumptionModel</span></span>
<span data-ttu-id="de760-148">Gibt an, dass die Logik-App-Abrechnung das verbrauchsbasierte Modell verwendet.</span><span class="sxs-lookup"><span data-stu-id="de760-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="de760-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de760-149">-Confirm</span></span>
<span data-ttu-id="de760-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de760-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de760-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de760-151">-WhatIf</span></span>
<span data-ttu-id="de760-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de760-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de760-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de760-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de760-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de760-154">CommonParameters</span></span>
<span data-ttu-id="de760-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de760-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de760-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de760-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de760-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de760-157">INPUTS</span></span>

### <span data-ttu-id="de760-158">System. String</span><span class="sxs-lookup"><span data-stu-id="de760-158">System.String</span></span>

## <span data-ttu-id="de760-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de760-159">OUTPUTS</span></span>

### <span data-ttu-id="de760-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="de760-160">System.Object</span></span>

## <span data-ttu-id="de760-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="de760-161">NOTES</span></span>

## <span data-ttu-id="de760-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de760-162">RELATED LINKS</span></span>

[<span data-ttu-id="de760-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="de760-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="de760-164">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="de760-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="de760-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="de760-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="de760-166">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="de760-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


