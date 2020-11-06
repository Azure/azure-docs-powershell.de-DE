---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502949"
---
# <span data-ttu-id="c4e59-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c4e59-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="c4e59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4e59-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e59-103">Erstellt und startet einen Daten Migrationstask im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="c4e59-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4e59-104">SYNTAX</span></span>

### <span data-ttu-id="c4e59-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4e59-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4e59-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e59-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e59-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e59-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4e59-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e59-109">Das New-AzureRmDataMigrationTask-Cmdlet erstellt datenmigrationsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="c4e59-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="c4e59-110">Dieses Cmdlet übernimmt Parameter für den Aufgabentyp Enumerator, die Azure-Ressourcengruppe, den Namen des zugeordneten Azure Database Migration Service und Project als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="c4e59-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="c4e59-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4e59-111">EXAMPLES</span></span>

### <span data-ttu-id="c4e59-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4e59-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="c4e59-113">Dieses Beispielskript zeigt, wie Sie einen neuen Daten Migrations Task mit dem Namen MyMigrationTask im Projekt mit dem Namen myDMSProject und dem Dienst mit dem Namen Test Service erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4e59-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="c4e59-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4e59-114">PARAMETERS</span></span>

### <span data-ttu-id="c4e59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e59-115">-DefaultProfile</span></span>
<span data-ttu-id="c4e59-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4e59-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e59-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4e59-117">-InputObject</span></span>
<span data-ttu-id="c4e59-118">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4e59-118">PSProject Object.</span></span>

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

### <span data-ttu-id="c4e59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4e59-119">-Name</span></span>
<span data-ttu-id="c4e59-120">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="c4e59-120">The name of the task.</span></span>

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

### <span data-ttu-id="c4e59-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c4e59-121">-ProjectName</span></span>
<span data-ttu-id="c4e59-122">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="c4e59-122">The name of the project.</span></span>

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

### <span data-ttu-id="c4e59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e59-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4e59-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4e59-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4e59-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c4e59-125">-ResourceId</span></span>
<span data-ttu-id="c4e59-126">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c4e59-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="c4e59-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4e59-127">-ServiceName</span></span>
<span data-ttu-id="c4e59-128">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="c4e59-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c4e59-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="c4e59-129">-TaskType</span></span>
<span data-ttu-id="c4e59-130">Aufgabentyp</span><span class="sxs-lookup"><span data-stu-id="c4e59-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e59-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4e59-131">-Confirm</span></span>
<span data-ttu-id="c4e59-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4e59-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e59-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e59-133">-WhatIf</span></span>
<span data-ttu-id="c4e59-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4e59-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e59-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4e59-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e59-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e59-136">CommonParameters</span></span>
<span data-ttu-id="c4e59-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e59-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e59-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e59-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e59-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4e59-139">INPUTS</span></span>

### <span data-ttu-id="c4e59-140">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="c4e59-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="c4e59-141">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4e59-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c4e59-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e59-142">System.String</span></span>

## <span data-ttu-id="c4e59-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4e59-143">OUTPUTS</span></span>

### <span data-ttu-id="c4e59-144">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c4e59-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="c4e59-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4e59-145">NOTES</span></span>

## <span data-ttu-id="c4e59-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4e59-146">RELATED LINKS</span></span>
