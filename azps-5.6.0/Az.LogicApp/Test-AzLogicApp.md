---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: 6639a397c97be35565d374279b2981fa2b1eabd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918800"
---
# <span data-ttu-id="f177f-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="f177f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f177f-102">SYNOPSIS</span></span>
<span data-ttu-id="f177f-103">Überprüft eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="f177f-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="f177f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f177f-104">SYNTAX</span></span>

### <span data-ttu-id="f177f-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f177f-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f177f-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f177f-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f177f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f177f-107">DESCRIPTION</span></span>
<span data-ttu-id="f177f-108">Das **Test-AzLogicApp-Cmdlet** überprüft eine Logik-App-Definition in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f177f-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="f177f-109">Geben Sie den Namen der Logik-App, den Ressourcengruppennamen, den Standort, den Zustand, die Integrationskonto-ID oder parameter an.</span><span class="sxs-lookup"><span data-stu-id="f177f-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="f177f-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="f177f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f177f-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="f177f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f177f-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="f177f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f177f-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f177f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f177f-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f177f-114">EXAMPLES</span></span>

### <span data-ttu-id="f177f-115">Beispiel 1: Überprüfen einer Logik-App mithilfe von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="f177f-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="f177f-116">Mit diesem Befehl wird eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe überprüft.</span><span class="sxs-lookup"><span data-stu-id="f177f-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="f177f-117">Der Befehl gibt Definitions- und Parameterdateipfade an.</span><span class="sxs-lookup"><span data-stu-id="f177f-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="f177f-118">Beispiel 2: Überprüfen einer Logik-App mithilfe von -Objekten</span><span class="sxs-lookup"><span data-stu-id="f177f-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="f177f-119">Mit diesem Befehl wird eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe überprüft.</span><span class="sxs-lookup"><span data-stu-id="f177f-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="f177f-120">Der Befehl gibt Definitions- und Parameterobjekte an.</span><span class="sxs-lookup"><span data-stu-id="f177f-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="f177f-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f177f-121">Example 3</span></span>

<span data-ttu-id="f177f-122">Überprüft eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="f177f-122">Validates a logic app definition.</span></span> <span data-ttu-id="f177f-123">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="f177f-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="f177f-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f177f-124">PARAMETERS</span></span>

### <span data-ttu-id="f177f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f177f-125">-DefaultProfile</span></span>
<span data-ttu-id="f177f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f177f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f177f-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="f177f-127">-Definition</span></span>
<span data-ttu-id="f177f-128">Gibt die Definition einer Logik-App als Objekt oder zeichenfolge im JavaScript-Objekt-Notation(JSON)-Format an.</span><span class="sxs-lookup"><span data-stu-id="f177f-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="f177f-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="f177f-129">-DefinitionFilePath</span></span>
<span data-ttu-id="f177f-130">Gibt die Definition Ihrer Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="f177f-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="f177f-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="f177f-131">-IntegrationAccountId</span></span>
<span data-ttu-id="f177f-132">Gibt eine Integrationskonto-ID für die Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="f177f-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="f177f-133">-Location</span><span class="sxs-lookup"><span data-stu-id="f177f-133">-Location</span></span>
<span data-ttu-id="f177f-134">Gibt den Speicherort der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="f177f-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="f177f-135">Geben Sie einen Azure-Rechenzentrumsspeicherort ein, z. B. West-USA oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="f177f-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="f177f-136">Sie können eine Logik-App an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="f177f-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="f177f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f177f-137">-Name</span></span>
<span data-ttu-id="f177f-138">Gibt den Namen der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="f177f-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="f177f-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="f177f-139">-ParameterFilePath</span></span>
<span data-ttu-id="f177f-140">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="f177f-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="f177f-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f177f-141">-Parameters</span></span>
<span data-ttu-id="f177f-142">Gibt ein Parametersammlungsobjekt der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="f177f-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="f177f-143">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="f177f-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="f177f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f177f-144">-ResourceGroupName</span></span>
<span data-ttu-id="f177f-145">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f177f-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f177f-146">-State</span><span class="sxs-lookup"><span data-stu-id="f177f-146">-State</span></span>
<span data-ttu-id="f177f-147">Gibt einen Zustand der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="f177f-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="f177f-148">Die zulässigen Werte für diesen Parameter sind: Aktiviert und Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f177f-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="f177f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f177f-149">CommonParameters</span></span>
<span data-ttu-id="f177f-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f177f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f177f-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f177f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f177f-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f177f-152">INPUTS</span></span>

### <span data-ttu-id="f177f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f177f-153">System.String</span></span>

## <span data-ttu-id="f177f-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f177f-154">OUTPUTS</span></span>

### <span data-ttu-id="f177f-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="f177f-155">System.Void</span></span>

## <span data-ttu-id="f177f-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f177f-156">NOTES</span></span>

## <span data-ttu-id="f177f-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f177f-157">RELATED LINKS</span></span>

[<span data-ttu-id="f177f-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="f177f-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="f177f-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="f177f-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="f177f-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="f177f-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


