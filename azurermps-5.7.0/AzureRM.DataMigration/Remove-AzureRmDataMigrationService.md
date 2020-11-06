---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499866"
---
# <span data-ttu-id="d1505-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d1505-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="d1505-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1505-102">SYNOPSIS</span></span>
<span data-ttu-id="d1505-103">Entfernt eine Instanz des Azure Database Migration Service aus Azure.</span><span class="sxs-lookup"><span data-stu-id="d1505-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1505-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1505-104">SYNTAX</span></span>

### <span data-ttu-id="d1505-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1505-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d1505-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1505-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d1505-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1505-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d1505-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1505-108">DESCRIPTION</span></span>
<span data-ttu-id="d1505-109">Das Remove-AzureRmDataMigrationService-Cmdlet entfernt eine Instanz des Azure Database Migration Service aus Azure.</span><span class="sxs-lookup"><span data-stu-id="d1505-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="d1505-110">Durch die Bereitstellung des DeleteRunningTask-Parameters werden alle Azure-Daten Bank Migrationsdienst Aufgaben entfernt, die dem zu entfernenden Dienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1505-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="d1505-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1505-111">EXAMPLES</span></span>

### <span data-ttu-id="d1505-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1505-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="d1505-113">Im obigen Beispiel wird eine Instanz des Azure Database Migration Service mit dem Namen Test Service entfernt, die in einer Azure-Ressourcengruppe mit dem Namen myresourcegroup enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d1505-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="d1505-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1505-114">PARAMETERS</span></span>

### <span data-ttu-id="d1505-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1505-115">-Confirm</span></span>
<span data-ttu-id="d1505-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1505-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1505-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1505-117">-DefaultProfile</span></span>
<span data-ttu-id="d1505-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1505-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1505-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="d1505-119">-DeleteRunningTask</span></span>
<span data-ttu-id="d1505-120">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d1505-120">Delete any running task</span></span>

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

### <span data-ttu-id="d1505-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d1505-121">-Force</span></span>
<span data-ttu-id="d1505-122">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="d1505-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d1505-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1505-123">-InputObject</span></span>
<span data-ttu-id="d1505-124">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1505-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1505-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d1505-125">-Name</span></span>
<span data-ttu-id="d1505-126">Der Name des Daten Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="d1505-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1505-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1505-127">-PassThru</span></span>
<span data-ttu-id="d1505-128">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="d1505-128">Returns an true/false.</span></span>
<span data-ttu-id="d1505-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d1505-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1505-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1505-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1505-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1505-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1505-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1505-132">-ResourceId</span></span>
<span data-ttu-id="d1505-133">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d1505-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="d1505-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1505-134">-WhatIf</span></span>
<span data-ttu-id="d1505-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1505-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1505-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1505-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="d1505-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1505-137">INPUTS</span></span>

### <span data-ttu-id="d1505-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d1505-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="d1505-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1505-139">System.String</span></span>


## <span data-ttu-id="d1505-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1505-140">OUTPUTS</span></span>

### <span data-ttu-id="d1505-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1505-141">System.Boolean</span></span>


## <span data-ttu-id="d1505-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1505-142">NOTES</span></span>

## <span data-ttu-id="d1505-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1505-143">RELATED LINKS</span></span>


