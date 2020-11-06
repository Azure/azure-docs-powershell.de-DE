---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496222"
---
# <span data-ttu-id="f8ab5-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f8ab5-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="f8ab5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ab5-103">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ab5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ab5-104">SYNTAX</span></span>

### <span data-ttu-id="f8ab5-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8ab5-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8ab5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8ab5-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8ab5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8ab5-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ab5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="f8ab5-109">Das New-AzureRmDataMigrationProject-Cmdlet erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="f8ab5-110">Dieses Cmdlet übernimmt alle erforderlichen Parameter, beispielsweise den Namen der Azure-Ressourcengruppe, den Namen des Azure-Daten Migrations Diensts, in dem das neue Projekt erstellt werden soll, den Bereich, in dem das Projekt erstellt werden soll, den eindeutigen Namen des neuen Projekts, die Quell-und Ziel Verbindungsobjekte sowie das Zielobjekttyp Objekt als Eingabe für die Liste der zu migrierenden Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="f8ab5-111">Verwenden Sie das New-AzureRmDataMigrationConnectionInfo-Cmdlet, um ein neues ConnectionInfo-Objekt für die Quell-und Zielverbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="f8ab5-112">Die Liste der Microsoft. Azure. Management. datamigration. Models. DatabaseInfo wird für ausgewählte Datenbanken erwartet. Dieses Objekt kann mithilfe New-AzureRmDataMigrationDatabaseInfo-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="f8ab5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8ab5-113">EXAMPLES</span></span>

### <span data-ttu-id="f8ab5-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8ab5-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="f8ab5-115">Das obige Beispiel zeigt, wie Sie ein neues Projekt mit dem Namen MyDMSProject erstellen, das sich in der Region Central US unter der Azure Database Migration Service-Instanz mit dem Namen Test Service befindet.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="f8ab5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ab5-116">PARAMETERS</span></span>

### <span data-ttu-id="f8ab5-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f8ab5-117">-DatabaseInfo</span></span>
<span data-ttu-id="f8ab5-118">Datenbankinformationen.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-118">Database Infos.</span></span>

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

### <span data-ttu-id="f8ab5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ab5-119">-DefaultProfile</span></span>
<span data-ttu-id="f8ab5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ab5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8ab5-121">-InputObject</span></span>
<span data-ttu-id="f8ab5-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="f8ab5-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="f8ab5-123">-Location</span></span>
<span data-ttu-id="f8ab5-124">Der Speicherort der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="f8ab5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f8ab5-125">-Name</span></span>
<span data-ttu-id="f8ab5-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-126">The name of the project.</span></span>

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

### <span data-ttu-id="f8ab5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ab5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8ab5-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8ab5-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8ab5-129">-ResourceId</span></span>
<span data-ttu-id="f8ab5-130">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="f8ab5-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f8ab5-131">-ServiceName</span></span>
<span data-ttu-id="f8ab5-132">Der Name der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="f8ab5-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="f8ab5-133">-SourceConnection</span></span>
<span data-ttu-id="f8ab5-134">Informationen zur Quellverbindung.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="f8ab5-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f8ab5-135">-SourceType</span></span>
<span data-ttu-id="f8ab5-136">Quell Plattformtyp für Project.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="f8ab5-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="f8ab5-137">-TargetConnection</span></span>
<span data-ttu-id="f8ab5-138">Ziel Verbindungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-138">Target connection information.</span></span>

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

### <span data-ttu-id="f8ab5-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="f8ab5-139">-TargetType</span></span>
<span data-ttu-id="f8ab5-140">Der Typ der Zielplattform für Project.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="f8ab5-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8ab5-141">-Confirm</span></span>
<span data-ttu-id="f8ab5-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ab5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ab5-143">-WhatIf</span></span>
<span data-ttu-id="f8ab5-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8ab5-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ab5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ab5-146">CommonParameters</span></span>
<span data-ttu-id="f8ab5-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ab5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ab5-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ab5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ab5-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8ab5-149">INPUTS</span></span>

### <span data-ttu-id="f8ab5-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8ab5-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="f8ab5-151">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8ab5-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f8ab5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f8ab5-152">System.String</span></span>

## <span data-ttu-id="f8ab5-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8ab5-153">OUTPUTS</span></span>

### <span data-ttu-id="f8ab5-154">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="f8ab5-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="f8ab5-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8ab5-155">NOTES</span></span>

## <span data-ttu-id="f8ab5-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8ab5-156">RELATED LINKS</span></span>
