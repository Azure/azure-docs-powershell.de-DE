---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938816"
---
# <span data-ttu-id="da051-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="da051-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="da051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da051-102">SYNOPSIS</span></span>
<span data-ttu-id="da051-103">Erstellt und startet eine Datenmigrationsaufgabe im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="da051-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="da051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da051-104">SYNTAX</span></span>

### <span data-ttu-id="da051-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="da051-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da051-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da051-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da051-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da051-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da051-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da051-108">DESCRIPTION</span></span>
<span data-ttu-id="da051-109">Das New-AzDataMigrationTask-Cmdlet erstellt eine Datenmigrationsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="da051-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="da051-110">Dieses Cmdlet übernimmt Parameter für Vorgangstypenumerator, Azure-Ressourcengruppe, Den Namen des zugeordneten Azure-Datenbankmigrationsdiensts und Project als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="da051-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="da051-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da051-111">EXAMPLES</span></span>

### <span data-ttu-id="da051-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da051-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="da051-113">Dieses Beispielskript zeigt, wie Sie eine neue Datenmigrationsaufgabe namens "MyMigrationTask" im Projekt mit dem Namen "myDMSProject" und dem Dienst "TestService" erstellen.</span><span class="sxs-lookup"><span data-stu-id="da051-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="da051-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="da051-114">PARAMETERS</span></span>

### <span data-ttu-id="da051-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da051-115">-DefaultProfile</span></span>
<span data-ttu-id="da051-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da051-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da051-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da051-117">-InputObject</span></span>
<span data-ttu-id="da051-118">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="da051-118">PSProject Object.</span></span>

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

### <span data-ttu-id="da051-119">-Name</span><span class="sxs-lookup"><span data-stu-id="da051-119">-Name</span></span>
<span data-ttu-id="da051-120">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="da051-120">The name of the task.</span></span>

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

### <span data-ttu-id="da051-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="da051-121">-ProjectName</span></span>
<span data-ttu-id="da051-122">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="da051-122">The name of the project.</span></span>

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

### <span data-ttu-id="da051-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da051-123">-ResourceGroupName</span></span>
<span data-ttu-id="da051-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da051-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="da051-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da051-125">-ResourceId</span></span>
<span data-ttu-id="da051-126">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="da051-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="da051-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da051-127">-ServiceName</span></span>
<span data-ttu-id="da051-128">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="da051-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="da051-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="da051-129">-TaskType</span></span>
<span data-ttu-id="da051-130">Vorgangstyp.</span><span class="sxs-lookup"><span data-stu-id="da051-130">Task Type.</span></span>

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

### <span data-ttu-id="da051-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="da051-131">-MigrationValidation</span></span> 
<span data-ttu-id="da051-132">Vorgangsantwortobjekt per Überprüfungsaufruf, optional, aber empfohlen.</span><span class="sxs-lookup"><span data-stu-id="da051-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="da051-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="da051-133">-Wait</span></span>
<span data-ttu-id="da051-134">Gibt an, ob sie warten soll, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="da051-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="da051-135">Wenn das Kennzeichen festgelegt ist, überprüft alle eine Sekunde, bis die Aufgabe abgeschlossen ist, und kehren Sie zum Benutzer zurück zu den Aufgabeneigenschaften, in denen die Ausgabe oder der Fehler überprüft werden können.</span><span class="sxs-lookup"><span data-stu-id="da051-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="da051-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da051-136">-Confirm</span></span>
<span data-ttu-id="da051-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da051-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da051-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da051-138">-WhatIf</span></span>
<span data-ttu-id="da051-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da051-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da051-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da051-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da051-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da051-141">CommonParameters</span></span>
<span data-ttu-id="da051-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da051-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da051-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da051-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da051-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da051-144">INPUTS</span></span>

### <span data-ttu-id="da051-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="da051-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="da051-146">System.String</span><span class="sxs-lookup"><span data-stu-id="da051-146">System.String</span></span>

## <span data-ttu-id="da051-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da051-147">OUTPUTS</span></span>

### <span data-ttu-id="da051-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="da051-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="da051-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="da051-149">NOTES</span></span>

## <span data-ttu-id="da051-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="da051-150">RELATED LINKS</span></span>
