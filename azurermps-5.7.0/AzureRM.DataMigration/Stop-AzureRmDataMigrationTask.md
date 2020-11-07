---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663069"
---
# <span data-ttu-id="55d8a-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="55d8a-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="55d8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="55d8a-103">Beendet eine Azure-Datenbank-Migrationsdienst Aufgabe, die sich in einem aktiven Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="55d8a-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d8a-104">SYNTAX</span></span>

### <span data-ttu-id="55d8a-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55d8a-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="55d8a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55d8a-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="55d8a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55d8a-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="55d8a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55d8a-108">DESCRIPTION</span></span>
<span data-ttu-id="55d8a-109">Stop-AzureRmDataMigrationTask-Cmdlet beendet die Daten Bank Migrations Aktivität im aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="55d8a-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="55d8a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55d8a-110">EXAMPLES</span></span>

### <span data-ttu-id="55d8a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55d8a-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="55d8a-112">Im obigen Beispiel wird die Azure-Daten Bank Migrationsdienst Aufgabe mit dem Namen "myDMSTask" beendet, die mit Project myDMSProject und Azure Database Migration Service Instance namens Test Service verbunden ist</span><span class="sxs-lookup"><span data-stu-id="55d8a-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="55d8a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55d8a-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="55d8a-114">Im obigen Beispiel wird die Azure-Daten Bank Migrationsdienst Aufgabe als Eingabeparameter PSProjectTask-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="55d8a-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="55d8a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="55d8a-115">PARAMETERS</span></span>

### <span data-ttu-id="55d8a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55d8a-116">-Confirm</span></span>
<span data-ttu-id="55d8a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55d8a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d8a-118">-DefaultProfile</span></span>
<span data-ttu-id="55d8a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55d8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d8a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55d8a-120">-InputObject</span></span>
<span data-ttu-id="55d8a-121">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="55d8a-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="55d8a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="55d8a-122">-Name</span></span>
<span data-ttu-id="55d8a-123">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="55d8a-123">The name of the task.</span></span>

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

### <span data-ttu-id="55d8a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55d8a-124">-PassThru</span></span>
<span data-ttu-id="55d8a-125">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="55d8a-125">Returns an true/false.</span></span>
<span data-ttu-id="55d8a-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="55d8a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55d8a-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="55d8a-127">-ProjectName</span></span>
<span data-ttu-id="55d8a-128">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="55d8a-128">The name of the project.</span></span>

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

### <span data-ttu-id="55d8a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d8a-129">-ResourceGroupName</span></span>
<span data-ttu-id="55d8a-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55d8a-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="55d8a-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55d8a-131">-ResourceId</span></span>
<span data-ttu-id="55d8a-132">ProjectTask-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="55d8a-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="55d8a-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="55d8a-133">-ServiceName</span></span>
<span data-ttu-id="55d8a-134">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="55d8a-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="55d8a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d8a-135">-WhatIf</span></span>
<span data-ttu-id="55d8a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55d8a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55d8a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55d8a-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="55d8a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55d8a-138">INPUTS</span></span>

### <span data-ttu-id="55d8a-139">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="55d8a-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="55d8a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="55d8a-140">System.String</span></span>


## <span data-ttu-id="55d8a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55d8a-141">OUTPUTS</span></span>

### <span data-ttu-id="55d8a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55d8a-142">System.Boolean</span></span>


## <span data-ttu-id="55d8a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="55d8a-143">NOTES</span></span>

## <span data-ttu-id="55d8a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55d8a-144">RELATED LINKS</span></span>

