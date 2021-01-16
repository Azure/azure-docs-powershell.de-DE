---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371551"
---
# <span data-ttu-id="6a6f0-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="6a6f0-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="6a6f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6f0-103">Ruft eine gelöschte Datenbank ab, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="6a6f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a6f0-104">SYNTAX</span></span>

### <span data-ttu-id="6a6f0-105">DeletedDatabaseList (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a6f0-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a6f0-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="6a6f0-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a6f0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a6f0-107">DESCRIPTION</span></span>
<span data-ttu-id="6a6f0-108">Das **Cmdlet "Get-AzSqlDeletedInstanceDatabaseBackup"** ruft eine angegebene gelöschte SQL Instanz-Datenbanksicherung ab, die Sie wiederherstellen können, oder alle gelöschten Sicherungen, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="6a6f0-109">Dieses Cmdlet wird auch vom Instance SQL-Stretch-Datenbankdienst in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6a6f0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a6f0-110">EXAMPLES</span></span>

### <span data-ttu-id="6a6f0-111">Beispiel 1: Alle gelöschten Datenbanksicherungen auf einem Server erhalten</span><span class="sxs-lookup"><span data-stu-id="6a6f0-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="6a6f0-112">Dieser Befehl ruft alle gelöschten Datenbanksicherungen auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="6a6f0-113">Beispiel 2: Erhalten einer angegebenen gelöschten Datenbanksicherung</span><span class="sxs-lookup"><span data-stu-id="6a6f0-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="6a6f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a6f0-114">PARAMETERS</span></span>

### <span data-ttu-id="6a6f0-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a6f0-115">-DatabaseName</span></span>
<span data-ttu-id="6a6f0-116">Der Name der Azure SQL-Instanzdatenbank, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6f0-117">-DefaultProfile</span></span>
<span data-ttu-id="6a6f0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6f0-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="6a6f0-119">-DeletionDate</span></span>
<span data-ttu-id="6a6f0-120">Das Löschdatum der Azure SQL-Instanzdatenbank zum Abrufen von Sicherungen mit Genauigkeit in Millisekunden (z. B. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="6a6f0-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6f0-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6a6f0-121">-InstanceName</span></span>
<span data-ttu-id="6a6f0-122">Der Name der Azure SQL verwalteten Instanz, in der sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a6f0-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6f0-125">CommonParameters</span></span>
<span data-ttu-id="6a6f0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6f0-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a6f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6f0-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a6f0-128">INPUTS</span></span>

### <span data-ttu-id="6a6f0-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6a6f0-129">None</span></span>

## <span data-ttu-id="6a6f0-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a6f0-130">OUTPUTS</span></span>

### <span data-ttu-id="6a6f0-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="6a6f0-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="6a6f0-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a6f0-132">NOTES</span></span>

## <span data-ttu-id="6a6f0-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a6f0-133">RELATED LINKS</span></span>
