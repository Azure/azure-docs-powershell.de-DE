---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458021"
---
# <span data-ttu-id="b4bdc-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b4bdc-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="b4bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bdc-103">Ruft das PSProjectTask-Objekt ab, das einer Migrationsaufgabe des Azure Database Migration Service zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b4bdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4bdc-104">SYNTAX</span></span>

### <span data-ttu-id="b4bdc-105">ListByComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4bdc-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4bdc-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4bdc-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="b4bdc-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bdc-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bdc-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="b4bdc-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="b4bdc-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4bdc-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="b4bdc-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4bdc-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4bdc-114">DESCRIPTION</span></span>
<span data-ttu-id="b4bdc-115">Das Get-AzDataMigrationTask ruft die Eigenschaften ab, die einer Migrationsaufgabe des Azure Database Migration Service zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b4bdc-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4bdc-116">EXAMPLES</span></span>

### <span data-ttu-id="b4bdc-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4bdc-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="b4bdc-118">Das oben gezeigte Beispiel veranschaulicht die Verwendung des Cmdlets Get-AzDataMigrationTask Zum Abrufen der Eigenschaften, die einer Migrationsaufgabe des Azure Database Migration Service zugeordnet sind, basierend auf dem Aufgabennamen, der als Eingabeparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="b4bdc-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4bdc-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="b4bdc-120">Das beispiel oben veranschaulicht die Verwendung des Get-AzDataMigrationTask-Cmdlets zum Abrufen aller Migrationsaufgaben, die mit dem als Eingabeparameter übergebenen "PSProject"-Objekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="b4bdc-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4bdc-121">PARAMETERS</span></span>

### <span data-ttu-id="b4bdc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bdc-122">-DefaultProfile</span></span>
<span data-ttu-id="b4bdc-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bdc-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="b4bdc-124">-Expand</span></span>
<span data-ttu-id="b4bdc-125">Ausgabe erweitern</span><span class="sxs-lookup"><span data-stu-id="b4bdc-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4bdc-126">-InputObject</span></span>
<span data-ttu-id="b4bdc-127">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b4bdc-128">-Name</span></span>
<span data-ttu-id="b4bdc-129">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="b4bdc-130">-ProjectName</span></span>
<span data-ttu-id="b4bdc-131">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bdc-132">-ResourceGroupName</span></span>
<span data-ttu-id="b4bdc-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bdc-134">-ResourceId</span></span>
<span data-ttu-id="b4bdc-135">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="b4bdc-136">-ResultType</span></span>
<span data-ttu-id="b4bdc-137">Erweitern der Ausgabe eines bestimmten Ergebnistyps</span><span class="sxs-lookup"><span data-stu-id="b4bdc-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b4bdc-138">-ServiceName</span></span>
<span data-ttu-id="b4bdc-139">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="b4bdc-140">-TaskType</span></span>
<span data-ttu-id="b4bdc-141">Filtern sie nach TaskType.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bdc-142">CommonParameters</span></span>
<span data-ttu-id="b4bdc-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bdc-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bdc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bdc-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4bdc-145">INPUTS</span></span>

### <span data-ttu-id="b4bdc-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="b4bdc-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b4bdc-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b4bdc-147">System.String</span></span>

## <span data-ttu-id="b4bdc-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4bdc-148">OUTPUTS</span></span>

### <span data-ttu-id="b4bdc-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="b4bdc-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="b4bdc-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4bdc-150">NOTES</span></span>

## <span data-ttu-id="b4bdc-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4bdc-151">RELATED LINKS</span></span>
