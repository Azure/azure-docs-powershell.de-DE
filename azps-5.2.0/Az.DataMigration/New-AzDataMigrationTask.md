---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357663"
---
# <span data-ttu-id="44ce6-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="44ce6-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="44ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="44ce6-103">Erstellt und startet eine Datenmigrationsaufgabe im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="44ce6-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="44ce6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44ce6-104">SYNTAX</span></span>

### <span data-ttu-id="44ce6-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44ce6-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44ce6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44ce6-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ce6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44ce6-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ce6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44ce6-108">DESCRIPTION</span></span>
<span data-ttu-id="44ce6-109">Das New-AzDataMigrationTask erstellt eine Datenmigrationsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="44ce6-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="44ce6-110">Dieses Cmdlet übernimmt Parameter für den Vorgangstypenumerator, die Azure-Ressourcengruppe, den Namen des zugeordneten Azure-Datenbankmigrationsdiensts und Project als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="44ce6-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="44ce6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44ce6-111">EXAMPLES</span></span>

### <span data-ttu-id="44ce6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44ce6-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="44ce6-113">Dieses Beispielskript zeigt, wie Sie eine neue Datenmigrationsaufgabe namens "MyMigrationTask" im Projekt mit dem Namen "myDMSProject" und dem Dienst "TestService" erstellen.</span><span class="sxs-lookup"><span data-stu-id="44ce6-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="44ce6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44ce6-114">PARAMETERS</span></span>

### <span data-ttu-id="44ce6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ce6-115">-DefaultProfile</span></span>
<span data-ttu-id="44ce6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44ce6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44ce6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ce6-117">-InputObject</span></span>
<span data-ttu-id="44ce6-118">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="44ce6-118">PSProject Object.</span></span>

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

### <span data-ttu-id="44ce6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44ce6-119">-Name</span></span>
<span data-ttu-id="44ce6-120">Der Name des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="44ce6-120">The name of the task.</span></span>

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

### <span data-ttu-id="44ce6-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="44ce6-121">-ProjectName</span></span>
<span data-ttu-id="44ce6-122">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="44ce6-122">The name of the project.</span></span>

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

### <span data-ttu-id="44ce6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ce6-123">-ResourceGroupName</span></span>
<span data-ttu-id="44ce6-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="44ce6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="44ce6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44ce6-125">-ResourceId</span></span>
<span data-ttu-id="44ce6-126">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="44ce6-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="44ce6-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="44ce6-127">-ServiceName</span></span>
<span data-ttu-id="44ce6-128">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="44ce6-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="44ce6-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="44ce6-129">-TaskType</span></span>
<span data-ttu-id="44ce6-130">Vorgangsart.</span><span class="sxs-lookup"><span data-stu-id="44ce6-130">Task Type.</span></span>

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

### <span data-ttu-id="44ce6-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="44ce6-131">-MigrationValidation</span></span> 
<span data-ttu-id="44ce6-132">Aufgabenantwortobjekt nach Überprüfungsaufruf, optional, aber empfohlen.</span><span class="sxs-lookup"><span data-stu-id="44ce6-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="44ce6-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="44ce6-133">-Wait</span></span>
<span data-ttu-id="44ce6-134">Gibt an, ob auf den Abschluss eines Vorgangs gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44ce6-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="44ce6-135">Wenn das Kennzeichen festgelegt ist, überprüft die Überprüfung alle ein Sekunden, bis die Aufgabe abgeschlossen ist, und kehren Sie zu den Aufgabeneigenschaften zurück, in denen die Ausgabe oder der Fehler überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="44ce6-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="44ce6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44ce6-136">-Confirm</span></span>
<span data-ttu-id="44ce6-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44ce6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ce6-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="44ce6-138">-WhatIf</span></span>
<span data-ttu-id="44ce6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44ce6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ce6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44ce6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ce6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ce6-141">CommonParameters</span></span>
<span data-ttu-id="44ce6-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ce6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ce6-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ce6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ce6-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44ce6-144">INPUTS</span></span>

### <span data-ttu-id="44ce6-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="44ce6-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="44ce6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="44ce6-146">System.String</span></span>

## <span data-ttu-id="44ce6-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44ce6-147">OUTPUTS</span></span>

### <span data-ttu-id="44ce6-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="44ce6-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="44ce6-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44ce6-149">NOTES</span></span>

## <span data-ttu-id="44ce6-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44ce6-150">RELATED LINKS</span></span>
