---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 4dfe4f52a344b8d2308288cfb659792c7b4aabab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921979"
---
# <span data-ttu-id="86787-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="86787-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="86787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86787-102">SYNOPSIS</span></span>
<span data-ttu-id="86787-103">Ruft die Eigenschaften ab, die einer Instanz des Azure-Datenbankmigrationsdiensts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="86787-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="86787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86787-104">SYNTAX</span></span>

### <span data-ttu-id="86787-105">ResourceGroupSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86787-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86787-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86787-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86787-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="86787-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86787-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86787-108">DESCRIPTION</span></span>
<span data-ttu-id="86787-109">Das Get-AzDataMigrationService-Cmdlet ruft die Eigenschaften ab, die einer Instanz des Azure-Datenbankmigrationsdiensts zugeordnet sind, basierend auf dem Dienstnamen und dem Namen der Azure-Ressourcengruppe als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="86787-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="86787-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86787-110">EXAMPLES</span></span>

### <span data-ttu-id="86787-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86787-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="86787-112">Im vorstehenden Beispiel werden die Eigenschaften der Azure Database Migration Service-Instanz namens "testService" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="86787-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="86787-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="86787-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="86787-114">Im vorstehenden Beispiel werden Azure Database Migration Services in der Ressourcengruppe "testResourceGroup" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="86787-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="86787-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="86787-115">PARAMETERS</span></span>

### <span data-ttu-id="86787-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86787-116">-DefaultProfile</span></span>
<span data-ttu-id="86787-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86787-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86787-118">-Name</span><span class="sxs-lookup"><span data-stu-id="86787-118">-Name</span></span>
<span data-ttu-id="86787-119">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="86787-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86787-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86787-120">-ResourceGroupName</span></span>
<span data-ttu-id="86787-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86787-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86787-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86787-122">-ResourceId</span></span>
<span data-ttu-id="86787-123">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="86787-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="86787-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86787-124">CommonParameters</span></span>
<span data-ttu-id="86787-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86787-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86787-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86787-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86787-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86787-127">INPUTS</span></span>

### <span data-ttu-id="86787-128">System.String</span><span class="sxs-lookup"><span data-stu-id="86787-128">System.String</span></span>

## <span data-ttu-id="86787-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86787-129">OUTPUTS</span></span>

### <span data-ttu-id="86787-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="86787-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="86787-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="86787-131">NOTES</span></span>

## <span data-ttu-id="86787-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="86787-132">RELATED LINKS</span></span>
