---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505914"
---
# <span data-ttu-id="85462-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="85462-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="85462-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85462-102">SYNOPSIS</span></span>
<span data-ttu-id="85462-103">Ändert eine Logik-app in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85462-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85462-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85462-104">SYNTAX</span></span>

### <span data-ttu-id="85462-105">Verbrauch (Standard)</span><span class="sxs-lookup"><span data-stu-id="85462-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85462-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="85462-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85462-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85462-107">DESCRIPTION</span></span>
<span data-ttu-id="85462-108">Das Cmdlet " **Satz-AzureRmLogicApp** " ändert eine Logik-App mithilfe des Features "Logik-Apps".</span><span class="sxs-lookup"><span data-stu-id="85462-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="85462-109">Eine Logik-APP ist eine Sammlung von Aktionen oder Triggern, die in der Logik-App-Definition definiert sind.</span><span class="sxs-lookup"><span data-stu-id="85462-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="85462-110">Dieses Cmdlet gibt ein **Workflow** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="85462-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="85462-111">Sie können eine Logik-App ändern, indem Sie einen Namen, einen Speicherort, eine Logik-App-Definition, eine Ressourcengruppe und einen Plan angeben.</span><span class="sxs-lookup"><span data-stu-id="85462-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="85462-112">Eine Logik-App-Definition und-Parameter werden in JSON (JavaScript Object Notation) formatiert.</span><span class="sxs-lookup"><span data-stu-id="85462-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="85462-113">Sie können eine Logik-App als Vorlage für Definition und Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="85462-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="85462-114">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="85462-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="85462-115">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="85462-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="85462-116">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="85462-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="85462-117">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="85462-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="85462-118">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="85462-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="85462-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85462-119">EXAMPLES</span></span>

### <span data-ttu-id="85462-120">Beispiel 1: Ändern einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="85462-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="85462-121">Dieser Befehl ändert eine Logik-app.</span><span class="sxs-lookup"><span data-stu-id="85462-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="85462-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="85462-122">PARAMETERS</span></span>

### <span data-ttu-id="85462-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85462-123">-AppServicePlan</span></span>
<span data-ttu-id="85462-124">Gibt den Namen eines Plans an.</span><span class="sxs-lookup"><span data-stu-id="85462-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="85462-125">-Definition</span><span class="sxs-lookup"><span data-stu-id="85462-125">-Definition</span></span>
<span data-ttu-id="85462-126">Gibt die Definition einer Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="85462-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="85462-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="85462-127">-DefinitionFilePath</span></span>
<span data-ttu-id="85462-128">Gibt die Definition einer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="85462-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="85462-129">-Force</span><span class="sxs-lookup"><span data-stu-id="85462-129">-Force</span></span>
<span data-ttu-id="85462-130">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="85462-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85462-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="85462-131">-IntegrationAccountId</span></span>
<span data-ttu-id="85462-132">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="85462-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="85462-133">-Name</span><span class="sxs-lookup"><span data-stu-id="85462-133">-Name</span></span>
<span data-ttu-id="85462-134">Gibt den Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="85462-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="85462-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="85462-135">-ParameterFilePath</span></span>
<span data-ttu-id="85462-136">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="85462-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="85462-137">-Parameter</span><span class="sxs-lookup"><span data-stu-id="85462-137">-Parameters</span></span>
<span data-ttu-id="85462-138">Gibt ein Parameter-Auflistungsobjekt für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="85462-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="85462-139">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="85462-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="85462-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85462-140">-ResourceGroupName</span></span>
<span data-ttu-id="85462-141">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="85462-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85462-142">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="85462-142">-State</span></span>
<span data-ttu-id="85462-143">Gibt den Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="85462-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="85462-144">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="85462-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="85462-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="85462-145">-UseConsumptionModel</span></span>
<span data-ttu-id="85462-146">Gibt an, dass die Logik-App-Abrechnung das verbrauchsbasierte Modell verwendet.</span><span class="sxs-lookup"><span data-stu-id="85462-146">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="85462-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85462-147">-Confirm</span></span>
<span data-ttu-id="85462-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85462-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85462-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85462-149">-WhatIf</span></span>
<span data-ttu-id="85462-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85462-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85462-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85462-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85462-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85462-152">-DefaultProfile</span></span>
<span data-ttu-id="85462-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85462-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85462-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85462-154">CommonParameters</span></span>
<span data-ttu-id="85462-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85462-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85462-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85462-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85462-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85462-157">INPUTS</span></span>

## <span data-ttu-id="85462-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85462-158">OUTPUTS</span></span>

### <span data-ttu-id="85462-159">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="85462-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="85462-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="85462-160">NOTES</span></span>

## <span data-ttu-id="85462-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85462-161">RELATED LINKS</span></span>

[<span data-ttu-id="85462-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="85462-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="85462-163">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="85462-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="85462-164">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="85462-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="85462-165">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="85462-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


