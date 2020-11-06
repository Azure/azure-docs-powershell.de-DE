---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482989"
---
# <span data-ttu-id="95f57-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="95f57-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="95f57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95f57-102">SYNOPSIS</span></span>
<span data-ttu-id="95f57-103">Ruft das PSProjectTask-Objekt ab, das einem Azure Database Migration Service-Migrationsvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95f57-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f57-104">SYNTAX</span></span>

### <span data-ttu-id="95f57-105">ListByComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="95f57-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="95f57-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="95f57-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="95f57-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="95f57-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="95f57-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="95f57-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="95f57-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="95f57-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="95f57-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="95f57-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95f57-114">DESCRIPTION</span></span>
<span data-ttu-id="95f57-115">Das Get-AzureRmDataMigrationTask-Cmdlet ruft die Eigenschaften ab, die einem Azure Database Migration Service-Migrationsvorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95f57-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="95f57-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95f57-116">EXAMPLES</span></span>

### <span data-ttu-id="95f57-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95f57-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="95f57-118">Das obige Beispiel veranschaulicht die Verwendung von Get-AzureRmDataMigrationTask-Cmdlet zum Abrufen der Eigenschaften, die einem Azure Database Migration Service-Migrationsdienst basierend auf dem als Eingabeparameter übergebenen Aufgabennamen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95f57-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="95f57-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95f57-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="95f57-120">Das obige Beispiel veranschaulicht die Verwendung von Get-AzureRmDataMigrationTask-Cmdlet zum Abrufen aller Migrationsaufgaben, die mit dem als Eingabeparameter übergebenen PSProject-Objekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="95f57-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="95f57-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="95f57-121">PARAMETERS</span></span>

### <span data-ttu-id="95f57-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f57-122">-DefaultProfile</span></span>
<span data-ttu-id="95f57-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95f57-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-124">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="95f57-124">-Expand</span></span>
<span data-ttu-id="95f57-125">Ausgabe erweitern</span><span class="sxs-lookup"><span data-stu-id="95f57-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="95f57-126">-InputObject</span></span>
<span data-ttu-id="95f57-127">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95f57-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-128">-Name</span><span class="sxs-lookup"><span data-stu-id="95f57-128">-Name</span></span>
<span data-ttu-id="95f57-129">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="95f57-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="95f57-130">-ProjectName</span></span>
<span data-ttu-id="95f57-131">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="95f57-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f57-132">-ResourceGroupName</span></span>
<span data-ttu-id="95f57-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95f57-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="95f57-134">-ResourceId</span></span>
<span data-ttu-id="95f57-135">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="95f57-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-136">-Ergebnistyp</span><span class="sxs-lookup"><span data-stu-id="95f57-136">-ResultType</span></span>
<span data-ttu-id="95f57-137">Ausgabe des angegebenen Ergebnistyps erweitern</span><span class="sxs-lookup"><span data-stu-id="95f57-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95f57-138">-ServiceName</span></span>
<span data-ttu-id="95f57-139">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="95f57-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f57-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="95f57-140">-TaskType</span></span>
<span data-ttu-id="95f57-141">Nach TaskType Filtern</span><span class="sxs-lookup"><span data-stu-id="95f57-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="95f57-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95f57-142">INPUTS</span></span>

### <span data-ttu-id="95f57-143">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="95f57-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="95f57-144">System. String</span><span class="sxs-lookup"><span data-stu-id="95f57-144">System.String</span></span>

## <span data-ttu-id="95f57-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95f57-145">OUTPUTS</span></span>

### <span data-ttu-id="95f57-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. datamigration. Models. PSProjectTask, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="95f57-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="95f57-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="95f57-147">NOTES</span></span>

## <span data-ttu-id="95f57-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95f57-148">RELATED LINKS</span></span>

