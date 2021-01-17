---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360463"
---
# <span data-ttu-id="967b5-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="967b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="967b5-102">SYNOPSIS</span></span>
<span data-ttu-id="967b5-103">Überprüft eine Definition einer Logik-App.</span><span class="sxs-lookup"><span data-stu-id="967b5-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="967b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="967b5-104">SYNTAX</span></span>

### <span data-ttu-id="967b5-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="967b5-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="967b5-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="967b5-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="967b5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="967b5-107">DESCRIPTION</span></span>
<span data-ttu-id="967b5-108">Das **Cmdlet "Test-AzLogicApp"** überprüft eine Logik-App-Definition in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="967b5-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="967b5-109">Geben Sie den Namen der Logik-App, den Namen der Ressourcengruppe, den Standort, den Zustand, die Id des Integrationskontos oder Parameter an.</span><span class="sxs-lookup"><span data-stu-id="967b5-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="967b5-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="967b5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="967b5-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="967b5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="967b5-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="967b5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="967b5-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="967b5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="967b5-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="967b5-114">EXAMPLES</span></span>

### <span data-ttu-id="967b5-115">Beispiel 1: Überprüfen einer Logik-App mithilfe von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="967b5-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="967b5-116">Mit diesem Befehl wird eine Logik-App mit dem Namen "LogicApp01" in der angegebenen Ressourcengruppe überprüft.</span><span class="sxs-lookup"><span data-stu-id="967b5-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="967b5-117">Der Befehl gibt Pfade für Definitions- und Parameterdateien an.</span><span class="sxs-lookup"><span data-stu-id="967b5-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="967b5-118">Beispiel 2: Überprüfen einer Logik-App mithilfe von Objekten</span><span class="sxs-lookup"><span data-stu-id="967b5-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="967b5-119">Mit diesem Befehl wird eine Logik-App mit dem Namen "LogicApp01" in der angegebenen Ressourcengruppe überprüft.</span><span class="sxs-lookup"><span data-stu-id="967b5-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="967b5-120">Der Befehl gibt Definitions- und Parameterobjekte an.</span><span class="sxs-lookup"><span data-stu-id="967b5-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="967b5-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="967b5-121">Example 3</span></span>

<span data-ttu-id="967b5-122">Überprüft eine Definition einer Logik-App.</span><span class="sxs-lookup"><span data-stu-id="967b5-122">Validates a logic app definition.</span></span> <span data-ttu-id="967b5-123">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="967b5-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="967b5-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="967b5-124">PARAMETERS</span></span>

### <span data-ttu-id="967b5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967b5-125">-DefaultProfile</span></span>
<span data-ttu-id="967b5-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="967b5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="967b5-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="967b5-127">-Definition</span></span>
<span data-ttu-id="967b5-128">Gibt die Definition einer Logik-App als Objekt oder Zeichenfolge im JavaScript Object Notation (JSON)-Format an.</span><span class="sxs-lookup"><span data-stu-id="967b5-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="967b5-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="967b5-129">-DefinitionFilePath</span></span>
<span data-ttu-id="967b5-130">Gibt die Definition Ihrer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="967b5-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="967b5-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="967b5-131">-IntegrationAccountId</span></span>
<span data-ttu-id="967b5-132">Gibt eine Integrationskonto-ID für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="967b5-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="967b5-133">-Location</span><span class="sxs-lookup"><span data-stu-id="967b5-133">-Location</span></span>
<span data-ttu-id="967b5-134">Gibt die Position der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="967b5-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="967b5-135">Geben Sie einen Standort im Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="967b5-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="967b5-136">Sie können eine Logik-App an einer beliebigen Stelle platzieren.</span><span class="sxs-lookup"><span data-stu-id="967b5-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="967b5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="967b5-137">-Name</span></span>
<span data-ttu-id="967b5-138">Gibt den Namen der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="967b5-138">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="967b5-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="967b5-139">-ParameterFilePath</span></span>
<span data-ttu-id="967b5-140">Gibt den Pfad einer im JSON-Format formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="967b5-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="967b5-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="967b5-141">-Parameters</span></span>
<span data-ttu-id="967b5-142">Gibt ein Parametersammlungsobjekt der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="967b5-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="967b5-143">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="967b5-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="967b5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="967b5-144">-ResourceGroupName</span></span>
<span data-ttu-id="967b5-145">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="967b5-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="967b5-146">-State</span><span class="sxs-lookup"><span data-stu-id="967b5-146">-State</span></span>
<span data-ttu-id="967b5-147">Gibt einen Zustand der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="967b5-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="967b5-148">Die zulässigen Werte für diesen Parameter sind: "Enabled" und "Disabled".</span><span class="sxs-lookup"><span data-stu-id="967b5-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="967b5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967b5-149">CommonParameters</span></span>
<span data-ttu-id="967b5-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967b5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967b5-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967b5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967b5-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="967b5-152">INPUTS</span></span>

### <span data-ttu-id="967b5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="967b5-153">System.String</span></span>

## <span data-ttu-id="967b5-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="967b5-154">OUTPUTS</span></span>

### <span data-ttu-id="967b5-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="967b5-155">System.Void</span></span>

## <span data-ttu-id="967b5-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="967b5-156">NOTES</span></span>

## <span data-ttu-id="967b5-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="967b5-157">RELATED LINKS</span></span>

[<span data-ttu-id="967b5-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="967b5-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="967b5-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="967b5-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="967b5-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="967b5-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


