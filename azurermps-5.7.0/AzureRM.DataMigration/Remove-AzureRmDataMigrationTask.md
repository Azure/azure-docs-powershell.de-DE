---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498966"
---
# <span data-ttu-id="1dc20-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="1dc20-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="1dc20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dc20-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc20-103">Entfernt eine Azure Database Migration Service-Aufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc20-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc20-104">SYNTAX</span></span>

### <span data-ttu-id="1dc20-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dc20-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dc20-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc20-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dc20-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc20-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1dc20-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dc20-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc20-109">Das Remove-AzureRmDataMigrationTask-Cmdlet entfernt eine Azure-Datenbank-Migrationsdienst Aufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc20-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="1dc20-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dc20-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc20-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dc20-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="1dc20-112">Im vorherigen Beispiel wird eine Azure Database Migration Service-Aufgabe namens Workflow aus Azure basierend auf dem Task Name-Parameter entfernt.</span><span class="sxs-lookup"><span data-stu-id="1dc20-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="1dc20-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1dc20-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="1dc20-114">Im vorhergehenden Beispiel wird ein Azure Database Migration Service-Vorgang basierend auf dem übergebenen PSProjectTask-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="1dc20-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="1dc20-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dc20-115">PARAMETERS</span></span>

### <span data-ttu-id="1dc20-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dc20-116">-Confirm</span></span>
<span data-ttu-id="1dc20-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dc20-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc20-118">-DefaultProfile</span></span>
<span data-ttu-id="1dc20-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1dc20-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc20-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc20-120">-Force</span></span>
<span data-ttu-id="1dc20-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="1dc20-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1dc20-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1dc20-122">-InputObject</span></span>
<span data-ttu-id="1dc20-123">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1dc20-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc20-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1dc20-124">-Name</span></span>
<span data-ttu-id="1dc20-125">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1dc20-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc20-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc20-126">-PassThru</span></span>
<span data-ttu-id="1dc20-127">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="1dc20-127">Returns an true/false.</span></span>
<span data-ttu-id="1dc20-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1dc20-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1dc20-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1dc20-129">-ProjectName</span></span>
<span data-ttu-id="1dc20-130">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="1dc20-130">The name of the project.</span></span>

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

### <span data-ttu-id="1dc20-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc20-131">-ResourceGroupName</span></span>
<span data-ttu-id="1dc20-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1dc20-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dc20-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1dc20-133">-ResourceId</span></span>
<span data-ttu-id="1dc20-134">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1dc20-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="1dc20-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1dc20-135">-ServiceName</span></span>
<span data-ttu-id="1dc20-136">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="1dc20-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="1dc20-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc20-137">-WhatIf</span></span>
<span data-ttu-id="1dc20-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dc20-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc20-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dc20-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1dc20-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dc20-140">INPUTS</span></span>

### <span data-ttu-id="1dc20-141">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="1dc20-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="1dc20-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc20-142">System.String</span></span>


## <span data-ttu-id="1dc20-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dc20-143">OUTPUTS</span></span>

### <span data-ttu-id="1dc20-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dc20-144">System.Boolean</span></span>


## <span data-ttu-id="1dc20-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dc20-145">NOTES</span></span>

## <span data-ttu-id="1dc20-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dc20-146">RELATED LINKS</span></span>


