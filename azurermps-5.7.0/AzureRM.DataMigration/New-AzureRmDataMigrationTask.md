---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662855"
---
# <span data-ttu-id="27d99-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="27d99-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="27d99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27d99-102">SYNOPSIS</span></span>
<span data-ttu-id="27d99-103">Erstellt und startet einen Daten Migrationstask im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="27d99-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d99-104">SYNTAX</span></span>

### <span data-ttu-id="27d99-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="27d99-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27d99-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27d99-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27d99-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27d99-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="27d99-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27d99-108">DESCRIPTION</span></span>
<span data-ttu-id="27d99-109">Das New-AzureRmDataMigrationTask-Cmdlet erstellt datenmigrationsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="27d99-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="27d99-110">Dieses Cmdlet übernimmt Parameter für den Aufgabentyp Enumerator, die Azure-Ressourcengruppe, den Namen des zugeordneten Azure Data Migration Service und Project als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="27d99-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="27d99-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27d99-111">EXAMPLES</span></span>

### <span data-ttu-id="27d99-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27d99-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="27d99-113">Dieses Beispielskript zeigt, wie Sie einen neuen Daten Migrations Task mit dem Namen MyMigrationTask im Projekt mit dem Namen myDMSProject und dem Dienst mit dem Namen Test Service erstellen.</span><span class="sxs-lookup"><span data-stu-id="27d99-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="27d99-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="27d99-114">PARAMETERS</span></span>

### <span data-ttu-id="27d99-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27d99-115">-Confirm</span></span>
<span data-ttu-id="27d99-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27d99-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d99-117">-DefaultProfile</span></span>
<span data-ttu-id="27d99-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27d99-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27d99-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="27d99-119">-InputObject</span></span>
<span data-ttu-id="27d99-120">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="27d99-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27d99-121">-Name</span></span>
<span data-ttu-id="27d99-122">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="27d99-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="27d99-123">-ProjectName</span></span>
<span data-ttu-id="27d99-124">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="27d99-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d99-125">-ResourceGroupName</span></span>
<span data-ttu-id="27d99-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27d99-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="27d99-127">-ResourceId</span></span>
<span data-ttu-id="27d99-128">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="27d99-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="27d99-129">-ServiceName</span></span>
<span data-ttu-id="27d99-130">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="27d99-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="27d99-131">-TaskType</span></span>
<span data-ttu-id="27d99-132">Aufgabentyp</span><span class="sxs-lookup"><span data-stu-id="27d99-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d99-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d99-133">-WhatIf</span></span>
<span data-ttu-id="27d99-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27d99-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d99-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27d99-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="27d99-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27d99-136">INPUTS</span></span>

### <span data-ttu-id="27d99-137">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="27d99-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="27d99-138">System. String</span><span class="sxs-lookup"><span data-stu-id="27d99-138">System.String</span></span>


## <span data-ttu-id="27d99-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27d99-139">OUTPUTS</span></span>

### <span data-ttu-id="27d99-140">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="27d99-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="27d99-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="27d99-141">NOTES</span></span>

## <span data-ttu-id="27d99-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27d99-142">RELATED LINKS</span></span>


