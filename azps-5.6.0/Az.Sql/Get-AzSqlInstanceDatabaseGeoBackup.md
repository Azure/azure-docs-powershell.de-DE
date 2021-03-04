---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943385"
---
# <span data-ttu-id="8e851-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8e851-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="8e851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e851-102">SYNOPSIS</span></span>
<span data-ttu-id="8e851-103">Gibt Informationen zur redundanten SQL von Azure SQL verwaltete Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="8e851-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="8e851-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e851-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e851-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e851-105">DESCRIPTION</span></span>
<span data-ttu-id="8e851-106">Das **Get-AzSqlInstanceDatabaseGeoBackup-Cmdlet** ruft mindestens eine Azure SQL-Datenbank redundante Sicherungen aus einer verwalteten Azure SQL-Datenbankinstanz ab.</span><span class="sxs-lookup"><span data-stu-id="8e851-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="8e851-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e851-107">EXAMPLES</span></span>

### <span data-ttu-id="8e851-108">Beispiel 1: Alle redundanten Datenbanksicherungen für eine Instanz erhalten</span><span class="sxs-lookup"><span data-stu-id="8e851-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="8e851-109">Dieser Befehl ruft alle datenbank redundanten Sicherungen für die Instanz mit dem Namen "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="8e851-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="8e851-110">Beispiel 2: Erhalten einer redundanten Datenbanksicherung nach Name für eine verwaltete Instanz</span><span class="sxs-lookup"><span data-stu-id="8e851-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="8e851-111">Dieser Befehl ruft eine datenbank redundante Sicherung mit dem Namen "managedDatabase1" aus einer Instanz mit dem Namen "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="8e851-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="8e851-112">Beispiel 3: Erhalten aller redundanten Datenbanksicherungen für eine Instanz mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="8e851-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="8e851-113">Dieser Befehl ruft alle datenbank redundanten Sicherungen für die Instanz mit dem Namen "managedInstance1" ab, die mit "managedDatabase" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8e851-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="8e851-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e851-114">PARAMETERS</span></span>

### <span data-ttu-id="8e851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e851-115">-DefaultProfile</span></span>
<span data-ttu-id="8e851-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e851-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e851-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8e851-117">-InstanceName</span></span>
<span data-ttu-id="8e851-118">Der Name der -Instanz.</span><span class="sxs-lookup"><span data-stu-id="8e851-118">The name of the instance.</span></span>

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

### <span data-ttu-id="8e851-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e851-119">-Name</span></span>
<span data-ttu-id="8e851-120">Der Name der abzurufende Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8e851-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="8e851-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e851-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e851-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e851-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e851-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e851-123">CommonParameters</span></span>
<span data-ttu-id="8e851-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e851-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e851-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e851-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e851-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e851-126">INPUTS</span></span>

### <span data-ttu-id="8e851-127">Keine</span><span class="sxs-lookup"><span data-stu-id="8e851-127">None</span></span>

## <span data-ttu-id="8e851-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e851-128">OUTPUTS</span></span>

### <span data-ttu-id="8e851-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8e851-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="8e851-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e851-130">NOTES</span></span>

## <span data-ttu-id="8e851-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e851-131">RELATED LINKS</span></span>
