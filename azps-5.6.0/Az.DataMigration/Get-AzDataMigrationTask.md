---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 08f87d40eec10f10b12f568cae8e899f5b7468d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924992"
---
# <span data-ttu-id="f67ff-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f67ff-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="f67ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f67ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f67ff-103">Ruft das PSProjectTask-Objekt ab, das einer Azure Database Migration Service-Migrationsaufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f67ff-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="f67ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f67ff-104">SYNTAX</span></span>

### <span data-ttu-id="f67ff-105">ListByComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="f67ff-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="f67ff-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f67ff-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="f67ff-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="f67ff-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f67ff-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="f67ff-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="f67ff-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f67ff-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="f67ff-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f67ff-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f67ff-114">DESCRIPTION</span></span>
<span data-ttu-id="f67ff-115">Das Get-AzDataMigrationTask-Cmdlet ruft die Eigenschaften ab, die einer Azure Database Migration Service-Migrationsaufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f67ff-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="f67ff-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f67ff-116">EXAMPLES</span></span>

### <span data-ttu-id="f67ff-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f67ff-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="f67ff-118">Das vorstehende Beispiel veranschaulicht die Verwendung Get-AzDataMigrationTask-Cmdlets zum Abrufen der Eigenschaften, die einer Azure Database Migration Service-Migrationsaufgabe zugeordnet sind, basierend auf dem als Eingabeparameter übergebenen Aufgabennamen.</span><span class="sxs-lookup"><span data-stu-id="f67ff-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="f67ff-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f67ff-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="f67ff-120">Das vorstehende Beispiel veranschaulicht die Verwendung Get-AzDataMigrationTask-Cmdlets zum Abrufen aller Migrationsaufgaben, die dem als Eingabeparameter übergebenen PSProject-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f67ff-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="f67ff-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f67ff-121">PARAMETERS</span></span>

### <span data-ttu-id="f67ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67ff-122">-DefaultProfile</span></span>
<span data-ttu-id="f67ff-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f67ff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f67ff-124">-Erweitern</span><span class="sxs-lookup"><span data-stu-id="f67ff-124">-Expand</span></span>
<span data-ttu-id="f67ff-125">Ausgabe erweitern</span><span class="sxs-lookup"><span data-stu-id="f67ff-125">Expand output</span></span>

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

### <span data-ttu-id="f67ff-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f67ff-126">-InputObject</span></span>
<span data-ttu-id="f67ff-127">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f67ff-127">PSProject Object.</span></span>

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

### <span data-ttu-id="f67ff-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f67ff-128">-Name</span></span>
<span data-ttu-id="f67ff-129">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="f67ff-129">The name of the task.</span></span>

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

### <span data-ttu-id="f67ff-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f67ff-130">-ProjectName</span></span>
<span data-ttu-id="f67ff-131">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="f67ff-131">The name of the project.</span></span>

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

### <span data-ttu-id="f67ff-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f67ff-132">-ResourceGroupName</span></span>
<span data-ttu-id="f67ff-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f67ff-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="f67ff-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f67ff-134">-ResourceId</span></span>
<span data-ttu-id="f67ff-135">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f67ff-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="f67ff-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="f67ff-136">-ResultType</span></span>
<span data-ttu-id="f67ff-137">Erweitern Sie die Ausgabe eines bestimmten Ergebnistyps.</span><span class="sxs-lookup"><span data-stu-id="f67ff-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="f67ff-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f67ff-138">-ServiceName</span></span>
<span data-ttu-id="f67ff-139">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="f67ff-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="f67ff-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="f67ff-140">-TaskType</span></span>
<span data-ttu-id="f67ff-141">Filtern sie nach TaskType.</span><span class="sxs-lookup"><span data-stu-id="f67ff-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="f67ff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67ff-142">CommonParameters</span></span>
<span data-ttu-id="f67ff-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67ff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67ff-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67ff-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67ff-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f67ff-145">INPUTS</span></span>

### <span data-ttu-id="f67ff-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="f67ff-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="f67ff-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f67ff-147">System.String</span></span>

## <span data-ttu-id="f67ff-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f67ff-148">OUTPUTS</span></span>

### <span data-ttu-id="f67ff-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="f67ff-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="f67ff-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f67ff-150">NOTES</span></span>

## <span data-ttu-id="f67ff-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f67ff-151">RELATED LINKS</span></span>
