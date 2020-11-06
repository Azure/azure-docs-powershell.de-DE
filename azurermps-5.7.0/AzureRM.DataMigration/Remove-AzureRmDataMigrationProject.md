---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503766"
---
# <span data-ttu-id="75c9b-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="75c9b-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="75c9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="75c9b-103">Entfernt ein Azure Database Migration Service-Projekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="75c9b-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75c9b-104">SYNTAX</span></span>

### <span data-ttu-id="75c9b-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75c9b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="75c9b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c9b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="75c9b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c9b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="75c9b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75c9b-108">DESCRIPTION</span></span>
<span data-ttu-id="75c9b-109">Das Remove-AzureRmDataMigrationProject-Cmdlet entfernt ein Azure-Datenbank-Migrationsdienst Projekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="75c9b-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="75c9b-110">Durch die Bereitstellung des DeleteRunningTask-Parameters werden alle Azure-Datenbank-Migrationsdienst Aufgaben entfernt, die dem zu entfernenden Projekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="75c9b-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="75c9b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75c9b-111">EXAMPLES</span></span>

### <span data-ttu-id="75c9b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75c9b-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="75c9b-113">Im obigen Beispiel wird das Azure Database Migration Service-Projekt namens myDMProject aus Azure basierend auf Name als Eingabeparameter entfernt</span><span class="sxs-lookup"><span data-stu-id="75c9b-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="75c9b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="75c9b-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="75c9b-115">Im obigen Beispiel wird das Azure Database Migration Service-Projekt auf Grundlage des PSProject-Objekts als Eingabeparameter entfernt.</span><span class="sxs-lookup"><span data-stu-id="75c9b-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="75c9b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="75c9b-116">PARAMETERS</span></span>

### <span data-ttu-id="75c9b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75c9b-117">-Confirm</span></span>
<span data-ttu-id="75c9b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75c9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c9b-119">-DefaultProfile</span></span>
<span data-ttu-id="75c9b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75c9b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c9b-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="75c9b-121">-DeleteRunningTask</span></span>
<span data-ttu-id="75c9b-122">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="75c9b-122">Delete any running task</span></span>

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

### <span data-ttu-id="75c9b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="75c9b-123">-Force</span></span>
<span data-ttu-id="75c9b-124">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="75c9b-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="75c9b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75c9b-125">-InputObject</span></span>
<span data-ttu-id="75c9b-126">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="75c9b-126">PSProject Object.</span></span>

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

### <span data-ttu-id="75c9b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="75c9b-127">-Name</span></span>
<span data-ttu-id="75c9b-128">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="75c9b-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c9b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75c9b-129">-PassThru</span></span>
<span data-ttu-id="75c9b-130">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="75c9b-130">Returns an true/false.</span></span>
<span data-ttu-id="75c9b-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="75c9b-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75c9b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c9b-132">-ResourceGroupName</span></span>
<span data-ttu-id="75c9b-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75c9b-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="75c9b-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="75c9b-134">-ResourceId</span></span>
<span data-ttu-id="75c9b-135">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="75c9b-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="75c9b-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="75c9b-136">-ServiceName</span></span>
<span data-ttu-id="75c9b-137">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="75c9b-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="75c9b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c9b-138">-WhatIf</span></span>
<span data-ttu-id="75c9b-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75c9b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c9b-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75c9b-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="75c9b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75c9b-141">INPUTS</span></span>

### <span data-ttu-id="75c9b-142">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="75c9b-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="75c9b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="75c9b-143">System.String</span></span>


## <span data-ttu-id="75c9b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75c9b-144">OUTPUTS</span></span>

### <span data-ttu-id="75c9b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75c9b-145">System.Boolean</span></span>


## <span data-ttu-id="75c9b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="75c9b-146">NOTES</span></span>

## <span data-ttu-id="75c9b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75c9b-147">RELATED LINKS</span></span>

