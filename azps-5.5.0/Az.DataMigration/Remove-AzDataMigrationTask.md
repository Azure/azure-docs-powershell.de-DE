---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148073"
---
# <span data-ttu-id="0cf54-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0cf54-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="0cf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf54-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf54-103">Entfernt eine Aufgabe des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf54-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="0cf54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cf54-104">SYNTAX</span></span>

### <span data-ttu-id="0cf54-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cf54-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cf54-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cf54-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf54-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cf54-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf54-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cf54-108">DESCRIPTION</span></span>
<span data-ttu-id="0cf54-109">Das Remove-AzDataMigrationTask entfernt eine Azure-Datenbankmigrationsdienstaufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf54-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="0cf54-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0cf54-110">EXAMPLES</span></span>

### <span data-ttu-id="0cf54-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cf54-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0cf54-112">Im vorherigen Beispiel wird eine Azure-Datenbankmigrationsdienst-Aufgabe mit dem Namen "TestTask" basierend auf dem Parameter "Aufgabenname" aus Azure entfernt.</span><span class="sxs-lookup"><span data-stu-id="0cf54-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="0cf54-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0cf54-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="0cf54-114">Im vorherigen Beispiel wird eine Azure Database Migration Service-Aufgabe basierend auf dem übergebenen "PSProjectTask"-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="0cf54-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="0cf54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf54-115">PARAMETERS</span></span>

### <span data-ttu-id="0cf54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf54-116">-DefaultProfile</span></span>
<span data-ttu-id="0cf54-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cf54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf54-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0cf54-118">-Force</span></span>
<span data-ttu-id="0cf54-119">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="0cf54-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0cf54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cf54-120">-InputObject</span></span>
<span data-ttu-id="0cf54-121">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0cf54-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0cf54-122">-Name</span></span>
<span data-ttu-id="0cf54-123">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0cf54-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cf54-124">-PassThru</span></span>
<span data-ttu-id="0cf54-125">Gibt "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="0cf54-125">Returns an true/false.</span></span>
<span data-ttu-id="0cf54-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0cf54-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0cf54-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="0cf54-127">-ProjectName</span></span>
<span data-ttu-id="0cf54-128">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="0cf54-128">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf54-129">-ResourceGroupName</span></span>
<span data-ttu-id="0cf54-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0cf54-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf54-131">-ResourceId</span></span>
<span data-ttu-id="0cf54-132">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0cf54-132">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0cf54-133">-ServiceName</span></span>
<span data-ttu-id="0cf54-134">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="0cf54-134">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf54-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cf54-135">-Confirm</span></span>
<span data-ttu-id="0cf54-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cf54-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf54-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0cf54-137">-WhatIf</span></span>
<span data-ttu-id="0cf54-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cf54-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf54-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cf54-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf54-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf54-140">CommonParameters</span></span>
<span data-ttu-id="0cf54-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf54-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf54-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf54-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf54-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0cf54-143">INPUTS</span></span>

### <span data-ttu-id="0cf54-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="0cf54-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="0cf54-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0cf54-145">System.String</span></span>

## <span data-ttu-id="0cf54-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0cf54-146">OUTPUTS</span></span>

### <span data-ttu-id="0cf54-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0cf54-147">System.Boolean</span></span>

## <span data-ttu-id="0cf54-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0cf54-148">NOTES</span></span>

## <span data-ttu-id="0cf54-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0cf54-149">RELATED LINKS</span></span>
