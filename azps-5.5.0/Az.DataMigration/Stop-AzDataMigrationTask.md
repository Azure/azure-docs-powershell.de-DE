---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165313"
---
# <span data-ttu-id="2cba6-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2cba6-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="2cba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cba6-102">SYNOPSIS</span></span>
<span data-ttu-id="2cba6-103">Beendet eine Aufgabe des Azure Database Migration Service, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="2cba6-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="2cba6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cba6-104">SYNTAX</span></span>

### <span data-ttu-id="2cba6-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cba6-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cba6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cba6-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cba6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cba6-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cba6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cba6-108">DESCRIPTION</span></span>
<span data-ttu-id="2cba6-109">Stop-AzDataMigrationTask cmdlet beendet die Datenbankmigrationsaktivität im ausgeführten Zustand.</span><span class="sxs-lookup"><span data-stu-id="2cba6-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="2cba6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cba6-110">EXAMPLES</span></span>

### <span data-ttu-id="2cba6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cba6-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="2cba6-112">Im vorstehenden Beispiel wird die Azure Database Migration Service-Aufgabe mit dem Namen "myDMSTask" beendet, die dem Projekt "myDMSProject" und der Azure Database Migration Service-Instanz namens "TestService" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2cba6-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="2cba6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2cba6-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="2cba6-114">Im obigen Beispiel wird die Azure Database Migration Service-Aufgabe beendet, die als Eingabeparameter-PSProjectTask-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2cba6-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="2cba6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cba6-115">PARAMETERS</span></span>

### <span data-ttu-id="2cba6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cba6-116">-DefaultProfile</span></span>
<span data-ttu-id="2cba6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cba6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cba6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cba6-118">-InputObject</span></span>
<span data-ttu-id="2cba6-119">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2cba6-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="2cba6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2cba6-120">-Name</span></span>
<span data-ttu-id="2cba6-121">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2cba6-121">The name of the task.</span></span>

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

### <span data-ttu-id="2cba6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cba6-122">-PassThru</span></span>
<span data-ttu-id="2cba6-123">Gibt "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="2cba6-123">Returns an true/false.</span></span>
<span data-ttu-id="2cba6-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2cba6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2cba6-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2cba6-125">-ProjectName</span></span>
<span data-ttu-id="2cba6-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="2cba6-126">The name of the project.</span></span>

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

### <span data-ttu-id="2cba6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cba6-127">-ResourceGroupName</span></span>
<span data-ttu-id="2cba6-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cba6-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="2cba6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cba6-129">-ResourceId</span></span>
<span data-ttu-id="2cba6-130">ProjectTask-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2cba6-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="2cba6-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2cba6-131">-ServiceName</span></span>
<span data-ttu-id="2cba6-132">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="2cba6-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2cba6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cba6-133">-Confirm</span></span>
<span data-ttu-id="2cba6-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cba6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cba6-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2cba6-135">-WhatIf</span></span>
<span data-ttu-id="2cba6-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cba6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cba6-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cba6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cba6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cba6-138">CommonParameters</span></span>
<span data-ttu-id="2cba6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cba6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cba6-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cba6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cba6-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cba6-141">INPUTS</span></span>

### <span data-ttu-id="2cba6-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2cba6-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="2cba6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2cba6-143">System.String</span></span>

## <span data-ttu-id="2cba6-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cba6-144">OUTPUTS</span></span>

### <span data-ttu-id="2cba6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2cba6-145">System.Boolean</span></span>

## <span data-ttu-id="2cba6-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cba6-146">NOTES</span></span>

## <span data-ttu-id="2cba6-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cba6-147">RELATED LINKS</span></span>
