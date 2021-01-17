---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292564"
---
# <span data-ttu-id="837be-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="837be-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="837be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="837be-102">SYNOPSIS</span></span>
<span data-ttu-id="837be-103">Beendet eine Aufgabe des Azure Database Migration Service, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="837be-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="837be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="837be-104">SYNTAX</span></span>

### <span data-ttu-id="837be-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="837be-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837be-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="837be-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837be-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="837be-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837be-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="837be-108">DESCRIPTION</span></span>
<span data-ttu-id="837be-109">Stop-AzDataMigrationTask cmdlet beendet die Datenbankmigrationsaktivität im ausgeführten Zustand.</span><span class="sxs-lookup"><span data-stu-id="837be-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="837be-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="837be-110">EXAMPLES</span></span>

### <span data-ttu-id="837be-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="837be-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="837be-112">Im vorstehenden Beispiel wird die Azure Database Migration Service-Aufgabe mit dem Namen "myDMSTask" beendet, die dem Projekt "myDMSProject" und der Azure Database Migration Service-Instanz namens "TestService" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="837be-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="837be-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="837be-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="837be-114">Im obigen Beispiel wird die Azure Database Migration Service-Aufgabe beendet, die als Eingabeparameter-PSProjectTask-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="837be-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="837be-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="837be-115">PARAMETERS</span></span>

### <span data-ttu-id="837be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837be-116">-DefaultProfile</span></span>
<span data-ttu-id="837be-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="837be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="837be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="837be-118">-InputObject</span></span>
<span data-ttu-id="837be-119">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="837be-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="837be-120">-Name</span><span class="sxs-lookup"><span data-stu-id="837be-120">-Name</span></span>
<span data-ttu-id="837be-121">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="837be-121">The name of the task.</span></span>

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

### <span data-ttu-id="837be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="837be-122">-PassThru</span></span>
<span data-ttu-id="837be-123">Gibt "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="837be-123">Returns an true/false.</span></span>
<span data-ttu-id="837be-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="837be-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="837be-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="837be-125">-ProjectName</span></span>
<span data-ttu-id="837be-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="837be-126">The name of the project.</span></span>

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

### <span data-ttu-id="837be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837be-127">-ResourceGroupName</span></span>
<span data-ttu-id="837be-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="837be-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="837be-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="837be-129">-ResourceId</span></span>
<span data-ttu-id="837be-130">ProjectTask-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="837be-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="837be-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="837be-131">-ServiceName</span></span>
<span data-ttu-id="837be-132">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="837be-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="837be-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="837be-133">-Confirm</span></span>
<span data-ttu-id="837be-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="837be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837be-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="837be-135">-WhatIf</span></span>
<span data-ttu-id="837be-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="837be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837be-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="837be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837be-138">CommonParameters</span></span>
<span data-ttu-id="837be-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837be-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837be-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837be-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="837be-141">INPUTS</span></span>

### <span data-ttu-id="837be-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="837be-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="837be-143">System.String</span><span class="sxs-lookup"><span data-stu-id="837be-143">System.String</span></span>

## <span data-ttu-id="837be-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="837be-144">OUTPUTS</span></span>

### <span data-ttu-id="837be-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="837be-145">System.Boolean</span></span>

## <span data-ttu-id="837be-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="837be-146">NOTES</span></span>

## <span data-ttu-id="837be-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="837be-147">RELATED LINKS</span></span>
