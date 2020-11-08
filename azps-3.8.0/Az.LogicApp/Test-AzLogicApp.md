---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: e13f4af6f998b069168dfffca3dedc7ba385841e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995116"
---
# <span data-ttu-id="3b1c0-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="3b1c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1c0-103">Validiert eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="3b1c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b1c0-104">SYNTAX</span></span>

### <span data-ttu-id="3b1c0-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1c0-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b1c0-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1c0-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b1c0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b1c0-107">DESCRIPTION</span></span>
<span data-ttu-id="3b1c0-108">Das Cmdlet **Test-AzLogicApp** überprüft eine Logik-App-Definition in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="3b1c0-109">Geben Sie den Namen der Logik-APP, den Namen der Ressourcengruppe, den Standort, den Zustand, die Integrations Konto-ID oder Parameter an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="3b1c0-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3b1c0-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3b1c0-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3b1c0-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3b1c0-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b1c0-114">EXAMPLES</span></span>

### <span data-ttu-id="3b1c0-115">Beispiel 1: Überprüfen einer Logik-App mithilfe von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="3b1c0-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="3b1c0-116">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="3b1c0-117">Der Befehl gibt Definitions-und Parameterdatei Pfade an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="3b1c0-118">Beispiel 2: Überprüfen einer Logik-App mithilfe von Objekten</span><span class="sxs-lookup"><span data-stu-id="3b1c0-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="3b1c0-119">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="3b1c0-120">Der Befehl gibt Definitions-und Parameterobjekte an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="3b1c0-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b1c0-121">PARAMETERS</span></span>

### <span data-ttu-id="3b1c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1c0-122">-DefaultProfile</span></span>
<span data-ttu-id="3b1c0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b1c0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b1c0-124">-Definition</span><span class="sxs-lookup"><span data-stu-id="3b1c0-124">-Definition</span></span>
<span data-ttu-id="3b1c0-125">Gibt die Definition einer Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="3b1c0-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="3b1c0-126">-DefinitionFilePath</span></span>
<span data-ttu-id="3b1c0-127">Gibt die Definition der Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="3b1c0-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="3b1c0-128">-IntegrationAccountId</span></span>
<span data-ttu-id="3b1c0-129">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="3b1c0-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="3b1c0-130">-Location</span></span>
<span data-ttu-id="3b1c0-131">Gibt den Speicherort der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="3b1c0-132">Geben Sie einen Azure Data Center-Standort ein, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="3b1c0-133">Sie können eine Logik-APP an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="3b1c0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3b1c0-134">-Name</span></span>
<span data-ttu-id="3b1c0-135">Gibt den Namen der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-135">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="3b1c0-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="3b1c0-136">-ParameterFilePath</span></span>
<span data-ttu-id="3b1c0-137">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="3b1c0-138">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3b1c0-138">-Parameters</span></span>
<span data-ttu-id="3b1c0-139">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="3b1c0-140">Geben Sie eine Hashtabelle, eine Wörterbuch \< Zeichenfolge \> oder eine Wörterbuch \< Zeichenfolge, Workflowparameter, an \> .</span><span class="sxs-lookup"><span data-stu-id="3b1c0-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="3b1c0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1c0-141">-ResourceGroupName</span></span>
<span data-ttu-id="3b1c0-142">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3b1c0-143">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="3b1c0-143">-State</span></span>
<span data-ttu-id="3b1c0-144">Gibt einen Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="3b1c0-145">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="3b1c0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1c0-146">CommonParameters</span></span>
<span data-ttu-id="3b1c0-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1c0-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1c0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1c0-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b1c0-149">INPUTS</span></span>

### <span data-ttu-id="3b1c0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3b1c0-150">System.String</span></span>

## <span data-ttu-id="3b1c0-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b1c0-151">OUTPUTS</span></span>

### <span data-ttu-id="3b1c0-152">System. void</span><span class="sxs-lookup"><span data-stu-id="3b1c0-152">System.Void</span></span>

## <span data-ttu-id="3b1c0-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b1c0-153">NOTES</span></span>

## <span data-ttu-id="3b1c0-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b1c0-154">RELATED LINKS</span></span>

[<span data-ttu-id="3b1c0-155">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-155">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="3b1c0-156">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-156">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="3b1c0-157">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-157">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="3b1c0-158">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-158">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="3b1c0-159">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3b1c0-159">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


