---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941888"
---
# <span data-ttu-id="70a49-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="70a49-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="70a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70a49-102">SYNOPSIS</span></span>
<span data-ttu-id="70a49-103">Entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="70a49-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="70a49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70a49-104">SYNTAX</span></span>

### <span data-ttu-id="70a49-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="70a49-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a49-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70a49-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a49-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70a49-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70a49-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70a49-108">DESCRIPTION</span></span>
<span data-ttu-id="70a49-109">Das Remove-AzDataMigrationService-Cmdlet entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="70a49-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="70a49-110">Wenn Sie den Parameter DeleteRunningTask bereitstellen, werden alle Azure Database Migration Service-Aufgaben entfernt, die dem dienst zugeordnet sind, der entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="70a49-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="70a49-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70a49-111">EXAMPLES</span></span>

### <span data-ttu-id="70a49-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70a49-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="70a49-113">Im vorstehenden Beispiel wird eine Instanz des Azure-Datenbankmigrationsdiensts mit dem Namen TestService entfernt, die in einer Azure-Ressourcengruppe mit dem Namen MyResourceGroup enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="70a49-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="70a49-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="70a49-114">PARAMETERS</span></span>

### <span data-ttu-id="70a49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a49-115">-DefaultProfile</span></span>
<span data-ttu-id="70a49-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70a49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a49-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="70a49-117">-DeleteRunningTask</span></span>
<span data-ttu-id="70a49-118">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="70a49-118">Delete any running task</span></span>

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

### <span data-ttu-id="70a49-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="70a49-119">-Force</span></span>
<span data-ttu-id="70a49-120">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="70a49-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="70a49-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70a49-121">-InputObject</span></span>
<span data-ttu-id="70a49-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="70a49-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="70a49-123">-Name</span><span class="sxs-lookup"><span data-stu-id="70a49-123">-Name</span></span>
<span data-ttu-id="70a49-124">Der Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="70a49-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="70a49-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70a49-125">-PassThru</span></span>
<span data-ttu-id="70a49-126">Gibt den Wert "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="70a49-126">Returns an true/false.</span></span>
<span data-ttu-id="70a49-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="70a49-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70a49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a49-128">-ResourceGroupName</span></span>
<span data-ttu-id="70a49-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70a49-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="70a49-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70a49-130">-ResourceId</span></span>
<span data-ttu-id="70a49-131">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="70a49-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="70a49-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70a49-132">-Confirm</span></span>
<span data-ttu-id="70a49-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70a49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a49-134">-WhatIf</span></span>
<span data-ttu-id="70a49-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70a49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70a49-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70a49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a49-137">CommonParameters</span></span>
<span data-ttu-id="70a49-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a49-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a49-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a49-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70a49-140">INPUTS</span></span>

### <span data-ttu-id="70a49-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="70a49-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="70a49-142">System.String</span><span class="sxs-lookup"><span data-stu-id="70a49-142">System.String</span></span>

## <span data-ttu-id="70a49-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70a49-143">OUTPUTS</span></span>

### <span data-ttu-id="70a49-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70a49-144">System.Boolean</span></span>

## <span data-ttu-id="70a49-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="70a49-145">NOTES</span></span>

## <span data-ttu-id="70a49-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="70a49-146">RELATED LINKS</span></span>
