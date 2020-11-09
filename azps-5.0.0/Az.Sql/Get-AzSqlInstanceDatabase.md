---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296637"
---
# <span data-ttu-id="338f5-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="338f5-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="338f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="338f5-102">SYNOPSIS</span></span>
<span data-ttu-id="338f5-103">Gibt Informationen zur Datenbank der Azure SQL-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="338f5-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="338f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="338f5-104">SYNTAX</span></span>

### <span data-ttu-id="338f5-105">GetInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="338f5-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="338f5-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="338f5-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="338f5-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="338f5-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="338f5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="338f5-108">DESCRIPTION</span></span>
<span data-ttu-id="338f5-109">Das Cmdlet " **Get-AzSqlInstanceDatabase** " Ruft eine oder mehrere Azure SQL-Datenbanken aus einer Azure SQL-Datenbank mit verwalteten Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="338f5-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="338f5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="338f5-110">EXAMPLES</span></span>

### <span data-ttu-id="338f5-111">Beispiel 1: Abrufen aller Datenbanken in einer Instanz</span><span class="sxs-lookup"><span data-stu-id="338f5-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="338f5-112">Dieser Befehl ruft alle Datenbanken auf der Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="338f5-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="338f5-113">Beispiel 2: Abrufen einer Datenbank nach Namen in einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="338f5-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="338f5-114">Dieser Befehl ruft eine Datenbank mit dem Namen managedDatabase1 aus einer Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="338f5-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="338f5-115">Beispiel 3: Abrufen aller Datenbanken in einer Instanz mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="338f5-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="338f5-116">Dieser Befehl ruft alle Datenbanken auf der Instanz mit dem Namen managedInstance1 ab, die mit "managedDatabase" beginnen.</span><span class="sxs-lookup"><span data-stu-id="338f5-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="338f5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="338f5-117">PARAMETERS</span></span>

### <span data-ttu-id="338f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338f5-118">-DefaultProfile</span></span>
<span data-ttu-id="338f5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="338f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338f5-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="338f5-120">-InstanceName</span></span>
<span data-ttu-id="338f5-121">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="338f5-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338f5-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="338f5-122">-InstanceObject</span></span>
<span data-ttu-id="338f5-123">Das Instanzen Objekt, das zum Abrufen der Instanzdatenbank verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="338f5-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="338f5-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="338f5-124">-InstanceResourceId</span></span>
<span data-ttu-id="338f5-125">Die Ressourcen-ID des abzurufenden Instanzen Objekts.</span><span class="sxs-lookup"><span data-stu-id="338f5-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="338f5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="338f5-126">-Name</span></span>
<span data-ttu-id="338f5-127">Der Name der Azure SQL-Instanzen Datenbank, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="338f5-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="338f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="338f5-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="338f5-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338f5-130">CommonParameters</span></span>
<span data-ttu-id="338f5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338f5-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="338f5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338f5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="338f5-133">INPUTS</span></span>

### <span data-ttu-id="338f5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="338f5-134">System.String</span></span>

### <span data-ttu-id="338f5-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="338f5-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="338f5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="338f5-136">OUTPUTS</span></span>

### <span data-ttu-id="338f5-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="338f5-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="338f5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="338f5-138">NOTES</span></span>

## <span data-ttu-id="338f5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="338f5-139">RELATED LINKS</span></span>
