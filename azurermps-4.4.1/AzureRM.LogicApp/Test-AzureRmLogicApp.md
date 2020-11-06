---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505902"
---
# <span data-ttu-id="40276-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="40276-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40276-102">SYNOPSIS</span></span>
<span data-ttu-id="40276-103">Validiert eine Logik-App-Definition.</span><span class="sxs-lookup"><span data-stu-id="40276-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40276-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40276-104">SYNTAX</span></span>

### <span data-ttu-id="40276-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="40276-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40276-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="40276-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40276-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40276-107">DESCRIPTION</span></span>
<span data-ttu-id="40276-108">Das Cmdlet **Test-AzureRmLogicApp** überprüft eine Logik-App-Definition in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40276-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="40276-109">Geben Sie den Namen der Logik-APP, den Namen der Ressourcengruppe, den Standort, den Zustand, die Integrations Konto-ID oder Parameter an.</span><span class="sxs-lookup"><span data-stu-id="40276-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="40276-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="40276-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="40276-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="40276-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="40276-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="40276-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="40276-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="40276-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="40276-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40276-114">EXAMPLES</span></span>

### <span data-ttu-id="40276-115">Beispiel 1: Überprüfen einer Logik-App mithilfe von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="40276-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="40276-116">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40276-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="40276-117">Der Befehl gibt Definitions-und Parameterdatei Pfade an.</span><span class="sxs-lookup"><span data-stu-id="40276-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="40276-118">Beispiel 2: Überprüfen einer Logik-App mithilfe von Objekten</span><span class="sxs-lookup"><span data-stu-id="40276-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="40276-119">Dieser Befehl überprüft eine Logik-App mit dem Namen LogicApp01 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40276-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="40276-120">Der Befehl gibt Definitions-und Parameterobjekte an.</span><span class="sxs-lookup"><span data-stu-id="40276-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="40276-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="40276-121">PARAMETERS</span></span>

### <span data-ttu-id="40276-122">-Definition</span><span class="sxs-lookup"><span data-stu-id="40276-122">-Definition</span></span>
<span data-ttu-id="40276-123">Gibt die Definition einer Logik-App als ein Objekt oder eine Zeichenfolge im JSON-Format (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="40276-123">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="40276-124">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="40276-124">-DefinitionFilePath</span></span>
<span data-ttu-id="40276-125">Gibt die Definition der Logik-App als Pfad einer Definitionsdatei im JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="40276-125">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="40276-126">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="40276-126">-IntegrationAccountId</span></span>
<span data-ttu-id="40276-127">Gibt eine Integrations Konto-ID für die Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="40276-127">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="40276-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="40276-128">-Location</span></span>
<span data-ttu-id="40276-129">Gibt den Speicherort der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="40276-129">Specifies the location of the logic app.</span></span>
<span data-ttu-id="40276-130">Geben Sie einen Azure Data Center-Standort ein, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="40276-130">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="40276-131">Sie können eine Logik-APP an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="40276-131">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="40276-132">-Name</span><span class="sxs-lookup"><span data-stu-id="40276-132">-Name</span></span>
<span data-ttu-id="40276-133">Gibt den Namen der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="40276-133">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="40276-134">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="40276-134">-ParameterFilePath</span></span>
<span data-ttu-id="40276-135">Gibt den Pfad einer JSON-formatierten Parameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="40276-135">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="40276-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="40276-136">-Parameters</span></span>
<span data-ttu-id="40276-137">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="40276-137">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="40276-138">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="40276-138">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="40276-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40276-139">-ResourceGroupName</span></span>
<span data-ttu-id="40276-140">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="40276-140">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40276-141">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="40276-141">-State</span></span>
<span data-ttu-id="40276-142">Gibt einen Zustand der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="40276-142">Specifies a state of the logic app.</span></span>
<span data-ttu-id="40276-143">Die zulässigen Werte für diesen Parameter sind: aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40276-143">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="40276-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40276-144">-DefaultProfile</span></span>
<span data-ttu-id="40276-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40276-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40276-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40276-146">CommonParameters</span></span>
<span data-ttu-id="40276-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40276-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40276-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40276-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40276-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40276-149">INPUTS</span></span>

## <span data-ttu-id="40276-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40276-150">OUTPUTS</span></span>

### <span data-ttu-id="40276-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="40276-151">System.Object</span></span>

## <span data-ttu-id="40276-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="40276-152">NOTES</span></span>

## <span data-ttu-id="40276-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40276-153">RELATED LINKS</span></span>

[<span data-ttu-id="40276-154">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-154">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="40276-155">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-155">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="40276-156">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-156">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="40276-157">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-157">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="40276-158">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="40276-158">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


