---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307107"
---
# <span data-ttu-id="7d6cf-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="7d6cf-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="7d6cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6cf-103">Gibt Informationen zur redundanten Sicherung SQL Verwaltete Instanz von Azure zurück.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="7d6cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d6cf-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6cf-106">Das **Cmdlet "Get-AzSqlInstanceDatabaseGeoBackup"** ruft redundante Sicherungen von Azure SQL-Datenbanken aus einer verwalteten Azure SQL-Datenbankinstanz ab.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7d6cf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="7d6cf-108">Beispiel 1: Alle redundanten Datenbanksicherungen für eine Instanz erhalten</span><span class="sxs-lookup"><span data-stu-id="7d6cf-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="7d6cf-109">Dieser Befehl ruft alle redundanten Datenbanksicherungen für die Instanz namens "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="7d6cf-110">Beispiel 2: Erhalten einer redundanten Datenbanksicherung nach Name für eine verwaltete Instanz</span><span class="sxs-lookup"><span data-stu-id="7d6cf-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="7d6cf-111">Dieser Befehl ruft eine redundante Datenbanksicherung namens "managedDatabase1" aus einer Instanz namens "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="7d6cf-112">Beispiel 3: Erhalten aller redundanten Datenbanksicherungen für eine Instanz mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="7d6cf-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="7d6cf-113">Dieser Befehl ruft alle redundanten Datenbanksicherungen für die Instanz namens "managedInstance1" ab, die mit "managedDatabase" beginnen.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="7d6cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d6cf-114">PARAMETERS</span></span>

### <span data-ttu-id="7d6cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6cf-115">-DefaultProfile</span></span>
<span data-ttu-id="7d6cf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d6cf-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7d6cf-117">-InstanceName</span></span>
<span data-ttu-id="7d6cf-118">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-118">The name of the instance.</span></span>

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

### <span data-ttu-id="7d6cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7d6cf-119">-Name</span></span>
<span data-ttu-id="7d6cf-120">Der Name der abzurufende Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6cf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6cf-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d6cf-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6cf-123">CommonParameters</span></span>
<span data-ttu-id="7d6cf-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6cf-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d6cf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6cf-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d6cf-126">INPUTS</span></span>

### <span data-ttu-id="7d6cf-127">Keine</span><span class="sxs-lookup"><span data-stu-id="7d6cf-127">None</span></span>

## <span data-ttu-id="7d6cf-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d6cf-128">OUTPUTS</span></span>

### <span data-ttu-id="7d6cf-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7d6cf-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="7d6cf-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d6cf-130">NOTES</span></span>

## <span data-ttu-id="7d6cf-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d6cf-131">RELATED LINKS</span></span>
