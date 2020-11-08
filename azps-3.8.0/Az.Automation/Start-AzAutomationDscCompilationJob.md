---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995278"
---
# <span data-ttu-id="7b3ad-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7b3ad-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="7b3ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3ad-103">Kompiliert eine DSC-Konfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="7b3ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b3ad-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b3ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3ad-106">Das Cmdlet **Start-AzAutomationDscCompilationJob** kompiliert eine APS-Konfiguration (Desired State Configuration, DSC) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="7b3ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b3ad-107">EXAMPLES</span></span>

### <span data-ttu-id="7b3ad-108">Beispiel 1: Kompilieren einer Azure DSC-Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="7b3ad-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b3ad-109">Der erste Befehl erstellt ein Wörterbuch mit Parametern und speichert Sie in der $params-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="7b3ad-110">Der zweite Befehl kompiliert die DSC-Konfiguration mit dem Namen Config01.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="7b3ad-111">Der Befehl enthält die Werte in $params für DSC-Konfigurationsparameter.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="7b3ad-112">Beispiel 2: Kompilieren einer Azure DSC-Konfiguration in der Automatisierung mit einer neuen Buildversion für die Knoten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="7b3ad-113">Ähnlich wie im ersten Beispiel erstellt der erste Befehl ein Wörterbuch mit Parametern und speichert Sie in der $params-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="7b3ad-114">Der zweite Befehl kompiliert die DSC-Konfiguration mit dem Namen Config01.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="7b3ad-115">Der Befehl enthält die Werte in $params für DSC-Konfigurationsparameter.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="7b3ad-116">Die zuvor vorhandene Knoten Konfiguration wird nicht durch Erstellen einer neuen Knoten Konfiguration mit dem Namen Config01 [<2>] überschrieben <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="7b3ad-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="7b3ad-117">Die Versionsnummer wird basierend auf der bereits vorhandenen Versionsnummer inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="7b3ad-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b3ad-118">PARAMETERS</span></span>

### <span data-ttu-id="7b3ad-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b3ad-119">-AutomationAccountName</span></span>
<span data-ttu-id="7b3ad-120">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="7b3ad-121">-ConfigurationData</span></span>
<span data-ttu-id="7b3ad-122">Gibt ein Verzeichnis mit Konfigurationsdaten für die DSC-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7b3ad-123">-ConfigurationName</span></span>
<span data-ttu-id="7b3ad-124">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet kompiliert.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3ad-125">-DefaultProfile</span></span>
<span data-ttu-id="7b3ad-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7b3ad-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b3ad-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="7b3ad-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="7b3ad-128">Erstellt eine neue Buildversion für die Knoten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-129">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7b3ad-129">-Parameters</span></span>
<span data-ttu-id="7b3ad-130">Gibt ein Wörterbuch mit Parametern an, mit denen dieses Cmdlet die DSC-Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="7b3ad-132">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b3ad-133">-Confirm</span></span>
<span data-ttu-id="7b3ad-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3ad-135">-WhatIf</span></span>
<span data-ttu-id="7b3ad-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b3ad-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3ad-138">CommonParameters</span></span>
<span data-ttu-id="7b3ad-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3ad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3ad-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3ad-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3ad-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b3ad-141">INPUTS</span></span>

### <span data-ttu-id="7b3ad-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7b3ad-142">System.String</span></span>

## <span data-ttu-id="7b3ad-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b3ad-143">OUTPUTS</span></span>

### <span data-ttu-id="7b3ad-144">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="7b3ad-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="7b3ad-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b3ad-145">NOTES</span></span>

## <span data-ttu-id="7b3ad-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b3ad-146">RELATED LINKS</span></span>

[<span data-ttu-id="7b3ad-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7b3ad-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="7b3ad-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7b3ad-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


