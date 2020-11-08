---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173752"
---
# <span data-ttu-id="bb9f3-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="bb9f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9f3-103">Validiert eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="bb9f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb9f3-104">SYNTAX</span></span>

### <span data-ttu-id="bb9f3-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb9f3-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb9f3-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb9f3-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb9f3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb9f3-107">DESCRIPTION</span></span>
<span data-ttu-id="bb9f3-108">Das Cmdlet **Test-AzLogicApp** überprüft eine Logik-App-Definition in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="bb9f3-109">Geben Sie den Namen der Logik-APP, den Namen der Ressourcengruppe, den Standort, den Zustand, die Integrations Konto-ID oder Parameter an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="bb9f3-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bb9f3-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bb9f3-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bb9f3-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bb9f3-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb9f3-114">EXAMPLES</span></span>

### <span data-ttu-id="bb9f3-115">Beispiel 1: Überprüfen einer Logik-App mithilfe von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="bb9f3-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="bb9f3-116">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="bb9f3-117">Der Befehl gibt Definitions-und Parameterdatei Pfade an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="bb9f3-118">Beispiel 2: Überprüfen einer Logik-App mithilfe von Objekten</span><span class="sxs-lookup"><span data-stu-id="bb9f3-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="bb9f3-119">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="bb9f3-120">Der Befehl gibt Definitions-und Parameterobjekte an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="bb9f3-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bb9f3-121">Example 3</span></span>

<span data-ttu-id="bb9f3-122">Validiert eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-122">Validates a logic app definition.</span></span> <span data-ttu-id="bb9f3-123">automatisch</span><span class="sxs-lookup"><span data-stu-id="bb9f3-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="bb9f3-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb9f3-124">PARAMETERS</span></span>

### <span data-ttu-id="bb9f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9f3-125">-DefaultProfile</span></span>
<span data-ttu-id="bb9f3-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb9f3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb9f3-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="bb9f3-127">-Definition</span></span>
<span data-ttu-id="bb9f3-128">Gibt die Definition einer Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="bb9f3-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="bb9f3-129">-DefinitionFilePath</span></span>
<span data-ttu-id="bb9f3-130">Gibt die Definition der Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="bb9f3-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="bb9f3-131">-IntegrationAccountId</span></span>
<span data-ttu-id="bb9f3-132">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="bb9f3-133">-Standort</span><span class="sxs-lookup"><span data-stu-id="bb9f3-133">-Location</span></span>
<span data-ttu-id="bb9f3-134">Gibt den Speicherort der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="bb9f3-135">Geben Sie einen Azure Data Center-Standort ein, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="bb9f3-136">Sie können eine Logik-APP an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="bb9f3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="bb9f3-137">-Name</span></span>
<span data-ttu-id="bb9f3-138">Gibt den Namen der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="bb9f3-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="bb9f3-139">-ParameterFilePath</span></span>
<span data-ttu-id="bb9f3-140">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="bb9f3-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="bb9f3-141">-Parameters</span></span>
<span data-ttu-id="bb9f3-142">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="bb9f3-143">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="bb9f3-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="bb9f3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb9f3-144">-ResourceGroupName</span></span>
<span data-ttu-id="bb9f3-145">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bb9f3-146">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="bb9f3-146">-State</span></span>
<span data-ttu-id="bb9f3-147">Gibt einen Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="bb9f3-148">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="bb9f3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9f3-149">CommonParameters</span></span>
<span data-ttu-id="bb9f3-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb9f3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9f3-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9f3-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9f3-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb9f3-152">INPUTS</span></span>

### <span data-ttu-id="bb9f3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="bb9f3-153">System.String</span></span>

## <span data-ttu-id="bb9f3-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb9f3-154">OUTPUTS</span></span>

### <span data-ttu-id="bb9f3-155">System. void</span><span class="sxs-lookup"><span data-stu-id="bb9f3-155">System.Void</span></span>

## <span data-ttu-id="bb9f3-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb9f3-156">NOTES</span></span>

## <span data-ttu-id="bb9f3-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb9f3-157">RELATED LINKS</span></span>

[<span data-ttu-id="bb9f3-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="bb9f3-159">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="bb9f3-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="bb9f3-161">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="bb9f3-162">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bb9f3-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


