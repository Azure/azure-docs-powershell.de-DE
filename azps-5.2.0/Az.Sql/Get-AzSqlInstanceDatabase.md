---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299883"
---
# <span data-ttu-id="f7961-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f7961-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="f7961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7961-102">SYNOPSIS</span></span>
<span data-ttu-id="f7961-103">Gibt Informationen zur Azure SQL Verwaltete Instanzdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f7961-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="f7961-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7961-104">SYNTAX</span></span>

### <span data-ttu-id="f7961-105">GetInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7961-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7961-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f7961-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7961-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="f7961-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7961-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7961-108">DESCRIPTION</span></span>
<span data-ttu-id="f7961-109">Das **Cmdlet "Get-AzSqlInstanceDatabase"** ruft mindestens eine Azure SQL-Datenbank aus einer verwalteten Azure SQL-Datenbankinstanz ab.</span><span class="sxs-lookup"><span data-stu-id="f7961-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f7961-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7961-110">EXAMPLES</span></span>

### <span data-ttu-id="f7961-111">Beispiel 1: Alle Datenbanken für eine Instanz erhalten</span><span class="sxs-lookup"><span data-stu-id="f7961-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="f7961-112">Dieser Befehl ruft alle Datenbanken für die Instanz mit dem Namen "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="f7961-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="f7961-113">Beispiel 2: Erhalten einer Datenbank nach Name für eine verwaltete Instanz</span><span class="sxs-lookup"><span data-stu-id="f7961-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="f7961-114">Dieser Befehl ruft eine Datenbank namens "managedDatabase1" aus einer Instanz namens "managedInstance1" ab.</span><span class="sxs-lookup"><span data-stu-id="f7961-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="f7961-115">Beispiel 3: Erhalten aller Datenbanken für eine Instanz mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="f7961-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="f7961-116">Dieser Befehl ruft alle Datenbanken für die Instanz mit dem Namen "managedInstance1" ab, die mit "managedDatabase" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7961-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="f7961-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7961-117">PARAMETERS</span></span>

### <span data-ttu-id="f7961-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7961-118">-DefaultProfile</span></span>
<span data-ttu-id="f7961-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7961-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7961-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f7961-120">-InstanceName</span></span>
<span data-ttu-id="f7961-121">Der Instanzname.</span><span class="sxs-lookup"><span data-stu-id="f7961-121">The instance name.</span></span>

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

### <span data-ttu-id="f7961-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="f7961-122">-InstanceObject</span></span>
<span data-ttu-id="f7961-123">Das Instanzobjekt, das zum Abrufen einer Instanzdatenbank verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f7961-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="f7961-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="f7961-124">-InstanceResourceId</span></span>
<span data-ttu-id="f7961-125">Die Ressourcen-ID des zu erhaltende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="f7961-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="f7961-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f7961-126">-Name</span></span>
<span data-ttu-id="f7961-127">Der Name der Azure SQL-Instanzdatenbank, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7961-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="f7961-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7961-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7961-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7961-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7961-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7961-130">CommonParameters</span></span>
<span data-ttu-id="f7961-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7961-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7961-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7961-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7961-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7961-133">INPUTS</span></span>

### <span data-ttu-id="f7961-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f7961-134">System.String</span></span>

### <span data-ttu-id="f7961-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f7961-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="f7961-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7961-136">OUTPUTS</span></span>

### <span data-ttu-id="f7961-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f7961-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="f7961-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7961-138">NOTES</span></span>

## <span data-ttu-id="f7961-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7961-139">RELATED LINKS</span></span>
