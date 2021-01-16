---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296183"
---
# <span data-ttu-id="6a798-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a798-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="6a798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a798-102">SYNOPSIS</span></span>
<span data-ttu-id="6a798-103">Erstellt eine Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="6a798-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6a798-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a798-104">SYNTAX</span></span>

### <span data-ttu-id="6a798-105">CreateNewInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a798-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a798-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6a798-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a798-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6a798-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a798-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a798-108">DESCRIPTION</span></span>
<span data-ttu-id="6a798-109">Das **Cmdlet "New-AzSqlInstanceDatabase"** erstellt eine Azure SQL Verwaltete Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="6a798-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="6a798-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a798-110">EXAMPLES</span></span>

### <span data-ttu-id="6a798-111">Beispiel 1: Erstellen einer Datenbank für eine bestimmte Instanz</span><span class="sxs-lookup"><span data-stu-id="6a798-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="6a798-112">Mit diesem Befehl wird eine Instanzdatenbank namens "Database01" für "managedInstance1" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a798-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="6a798-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a798-113">PARAMETERS</span></span>

### <span data-ttu-id="6a798-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a798-114">-AsJob</span></span>
<span data-ttu-id="6a798-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6a798-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="6a798-116">-Collation</span></span>
<span data-ttu-id="6a798-117">Die Sortierung der Azure SQL Zu verwendende Instanzdatenbanksortierung.</span><span class="sxs-lookup"><span data-stu-id="6a798-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a798-118">-DefaultProfile</span></span>
<span data-ttu-id="6a798-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a798-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a798-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6a798-120">-InstanceName</span></span>
<span data-ttu-id="6a798-121">Der Instanzname.</span><span class="sxs-lookup"><span data-stu-id="6a798-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="6a798-122">-InstanceObject</span></span>
<span data-ttu-id="6a798-123">Das Instanzobjekt</span><span class="sxs-lookup"><span data-stu-id="6a798-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6a798-124">-InstanceResourceId</span></span>
<span data-ttu-id="6a798-125">Die Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6a798-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6a798-126">-Name</span></span>
<span data-ttu-id="6a798-127">Der Name der Azure SQL Instanzdatenbank, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a798-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a798-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a798-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a798-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a798-130">-Tag</span></span>
<span data-ttu-id="6a798-131">Die Tags, die der Azure Sql-Instanzdatenbank zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="6a798-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a798-132">-Confirm</span></span>
<span data-ttu-id="6a798-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a798-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a798-134">-WhatIf</span></span>
<span data-ttu-id="6a798-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a798-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a798-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a798-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a798-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a798-137">CommonParameters</span></span>
<span data-ttu-id="6a798-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a798-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a798-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a798-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a798-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a798-140">INPUTS</span></span>

### <span data-ttu-id="6a798-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6a798-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="6a798-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6a798-142">System.String</span></span>

## <span data-ttu-id="6a798-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a798-143">OUTPUTS</span></span>

### <span data-ttu-id="6a798-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6a798-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6a798-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a798-145">NOTES</span></span>

## <span data-ttu-id="6a798-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a798-146">RELATED LINKS</span></span>
