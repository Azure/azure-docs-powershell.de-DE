---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499546"
---
# <span data-ttu-id="6df85-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="6df85-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="6df85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6df85-102">SYNOPSIS</span></span>
<span data-ttu-id="6df85-103">Ruft das PSProjectTask-Objekt ab, das einem Azure Database Migration Service-Migrationsvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6df85-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6df85-104">SYNTAX</span></span>

### <span data-ttu-id="6df85-105">ListByComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="6df85-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="6df85-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6df85-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="6df85-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="6df85-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6df85-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="6df85-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="6df85-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df85-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="6df85-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6df85-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6df85-114">DESCRIPTION</span></span>
<span data-ttu-id="6df85-115">Das Get-AzureRmDataMigrationTask-Cmdlet ruft die Eigenschaften ab, die einem Azure Database Migration Service-Migrationsvorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6df85-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="6df85-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6df85-116">EXAMPLES</span></span>

### <span data-ttu-id="6df85-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6df85-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="6df85-118">Das obige Beispiel veranschaulicht die Verwendung von Get-AzureRmDataMigrationTask-Cmdlet zum Abrufen der Eigenschaften, die einem Azure Database Migration Service-Migrationsdienst basierend auf dem als Eingabeparameter übergebenen Aufgabennamen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6df85-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="6df85-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6df85-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="6df85-120">Das obige Beispiel veranschaulicht die Verwendung von Get-AzureRmDataMigrationTask-Cmdlet zum Abrufen aller Migrationsaufgaben, die mit dem als Eingabeparameter übergebenen PSProject-Objekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6df85-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="6df85-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="6df85-121">PARAMETERS</span></span>

### <span data-ttu-id="6df85-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df85-122">-DefaultProfile</span></span>
<span data-ttu-id="6df85-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6df85-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6df85-124">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="6df85-124">-Expand</span></span>
<span data-ttu-id="6df85-125">Ausgabe erweitern</span><span class="sxs-lookup"><span data-stu-id="6df85-125">Expand output</span></span>

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

### <span data-ttu-id="6df85-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6df85-126">-InputObject</span></span>
<span data-ttu-id="6df85-127">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6df85-127">PSProject Object.</span></span>

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

### <span data-ttu-id="6df85-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6df85-128">-Name</span></span>
<span data-ttu-id="6df85-129">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6df85-129">The name of the task.</span></span>

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

### <span data-ttu-id="6df85-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="6df85-130">-ProjectName</span></span>
<span data-ttu-id="6df85-131">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="6df85-131">The name of the project.</span></span>

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

### <span data-ttu-id="6df85-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df85-132">-ResourceGroupName</span></span>
<span data-ttu-id="6df85-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6df85-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="6df85-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6df85-134">-ResourceId</span></span>
<span data-ttu-id="6df85-135">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6df85-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="6df85-136">-Ergebnistyp</span><span class="sxs-lookup"><span data-stu-id="6df85-136">-ResultType</span></span>
<span data-ttu-id="6df85-137">Ausgabe des angegebenen Ergebnistyps erweitern</span><span class="sxs-lookup"><span data-stu-id="6df85-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df85-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6df85-138">-ServiceName</span></span>
<span data-ttu-id="6df85-139">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="6df85-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="6df85-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="6df85-140">-TaskType</span></span>
<span data-ttu-id="6df85-141">Nach TaskType Filtern</span><span class="sxs-lookup"><span data-stu-id="6df85-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df85-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df85-142">CommonParameters</span></span>
<span data-ttu-id="6df85-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df85-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df85-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df85-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df85-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6df85-145">INPUTS</span></span>

### <span data-ttu-id="6df85-146">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="6df85-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="6df85-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6df85-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6df85-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6df85-148">System.String</span></span>

## <span data-ttu-id="6df85-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6df85-149">OUTPUTS</span></span>

### <span data-ttu-id="6df85-150">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="6df85-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="6df85-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="6df85-151">NOTES</span></span>

## <span data-ttu-id="6df85-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6df85-152">RELATED LINKS</span></span>
