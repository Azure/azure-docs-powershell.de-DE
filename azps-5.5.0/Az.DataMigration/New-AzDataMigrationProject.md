---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167801"
---
# <span data-ttu-id="8e74f-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="8e74f-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="8e74f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e74f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e74f-103">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="8e74f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e74f-104">SYNTAX</span></span>

### <span data-ttu-id="8e74f-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e74f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e74f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e74f-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e74f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e74f-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e74f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e74f-108">DESCRIPTION</span></span>
<span data-ttu-id="8e74f-109">Das New-AzDataMigrationProject A0 erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="8e74f-110">Dieses Cmdlet übernimmt alle erforderlichen Parameter, z. B. den Namen der Azure-Ressourcengruppe, den Namen des Azure Data Migration Service, in dem ein neues Projekt erstellt werden soll, die Region, in der das Projekt erstellt werden soll, den eindeutigen Namen des neuen Projekts, die Quell- und Zielverbindungsobjekte und das Zieltypobjekt als Eingabe für die Liste der zu migrierenden Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="8e74f-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="8e74f-111">Verwenden Sie New-AzDataMigrationConnectionInfo A0 zum Erstellen eines neuen ConnectionInfo-Objekts für die Quell- und Zielverbindungen.</span><span class="sxs-lookup"><span data-stu-id="8e74f-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="8e74f-112">Die Liste von "Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo" wird für ausgewählte Datenbanken erwartet. dieses Objekt kann mithilfe eines cmdlets New-AzDataMigrationDatabaseInfo werden.</span><span class="sxs-lookup"><span data-stu-id="8e74f-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="8e74f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e74f-113">EXAMPLES</span></span>

### <span data-ttu-id="8e74f-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e74f-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="8e74f-115">Das beispiel oben zeigt, wie Sie ein neues Projekt mit dem Namen "MyDMSProject" erstellen, das sich in der Region "USA, Mitte" unter der Azure Database Migration Service-Instanz namens TestService befindet.</span><span class="sxs-lookup"><span data-stu-id="8e74f-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="8e74f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e74f-116">PARAMETERS</span></span>

### <span data-ttu-id="8e74f-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8e74f-117">-DatabaseInfo</span></span>
<span data-ttu-id="8e74f-118">Datenbankinformationen.</span><span class="sxs-lookup"><span data-stu-id="8e74f-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e74f-119">-DefaultProfile</span></span>
<span data-ttu-id="8e74f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e74f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e74f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e74f-121">-InputObject</span></span>
<span data-ttu-id="8e74f-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8e74f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8e74f-123">-Location</span></span>
<span data-ttu-id="8e74f-124">Der Speicherort der Azure-Datenbankmigrationsdienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="8e74f-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e74f-125">-Name</span></span>
<span data-ttu-id="8e74f-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="8e74f-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e74f-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e74f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e74f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e74f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e74f-129">-ResourceId</span></span>
<span data-ttu-id="8e74f-130">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8e74f-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8e74f-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e74f-131">-ServiceName</span></span>
<span data-ttu-id="8e74f-132">Der Name der Azure-Datenbankmigrationsdienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="8e74f-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="8e74f-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="8e74f-133">-SourceConnection</span></span>
<span data-ttu-id="8e74f-134">Quellverbindungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="8e74f-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="8e74f-135">-SourceType</span></span>
<span data-ttu-id="8e74f-136">Quellplattformtyp für Projekt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="8e74f-137">-TargetConnection</span></span>
<span data-ttu-id="8e74f-138">Zielverbindungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="8e74f-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="8e74f-139">-TargetType</span></span>
<span data-ttu-id="8e74f-140">Zielplattformtyp für Projekt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e74f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e74f-141">-Confirm</span></span>
<span data-ttu-id="8e74f-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e74f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e74f-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e74f-143">-WhatIf</span></span>
<span data-ttu-id="8e74f-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e74f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e74f-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e74f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e74f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e74f-146">CommonParameters</span></span>
<span data-ttu-id="8e74f-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e74f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e74f-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e74f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e74f-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e74f-149">INPUTS</span></span>

### <span data-ttu-id="8e74f-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8e74f-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="8e74f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="8e74f-151">System.String</span></span>

## <span data-ttu-id="8e74f-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e74f-152">OUTPUTS</span></span>

### <span data-ttu-id="8e74f-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="8e74f-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="8e74f-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e74f-154">NOTES</span></span>

## <span data-ttu-id="8e74f-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e74f-155">RELATED LINKS</span></span>
