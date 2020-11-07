---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: c40bd5761d7e0966e7d756a758f79bfb3592a2ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651461"
---
# <span data-ttu-id="bf656-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="bf656-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="bf656-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf656-102">SYNOPSIS</span></span>
<span data-ttu-id="bf656-103">Erstellt und startet einen Daten Migrationstask im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="bf656-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="bf656-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf656-104">SYNTAX</span></span>

### <span data-ttu-id="bf656-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf656-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf656-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf656-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf656-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf656-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf656-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf656-108">DESCRIPTION</span></span>
<span data-ttu-id="bf656-109">Das New-AzDataMigrationTask-Cmdlet erstellt datenmigrationsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf656-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="bf656-110">Dieses Cmdlet übernimmt Parameter für den Aufgabentyp Enumerator, die Azure-Ressourcengruppe, den Namen des zugeordneten Azure Database Migration Service und Project als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="bf656-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="bf656-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf656-111">EXAMPLES</span></span>

### <span data-ttu-id="bf656-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf656-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="bf656-113">Dieses Beispielskript zeigt, wie Sie einen neuen Daten Migrations Task mit dem Namen MyMigrationTask im Projekt mit dem Namen myDMSProject und dem Dienst mit dem Namen Test Service erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf656-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="bf656-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf656-114">PARAMETERS</span></span>

### <span data-ttu-id="bf656-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf656-115">-DefaultProfile</span></span>
<span data-ttu-id="bf656-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf656-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf656-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf656-117">-InputObject</span></span>
<span data-ttu-id="bf656-118">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bf656-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bf656-119">-Name</span></span>
<span data-ttu-id="bf656-120">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="bf656-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="bf656-121">-ProjectName</span></span>
<span data-ttu-id="bf656-122">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="bf656-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf656-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf656-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf656-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bf656-125">-ResourceId</span></span>
<span data-ttu-id="bf656-126">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bf656-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bf656-127">-ServiceName</span></span>
<span data-ttu-id="bf656-128">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="bf656-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="bf656-129">-TaskType</span></span>
<span data-ttu-id="bf656-130">Aufgabentyp</span><span class="sxs-lookup"><span data-stu-id="bf656-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="bf656-131">-MigrationValidation</span></span> 
<span data-ttu-id="bf656-132">Aufgaben Antwortobjekt durch Validierungs Aufruf, optional, aber empfohlen.</span><span class="sxs-lookup"><span data-stu-id="bf656-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf656-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="bf656-133">-Wait</span></span>
<span data-ttu-id="bf656-134">Gibt an, ob der Vorgang beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf656-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="bf656-135">Wenn das Flag gesetzt ist, überprüft alle Sekunden, bis die Aufgabe abgeschlossen ist, und kehren Sie zu den Aufgabeneigenschaften zurück, bei denen die Ausgabe oder der Fehler überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf656-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="bf656-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf656-136">-Confirm</span></span>
<span data-ttu-id="bf656-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf656-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf656-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf656-138">-WhatIf</span></span>
<span data-ttu-id="bf656-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf656-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf656-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf656-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf656-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf656-141">CommonParameters</span></span>
<span data-ttu-id="bf656-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf656-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf656-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf656-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf656-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf656-144">INPUTS</span></span>

### <span data-ttu-id="bf656-145">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="bf656-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="bf656-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bf656-146">System.String</span></span>

## <span data-ttu-id="bf656-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf656-147">OUTPUTS</span></span>

### <span data-ttu-id="bf656-148">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="bf656-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="bf656-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf656-149">NOTES</span></span>

## <span data-ttu-id="bf656-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf656-150">RELATED LINKS</span></span>
