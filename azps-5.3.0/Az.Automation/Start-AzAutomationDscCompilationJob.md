---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471238"
---
# <span data-ttu-id="4334f-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="4334f-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="4334f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4334f-102">SYNOPSIS</span></span>
<span data-ttu-id="4334f-103">Kompiliert eine DSC-Konfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="4334f-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="4334f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4334f-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4334f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4334f-105">DESCRIPTION</span></span>
<span data-ttu-id="4334f-106">Das **Cmdlet "Start-AzAutomationDscCompilationJob"** kompiliert eine Konfiguration der APS Desired State Configuration (DSC) in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="4334f-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="4334f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4334f-107">EXAMPLES</span></span>

### <span data-ttu-id="4334f-108">Beispiel 1: Kompilieren einer Azure -DSC-Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="4334f-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4334f-109">Der erste Befehl erstellt ein Wörterbuch mit Parametern und speichert sie in der $Params Variable.</span><span class="sxs-lookup"><span data-stu-id="4334f-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="4334f-110">Der zweite Befehl kompiliert die DSC-Konfiguration namens "Config01".</span><span class="sxs-lookup"><span data-stu-id="4334f-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="4334f-111">Der Befehl enthält die Werte in $Params für DSC-Konfigurationsparameter.</span><span class="sxs-lookup"><span data-stu-id="4334f-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="4334f-112">Beispiel 2: Kompilieren einer Azure -DSC-Konfiguration in der Automatisierung mit einer neuen Buildversion der Knotenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4334f-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="4334f-113">Ähnlich wie im ersten Beispiel erstellt der erste Befehl ein Wörterbuch mit Parametern und speichert sie in der $Params Variable.</span><span class="sxs-lookup"><span data-stu-id="4334f-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="4334f-114">Der zweite Befehl kompiliert die DSC-Konfiguration namens "Config01".</span><span class="sxs-lookup"><span data-stu-id="4334f-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="4334f-115">Der Befehl enthält die Werte in $Params für DSC-Konfigurationsparameter.</span><span class="sxs-lookup"><span data-stu-id="4334f-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="4334f-116">Die zuvor vorhandene Knotenkonfiguration wird nicht überschrieben, indem eine neue Knotenkonfiguration mit dem Namen "Config01[<2>] erstellt <NodeName> wird.</span><span class="sxs-lookup"><span data-stu-id="4334f-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="4334f-117">Die Versionsnummer wird basierend auf der vorhandenen Versionsnummer, die bereits vorhanden ist, erhöht.</span><span class="sxs-lookup"><span data-stu-id="4334f-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="4334f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4334f-118">PARAMETERS</span></span>

### <span data-ttu-id="4334f-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4334f-119">-AutomationAccountName</span></span>
<span data-ttu-id="4334f-120">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4334f-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="4334f-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="4334f-121">-ConfigurationData</span></span>
<span data-ttu-id="4334f-122">Gibt ein Wörterbuch mit Konfigurationsdaten für die DSC-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="4334f-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="4334f-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4334f-123">-ConfigurationName</span></span>
<span data-ttu-id="4334f-124">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4334f-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="4334f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4334f-125">-DefaultProfile</span></span>
<span data-ttu-id="4334f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4334f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4334f-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="4334f-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="4334f-128">Erstellt eine neue Buildversion der Knotenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4334f-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="4334f-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4334f-129">-Parameters</span></span>
<span data-ttu-id="4334f-130">Gibt ein Wörterbuch mit Parametern an, das von diesem Cmdlet zum Kompilieren der DSC-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4334f-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="4334f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4334f-131">-ResourceGroupName</span></span>
<span data-ttu-id="4334f-132">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4334f-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="4334f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4334f-133">-Confirm</span></span>
<span data-ttu-id="4334f-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4334f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4334f-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4334f-135">-WhatIf</span></span>
<span data-ttu-id="4334f-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4334f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4334f-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4334f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4334f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4334f-138">CommonParameters</span></span>
<span data-ttu-id="4334f-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4334f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4334f-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4334f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4334f-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4334f-141">INPUTS</span></span>

### <span data-ttu-id="4334f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4334f-142">System.String</span></span>

## <span data-ttu-id="4334f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4334f-143">OUTPUTS</span></span>

### <span data-ttu-id="4334f-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="4334f-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="4334f-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4334f-145">NOTES</span></span>

## <span data-ttu-id="4334f-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4334f-146">RELATED LINKS</span></span>

[<span data-ttu-id="4334f-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="4334f-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="4334f-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="4334f-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


