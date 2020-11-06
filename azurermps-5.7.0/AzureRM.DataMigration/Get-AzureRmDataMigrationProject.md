---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502610"
---
# <span data-ttu-id="85c40-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="85c40-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="85c40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85c40-102">SYNOPSIS</span></span>
<span data-ttu-id="85c40-103">Ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="85c40-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85c40-104">SYNTAX</span></span>

### <span data-ttu-id="85c40-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85c40-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="85c40-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c40-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="85c40-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c40-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="85c40-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85c40-108">DESCRIPTION</span></span>
<span data-ttu-id="85c40-109">Das Get-AzureRmDataMigrationProject-Cmdlet ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="85c40-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="85c40-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85c40-110">EXAMPLES</span></span>

### <span data-ttu-id="85c40-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85c40-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="85c40-112">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt namens Test Project in der Ressourcengruppe namens testResourceGroup und unter Dienst namens Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85c40-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="85c40-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85c40-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="85c40-114">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt auf Grundlage des PSProject-objekteingabe Parameters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="85c40-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="85c40-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="85c40-115">PARAMETERS</span></span>

### <span data-ttu-id="85c40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c40-116">-DefaultProfile</span></span>
<span data-ttu-id="85c40-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85c40-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c40-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85c40-118">-InputObject</span></span>
<span data-ttu-id="85c40-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="85c40-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="85c40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85c40-120">-Name</span></span>
<span data-ttu-id="85c40-121">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="85c40-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c40-122">-ResourceGroupName</span></span>
<span data-ttu-id="85c40-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85c40-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="85c40-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="85c40-124">-ResourceId</span></span>
<span data-ttu-id="85c40-125">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="85c40-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="85c40-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="85c40-126">-ServiceName</span></span>
<span data-ttu-id="85c40-127">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="85c40-127">Data Migration Service Name.</span></span>

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

## <span data-ttu-id="85c40-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85c40-128">INPUTS</span></span>

### <span data-ttu-id="85c40-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="85c40-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="85c40-130">System. String</span><span class="sxs-lookup"><span data-stu-id="85c40-130">System.String</span></span>


## <span data-ttu-id="85c40-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85c40-131">OUTPUTS</span></span>

### <span data-ttu-id="85c40-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. datamigration. Models. PSProject, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="85c40-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="85c40-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="85c40-133">NOTES</span></span>

## <span data-ttu-id="85c40-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85c40-134">RELATED LINKS</span></span>

