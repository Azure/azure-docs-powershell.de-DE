---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 449a1cfc3156b647eccee6fc320f41fa9e53549c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947920"
---
# <span data-ttu-id="41aed-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="41aed-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="41aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41aed-102">SYNOPSIS</span></span>
<span data-ttu-id="41aed-103">Entfernt ein Azure-Datenbankmigrationsdienstprojekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="41aed-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="41aed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41aed-104">SYNTAX</span></span>

### <span data-ttu-id="41aed-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="41aed-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41aed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41aed-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41aed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41aed-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41aed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41aed-108">DESCRIPTION</span></span>
<span data-ttu-id="41aed-109">Das Remove-AzDataMigrationProject-Cmdlet entfernt ein Azure-Datenbankmigrationsdienstprojekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="41aed-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="41aed-110">Wenn Sie den Parameter DeleteRunningTask bereitstellen, werden alle Azure Database Migration Service-Vorgänge entfernt, die dem entfernten Projekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="41aed-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="41aed-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41aed-111">EXAMPLES</span></span>

### <span data-ttu-id="41aed-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41aed-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="41aed-113">Im vorstehenden Beispiel wird das Projekt "Azure Database Migration Service" mit dem Namen "myDMProject" aus Azure entfernt, basierend auf dem Namen als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="41aed-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="41aed-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="41aed-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="41aed-115">Im vorstehenden Beispiel wird das Azure Database Migration Service-Projekt basierend auf dem PSProject-Objekt als Eingabeparameter entfernt.</span><span class="sxs-lookup"><span data-stu-id="41aed-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="41aed-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41aed-116">PARAMETERS</span></span>

### <span data-ttu-id="41aed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41aed-117">-DefaultProfile</span></span>
<span data-ttu-id="41aed-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41aed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41aed-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="41aed-119">-DeleteRunningTask</span></span>
<span data-ttu-id="41aed-120">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="41aed-120">Delete any running task</span></span>

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

### <span data-ttu-id="41aed-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="41aed-121">-Force</span></span>
<span data-ttu-id="41aed-122">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="41aed-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="41aed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41aed-123">-InputObject</span></span>
<span data-ttu-id="41aed-124">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="41aed-124">PSProject Object.</span></span>

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

### <span data-ttu-id="41aed-125">-Name</span><span class="sxs-lookup"><span data-stu-id="41aed-125">-Name</span></span>
<span data-ttu-id="41aed-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="41aed-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41aed-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41aed-127">-PassThru</span></span>
<span data-ttu-id="41aed-128">Gibt den Wert "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="41aed-128">Returns an true/false.</span></span>
<span data-ttu-id="41aed-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="41aed-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41aed-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41aed-130">-ResourceGroupName</span></span>
<span data-ttu-id="41aed-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41aed-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="41aed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41aed-132">-ResourceId</span></span>
<span data-ttu-id="41aed-133">Projektressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="41aed-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="41aed-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="41aed-134">-ServiceName</span></span>
<span data-ttu-id="41aed-135">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="41aed-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="41aed-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41aed-136">-Confirm</span></span>
<span data-ttu-id="41aed-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41aed-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41aed-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41aed-138">-WhatIf</span></span>
<span data-ttu-id="41aed-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41aed-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41aed-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41aed-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41aed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41aed-141">CommonParameters</span></span>
<span data-ttu-id="41aed-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41aed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41aed-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41aed-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41aed-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41aed-144">INPUTS</span></span>

### <span data-ttu-id="41aed-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="41aed-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="41aed-146">System.String</span><span class="sxs-lookup"><span data-stu-id="41aed-146">System.String</span></span>

## <span data-ttu-id="41aed-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41aed-147">OUTPUTS</span></span>

### <span data-ttu-id="41aed-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41aed-148">System.Boolean</span></span>

## <span data-ttu-id="41aed-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41aed-149">NOTES</span></span>

## <span data-ttu-id="41aed-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41aed-150">RELATED LINKS</span></span>
