---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497254"
---
# <span data-ttu-id="870f1-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="870f1-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="870f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="870f1-102">SYNOPSIS</span></span>
<span data-ttu-id="870f1-103">Erstellt eine Azure SQL-Datenbank mit verwalteten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="870f1-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="870f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="870f1-104">SYNTAX</span></span>

### <span data-ttu-id="870f1-105">CreateNewInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="870f1-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870f1-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="870f1-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870f1-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="870f1-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="870f1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="870f1-108">DESCRIPTION</span></span>
<span data-ttu-id="870f1-109">Das Cmdlet **New-AzureRmSqlInstanceDatabase** erstellt eine Azure SQL-Instanzdatenbank mit verwalteten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="870f1-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="870f1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="870f1-110">EXAMPLES</span></span>

### <span data-ttu-id="870f1-111">Beispiel 1: Erstellen einer Datenbank für eine angegebene Instanz</span><span class="sxs-lookup"><span data-stu-id="870f1-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
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

<span data-ttu-id="870f1-112">Dieser Befehl erstellt eine Instanzdatenbank mit dem Namen Database01 auf Instanz managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="870f1-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="870f1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="870f1-113">PARAMETERS</span></span>

### <span data-ttu-id="870f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="870f1-114">-AsJob</span></span>
<span data-ttu-id="870f1-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="870f1-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-116">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="870f1-116">-Collation</span></span>
<span data-ttu-id="870f1-117">Die Sortierung der zu verwendenden Azure SQL-Instanzendaten Bank Sortierung.</span><span class="sxs-lookup"><span data-stu-id="870f1-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870f1-118">-DefaultProfile</span></span>
<span data-ttu-id="870f1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="870f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="870f1-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="870f1-120">-InstanceName</span></span>
<span data-ttu-id="870f1-121">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="870f1-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="870f1-122">-InstanceObject</span></span>
<span data-ttu-id="870f1-123">Das Instance-Objekt</span><span class="sxs-lookup"><span data-stu-id="870f1-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="870f1-124">-InstanceResourceId</span></span>
<span data-ttu-id="870f1-125">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="870f1-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="870f1-126">-Name</span></span>
<span data-ttu-id="870f1-127">Der Name der zu erstellende Azure SQL-Instanzen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="870f1-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="870f1-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="870f1-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="870f1-130">-Tag</span></span>
<span data-ttu-id="870f1-131">Die Tags, die der Azure SQL-Instanzen Datenbank zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="870f1-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="870f1-132">-Confirm</span></span>
<span data-ttu-id="870f1-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="870f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870f1-134">-WhatIf</span></span>
<span data-ttu-id="870f1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="870f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="870f1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="870f1-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870f1-137">CommonParameters</span></span>
<span data-ttu-id="870f1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870f1-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870f1-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="870f1-140">INPUTS</span></span>

### <span data-ttu-id="870f1-141">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="870f1-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="870f1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="870f1-142">System.String</span></span>

## <span data-ttu-id="870f1-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="870f1-143">OUTPUTS</span></span>

### <span data-ttu-id="870f1-144">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="870f1-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="870f1-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="870f1-145">NOTES</span></span>

## <span data-ttu-id="870f1-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="870f1-146">RELATED LINKS</span></span>
