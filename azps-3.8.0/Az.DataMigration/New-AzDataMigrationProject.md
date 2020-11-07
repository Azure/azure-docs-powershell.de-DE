---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845324"
---
# <span data-ttu-id="89cde-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="89cde-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="89cde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89cde-102">SYNOPSIS</span></span>
<span data-ttu-id="89cde-103">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="89cde-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="89cde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89cde-104">SYNTAX</span></span>

### <span data-ttu-id="89cde-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89cde-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cde-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89cde-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cde-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89cde-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89cde-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89cde-108">DESCRIPTION</span></span>
<span data-ttu-id="89cde-109">Das New-AzDataMigrationProject-Cmdlet erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="89cde-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="89cde-110">Dieses Cmdlet übernimmt alle erforderlichen Parameter, beispielsweise den Namen der Azure-Ressourcengruppe, den Namen des Azure-Daten Migrations Diensts, in dem das neue Projekt erstellt werden soll, den Bereich, in dem das Projekt erstellt werden soll, den eindeutigen Namen des neuen Projekts, die Quell-und Ziel Verbindungsobjekte sowie das Zielobjekttyp Objekt als Eingabe für die Liste der zu migrierenden Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="89cde-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="89cde-111">Verwenden Sie das New-AzDataMigrationConnectionInfo-Cmdlet, um ein neues ConnectionInfo-Objekt für die Quell-und Zielverbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89cde-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="89cde-112">Die Liste der Microsoft. Azure. Management. datamigration. Models. DatabaseInfo wird für ausgewählte Datenbanken erwartet. Dieses Objekt kann mithilfe New-AzDataMigrationDatabaseInfo-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="89cde-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="89cde-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89cde-113">EXAMPLES</span></span>

### <span data-ttu-id="89cde-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89cde-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="89cde-115">Das obige Beispiel zeigt, wie Sie ein neues Projekt mit dem Namen MyDMSProject erstellen, das sich in der Region Central US unter der Azure Database Migration Service-Instanz mit dem Namen Test Service befindet.</span><span class="sxs-lookup"><span data-stu-id="89cde-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="89cde-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="89cde-116">PARAMETERS</span></span>

### <span data-ttu-id="89cde-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="89cde-117">-DatabaseInfo</span></span>
<span data-ttu-id="89cde-118">Datenbankinformationen.</span><span class="sxs-lookup"><span data-stu-id="89cde-118">Database Infos.</span></span>

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

### <span data-ttu-id="89cde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cde-119">-DefaultProfile</span></span>
<span data-ttu-id="89cde-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89cde-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89cde-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89cde-121">-InputObject</span></span>
<span data-ttu-id="89cde-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="89cde-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="89cde-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="89cde-123">-Location</span></span>
<span data-ttu-id="89cde-124">Der Speicherort der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="89cde-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="89cde-125">-Name</span><span class="sxs-lookup"><span data-stu-id="89cde-125">-Name</span></span>
<span data-ttu-id="89cde-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="89cde-126">The name of the project.</span></span>

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

### <span data-ttu-id="89cde-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89cde-127">-ResourceGroupName</span></span>
<span data-ttu-id="89cde-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89cde-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="89cde-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89cde-129">-ResourceId</span></span>
<span data-ttu-id="89cde-130">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="89cde-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="89cde-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="89cde-131">-ServiceName</span></span>
<span data-ttu-id="89cde-132">Der Name der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="89cde-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="89cde-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="89cde-133">-SourceConnection</span></span>
<span data-ttu-id="89cde-134">Informationen zur Quellverbindung.</span><span class="sxs-lookup"><span data-stu-id="89cde-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="89cde-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="89cde-135">-SourceType</span></span>
<span data-ttu-id="89cde-136">Quell Plattformtyp für Project.</span><span class="sxs-lookup"><span data-stu-id="89cde-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="89cde-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="89cde-137">-TargetConnection</span></span>
<span data-ttu-id="89cde-138">Ziel Verbindungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="89cde-138">Target connection information.</span></span>

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

### <span data-ttu-id="89cde-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="89cde-139">-TargetType</span></span>
<span data-ttu-id="89cde-140">Der Typ der Zielplattform für Project.</span><span class="sxs-lookup"><span data-stu-id="89cde-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="89cde-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89cde-141">-Confirm</span></span>
<span data-ttu-id="89cde-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89cde-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cde-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cde-143">-WhatIf</span></span>
<span data-ttu-id="89cde-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89cde-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89cde-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89cde-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89cde-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cde-146">CommonParameters</span></span>
<span data-ttu-id="89cde-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89cde-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cde-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89cde-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cde-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89cde-149">INPUTS</span></span>

### <span data-ttu-id="89cde-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="89cde-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="89cde-151">System. String</span><span class="sxs-lookup"><span data-stu-id="89cde-151">System.String</span></span>

## <span data-ttu-id="89cde-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89cde-152">OUTPUTS</span></span>

### <span data-ttu-id="89cde-153">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="89cde-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="89cde-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="89cde-154">NOTES</span></span>

## <span data-ttu-id="89cde-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89cde-155">RELATED LINKS</span></span>
