---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495618"
---
# <span data-ttu-id="c6bf5-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c6bf5-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="c6bf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="c6bf5-103">Gibt Informationen zur Datenbank der Azure SQL-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6bf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6bf5-104">SYNTAX</span></span>

### <span data-ttu-id="c6bf5-105">GetInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6bf5-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6bf5-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="c6bf5-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6bf5-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="c6bf5-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6bf5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6bf5-108">DESCRIPTION</span></span>
<span data-ttu-id="c6bf5-109">Das Cmdlet " **Get-AzureRmSqlInstanceDatabase** " Ruft eine oder mehrere Azure SQL-Datenbanken aus einer Azure SQL-Datenbank mit verwalteten Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c6bf5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6bf5-110">EXAMPLES</span></span>

### <span data-ttu-id="c6bf5-111">Beispiel 1: Abrufen aller Datenbanken in einer Instanz</span><span class="sxs-lookup"><span data-stu-id="c6bf5-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="c6bf5-112">Dieser Befehl ruft alle Datenbanken auf der Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="c6bf5-113">Beispiel 2: Abrufen einer Datenbank nach Namen in einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="c6bf5-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="c6bf5-114">Dieser Befehl ruft eine Datenbank mit dem Namen managedDatabase1 aus einer Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="c6bf5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6bf5-115">PARAMETERS</span></span>

### <span data-ttu-id="c6bf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bf5-116">-DefaultProfile</span></span>
<span data-ttu-id="c6bf5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6bf5-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c6bf5-118">-InstanceName</span></span>
<span data-ttu-id="c6bf5-119">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bf5-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="c6bf5-120">-InstanceObject</span></span>
<span data-ttu-id="c6bf5-121">Das Instanzen Objekt, das zum Abrufen der Instanzdatenbank verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="c6bf5-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6bf5-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c6bf5-122">-InstanceResourceId</span></span>
<span data-ttu-id="c6bf5-123">Die Ressourcen-ID des abzurufenden Instanzen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6bf5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c6bf5-124">-Name</span></span>
<span data-ttu-id="c6bf5-125">Der Name der Azure SQL-Instanzen Datenbank, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bf5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bf5-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6bf5-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bf5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bf5-128">CommonParameters</span></span>
<span data-ttu-id="c6bf5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6bf5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bf5-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6bf5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bf5-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6bf5-131">INPUTS</span></span>

### <span data-ttu-id="c6bf5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf5-132">System.String</span></span>
<span data-ttu-id="c6bf5-133">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c6bf5-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c6bf5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6bf5-134">OUTPUTS</span></span>

### <span data-ttu-id="c6bf5-135">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c6bf5-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c6bf5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6bf5-136">NOTES</span></span>

## <span data-ttu-id="c6bf5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6bf5-137">RELATED LINKS</span></span>
