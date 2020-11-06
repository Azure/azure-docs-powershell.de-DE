---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504437"
---
# <span data-ttu-id="7f88e-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7f88e-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="7f88e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f88e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f88e-103">Entfernt eine Azure Database Migration Service-Aufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="7f88e-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f88e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f88e-104">SYNTAX</span></span>

### <span data-ttu-id="7f88e-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f88e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f88e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f88e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f88e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f88e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f88e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f88e-108">DESCRIPTION</span></span>
<span data-ttu-id="7f88e-109">Das Remove-AzureRmDataMigrationTask-Cmdlet entfernt eine Azure-Datenbank-Migrationsdienst Aufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="7f88e-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="7f88e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f88e-110">EXAMPLES</span></span>

### <span data-ttu-id="7f88e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f88e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="7f88e-112">Im vorherigen Beispiel wird eine Azure Database Migration Service-Aufgabe namens Workflow aus Azure basierend auf dem Task Name-Parameter entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f88e-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="7f88e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f88e-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="7f88e-114">Im vorhergehenden Beispiel wird ein Azure Database Migration Service-Vorgang basierend auf dem übergebenen PSProjectTask-Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f88e-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="7f88e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f88e-115">PARAMETERS</span></span>

### <span data-ttu-id="7f88e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f88e-116">-DefaultProfile</span></span>
<span data-ttu-id="7f88e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f88e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f88e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7f88e-118">-Force</span></span>
<span data-ttu-id="7f88e-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="7f88e-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7f88e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f88e-120">-InputObject</span></span>
<span data-ttu-id="7f88e-121">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f88e-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f88e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7f88e-122">-Name</span></span>
<span data-ttu-id="7f88e-123">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7f88e-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f88e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f88e-124">-PassThru</span></span>
<span data-ttu-id="7f88e-125">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="7f88e-125">Returns an true/false.</span></span>
<span data-ttu-id="7f88e-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7f88e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f88e-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="7f88e-127">-ProjectName</span></span>
<span data-ttu-id="7f88e-128">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7f88e-128">The name of the project.</span></span>

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

### <span data-ttu-id="7f88e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f88e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7f88e-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7f88e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f88e-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f88e-131">-ResourceId</span></span>
<span data-ttu-id="7f88e-132">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7f88e-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="7f88e-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f88e-133">-ServiceName</span></span>
<span data-ttu-id="7f88e-134">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="7f88e-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="7f88e-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f88e-135">-Confirm</span></span>
<span data-ttu-id="7f88e-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f88e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f88e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f88e-137">-WhatIf</span></span>
<span data-ttu-id="7f88e-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f88e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f88e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f88e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f88e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f88e-140">CommonParameters</span></span>
<span data-ttu-id="7f88e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f88e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f88e-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f88e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f88e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f88e-143">INPUTS</span></span>

### <span data-ttu-id="7f88e-144">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7f88e-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="7f88e-145">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f88e-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7f88e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7f88e-146">System.String</span></span>

## <span data-ttu-id="7f88e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f88e-147">OUTPUTS</span></span>

### <span data-ttu-id="7f88e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f88e-148">System.Boolean</span></span>

## <span data-ttu-id="7f88e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f88e-149">NOTES</span></span>

## <span data-ttu-id="7f88e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f88e-150">RELATED LINKS</span></span>
