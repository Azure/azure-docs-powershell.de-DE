---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503773"
---
# <span data-ttu-id="663cb-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="663cb-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="663cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="663cb-102">SYNOPSIS</span></span>
<span data-ttu-id="663cb-103">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="663cb-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="663cb-104">SYNTAX</span></span>

### <span data-ttu-id="663cb-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="663cb-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="663cb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="663cb-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="663cb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="663cb-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="663cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="663cb-108">DESCRIPTION</span></span>
<span data-ttu-id="663cb-109">Das New-AzureRmDataMigrationProject-Cmdlet erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="663cb-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="663cb-110">Dieses Cmdlet übernimmt alle erforderlichen Parameter, beispielsweise den Namen der Azure-Ressourcengruppe, den Namen des Azure-Daten Migrations Diensts, in dem das neue Projekt erstellt werden soll, den Bereich, in dem das Projekt erstellt werden soll, den eindeutigen Namen des neuen Projekts, die Quell-und Ziel Verbindungsobjekte sowie das Zielobjekttyp Objekt als Eingabe für die Liste der zu migrierenden Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="663cb-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="663cb-111">Verwenden Sie das New-AzureRmDataMigrationConnectionInfo-Cmdlet, um ein neues ConnectionInfo-Objekt für die Quell-und Zielverbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="663cb-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="663cb-112">Die Liste der Microsoft. Azure. Management. datamigration. Models. DatabaseInfo wird für ausgewählte Datenbanken erwartet. Dieses Objekt kann mithilfe New-AzureRmDataMigrationDatabaseInfo-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="663cb-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="663cb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="663cb-113">EXAMPLES</span></span>

### <span data-ttu-id="663cb-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="663cb-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="663cb-115">Das obige Beispiel zeigt, wie Sie ein neues Projekt mit dem Namen MyDMSProject erstellen, das sich in der Region Central US unter der Azure Database Migration Service-Instanz mit dem Namen Test Service befindet.</span><span class="sxs-lookup"><span data-stu-id="663cb-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="663cb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="663cb-116">PARAMETERS</span></span>

### <span data-ttu-id="663cb-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="663cb-117">-Confirm</span></span>
<span data-ttu-id="663cb-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="663cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663cb-119">-DatabaseInfo []</span><span class="sxs-lookup"><span data-stu-id="663cb-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="663cb-120">Datenbankinformationen</span><span class="sxs-lookup"><span data-stu-id="663cb-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663cb-121">-DefaultProfile</span></span>
<span data-ttu-id="663cb-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="663cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663cb-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="663cb-123">-Location</span></span>
<span data-ttu-id="663cb-124">Der Speicherort der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="663cb-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="663cb-125">-ProjectName</span></span>
<span data-ttu-id="663cb-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="663cb-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="663cb-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="663cb-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="663cb-129">-ServiceName</span></span>
<span data-ttu-id="663cb-130">Der Name der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="663cb-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="663cb-131">-SourceConnection</span></span>
<span data-ttu-id="663cb-132">Informationen zur Quellverbindung.</span><span class="sxs-lookup"><span data-stu-id="663cb-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="663cb-133">-SourceType</span></span>
<span data-ttu-id="663cb-134">Quell Plattformtyp für Project.</span><span class="sxs-lookup"><span data-stu-id="663cb-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="663cb-135">-TargetConnection</span></span>
<span data-ttu-id="663cb-136">Ziel Verbindungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="663cb-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663cb-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="663cb-137">-TargetType</span></span>
<span data-ttu-id="663cb-138">Der Typ der Zielplattform für Project.</span><span class="sxs-lookup"><span data-stu-id="663cb-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="663cb-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="663cb-139">OUTPUTS</span></span>

### <span data-ttu-id="663cb-140">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="663cb-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="663cb-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="663cb-141">NOTES</span></span>

## <span data-ttu-id="663cb-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="663cb-142">RELATED LINKS</span></span>

