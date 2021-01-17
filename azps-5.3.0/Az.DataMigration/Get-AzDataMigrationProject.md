---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458023"
---
# <span data-ttu-id="95ff7-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="95ff7-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="95ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="95ff7-103">Ruft die Eigenschaften eines Azure-Datenbankmigrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="95ff7-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="95ff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95ff7-104">SYNTAX</span></span>

### <span data-ttu-id="95ff7-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95ff7-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95ff7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95ff7-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95ff7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95ff7-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95ff7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95ff7-108">DESCRIPTION</span></span>
<span data-ttu-id="95ff7-109">Das Get-AzDataMigrationProject cmdlet ruft die Eigenschaften eines Azure-Datenbankmigrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="95ff7-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="95ff7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="95ff7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95ff7-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="95ff7-112">Im vorstehenden Beispiel wird das Azure-Datenbankmigrationsprojekt mit dem Namen "TestProject" in der Ressourcengruppe mit dem Namen "testResourceGroup" und unter "testService" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="95ff7-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="95ff7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95ff7-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="95ff7-114">Im vorstehenden Beispiel wird das Azure-Datenbankmigrationsprojekt basierend auf dem übergebenen Parameter für die Eingabe des OBJEKTS "PSProject" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="95ff7-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="95ff7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95ff7-115">PARAMETERS</span></span>

### <span data-ttu-id="95ff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ff7-116">-DefaultProfile</span></span>
<span data-ttu-id="95ff7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ff7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95ff7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ff7-118">-InputObject</span></span>
<span data-ttu-id="95ff7-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95ff7-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="95ff7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="95ff7-120">-Name</span></span>
<span data-ttu-id="95ff7-121">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="95ff7-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ff7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ff7-122">-ResourceGroupName</span></span>
<span data-ttu-id="95ff7-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95ff7-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="95ff7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95ff7-124">-ResourceId</span></span>
<span data-ttu-id="95ff7-125">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="95ff7-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="95ff7-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95ff7-126">-ServiceName</span></span>
<span data-ttu-id="95ff7-127">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="95ff7-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="95ff7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ff7-128">CommonParameters</span></span>
<span data-ttu-id="95ff7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ff7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ff7-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ff7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ff7-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95ff7-131">INPUTS</span></span>

### <span data-ttu-id="95ff7-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="95ff7-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="95ff7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="95ff7-133">System.String</span></span>

## <span data-ttu-id="95ff7-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95ff7-134">OUTPUTS</span></span>

### <span data-ttu-id="95ff7-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="95ff7-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="95ff7-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95ff7-136">NOTES</span></span>

## <span data-ttu-id="95ff7-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95ff7-137">RELATED LINKS</span></span>
