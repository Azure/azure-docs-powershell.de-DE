---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377612"
---
# <span data-ttu-id="040d5-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="040d5-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="040d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="040d5-102">SYNOPSIS</span></span>
<span data-ttu-id="040d5-103">Entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="040d5-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="040d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="040d5-104">SYNTAX</span></span>

### <span data-ttu-id="040d5-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="040d5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040d5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="040d5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040d5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="040d5-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="040d5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="040d5-108">DESCRIPTION</span></span>
<span data-ttu-id="040d5-109">Das Remove-AzDataMigrationService cmdlet entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="040d5-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="040d5-110">Durch das Bereitstellen des Parameters "DeleteRunningTask" werden alle Azure Database Migration Service-Aufgaben entfernt, die dem Dienst zugeordnet sind, der entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="040d5-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="040d5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="040d5-111">EXAMPLES</span></span>

### <span data-ttu-id="040d5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="040d5-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="040d5-113">Im vorstehenden Beispiel wird eine Instanz des Azure-Datenbankmigrationsdiensts namens TestService entfernt, die in einer Azure-Ressourcengruppe namens "MyResourceGroup" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="040d5-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="040d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="040d5-114">PARAMETERS</span></span>

### <span data-ttu-id="040d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040d5-115">-DefaultProfile</span></span>
<span data-ttu-id="040d5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="040d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="040d5-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="040d5-117">-DeleteRunningTask</span></span>
<span data-ttu-id="040d5-118">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="040d5-118">Delete any running task</span></span>

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

### <span data-ttu-id="040d5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="040d5-119">-Force</span></span>
<span data-ttu-id="040d5-120">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="040d5-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="040d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="040d5-121">-InputObject</span></span>
<span data-ttu-id="040d5-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="040d5-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="040d5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="040d5-123">-Name</span></span>
<span data-ttu-id="040d5-124">Der Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="040d5-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040d5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="040d5-125">-PassThru</span></span>
<span data-ttu-id="040d5-126">Gibt "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="040d5-126">Returns an true/false.</span></span>
<span data-ttu-id="040d5-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="040d5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="040d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="040d5-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="040d5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="040d5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="040d5-130">-ResourceId</span></span>
<span data-ttu-id="040d5-131">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="040d5-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="040d5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="040d5-132">-Confirm</span></span>
<span data-ttu-id="040d5-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="040d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040d5-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="040d5-134">-WhatIf</span></span>
<span data-ttu-id="040d5-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="040d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040d5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="040d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040d5-137">CommonParameters</span></span>
<span data-ttu-id="040d5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="040d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040d5-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="040d5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040d5-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="040d5-140">INPUTS</span></span>

### <span data-ttu-id="040d5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="040d5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="040d5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="040d5-142">System.String</span></span>

## <span data-ttu-id="040d5-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="040d5-143">OUTPUTS</span></span>

### <span data-ttu-id="040d5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="040d5-144">System.Boolean</span></span>

## <span data-ttu-id="040d5-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="040d5-145">NOTES</span></span>

## <span data-ttu-id="040d5-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="040d5-146">RELATED LINKS</span></span>
