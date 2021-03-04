---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941880"
---
# <span data-ttu-id="9898b-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9898b-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="9898b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9898b-102">SYNOPSIS</span></span>
<span data-ttu-id="9898b-103">Entfernt eine Azure-Datenbankmigrationsdienstaufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="9898b-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="9898b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9898b-104">SYNTAX</span></span>

### <span data-ttu-id="9898b-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9898b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9898b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9898b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9898b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9898b-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9898b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9898b-108">DESCRIPTION</span></span>
<span data-ttu-id="9898b-109">Das Remove-AzDataMigrationTask-Cmdlet entfernt eine Azure-Datenbankmigrationsdienstaufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="9898b-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="9898b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9898b-110">EXAMPLES</span></span>

### <span data-ttu-id="9898b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9898b-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="9898b-112">Im vorherigen Beispiel wird eine Azure-Datenbankmigrationsdienstaufgabe namens TestTask aus Azure entfernt, die auf dem Parameter "Vorgangsname" basiert.</span><span class="sxs-lookup"><span data-stu-id="9898b-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="9898b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9898b-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="9898b-114">Im vorherigen Beispiel wird eine Azure-Datenbankmigrationsdienstaufgabe entfernt, die auf dem übergebenen PSProjectTask-Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="9898b-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="9898b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9898b-115">PARAMETERS</span></span>

### <span data-ttu-id="9898b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9898b-116">-DefaultProfile</span></span>
<span data-ttu-id="9898b-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9898b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9898b-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="9898b-118">-Force</span></span>
<span data-ttu-id="9898b-119">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="9898b-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9898b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9898b-120">-InputObject</span></span>
<span data-ttu-id="9898b-121">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9898b-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="9898b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9898b-122">-Name</span></span>
<span data-ttu-id="9898b-123">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9898b-123">The name of the task.</span></span>

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

### <span data-ttu-id="9898b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9898b-124">-PassThru</span></span>
<span data-ttu-id="9898b-125">Gibt den Wert "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="9898b-125">Returns an true/false.</span></span>
<span data-ttu-id="9898b-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="9898b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9898b-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9898b-127">-ProjectName</span></span>
<span data-ttu-id="9898b-128">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="9898b-128">The name of the project.</span></span>

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

### <span data-ttu-id="9898b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9898b-129">-ResourceGroupName</span></span>
<span data-ttu-id="9898b-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9898b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9898b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9898b-131">-ResourceId</span></span>
<span data-ttu-id="9898b-132">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9898b-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="9898b-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9898b-133">-ServiceName</span></span>
<span data-ttu-id="9898b-134">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="9898b-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9898b-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9898b-135">-Confirm</span></span>
<span data-ttu-id="9898b-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9898b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9898b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9898b-137">-WhatIf</span></span>
<span data-ttu-id="9898b-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9898b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9898b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9898b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9898b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9898b-140">CommonParameters</span></span>
<span data-ttu-id="9898b-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9898b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9898b-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9898b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9898b-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9898b-143">INPUTS</span></span>

### <span data-ttu-id="9898b-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="9898b-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="9898b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9898b-145">System.String</span></span>

## <span data-ttu-id="9898b-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9898b-146">OUTPUTS</span></span>

### <span data-ttu-id="9898b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9898b-147">System.Boolean</span></span>

## <span data-ttu-id="9898b-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9898b-148">NOTES</span></span>

## <span data-ttu-id="9898b-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9898b-149">RELATED LINKS</span></span>
