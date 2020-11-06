---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498965"
---
# <span data-ttu-id="536da-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="536da-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="536da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="536da-102">SYNOPSIS</span></span>
<span data-ttu-id="536da-103">Ruft die Eigenschaften ab, die einer Instanz des Azure Database Migration Service zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="536da-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="536da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="536da-104">SYNTAX</span></span>

### <span data-ttu-id="536da-105">ResourceGroupSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="536da-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="536da-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="536da-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="536da-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="536da-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="536da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="536da-108">DESCRIPTION</span></span>
<span data-ttu-id="536da-109">Das Get-AzureRmDataMigrationService-Cmdlet ruft die Eigenschaften ab, die einer Instanz des Azure Database-Migrations Diensts zugeordnet sind, basierend auf dem Dienstnamen und dem Namen der Azure-Ressourcengruppe als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="536da-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="536da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="536da-110">EXAMPLES</span></span>

### <span data-ttu-id="536da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="536da-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="536da-112">Im obigen Beispiel werden die Eigenschaften der Azure Database Migration Service-Instanz mit dem Namen Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="536da-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="536da-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="536da-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="536da-114">Im obigen Beispiel werden Azure Database Migration Services in der Ressourcengruppe namens testResourceGroup abgerufen.</span><span class="sxs-lookup"><span data-stu-id="536da-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="536da-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="536da-115">PARAMETERS</span></span>

### <span data-ttu-id="536da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="536da-116">-DefaultProfile</span></span>
<span data-ttu-id="536da-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="536da-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="536da-118">-Name</span><span class="sxs-lookup"><span data-stu-id="536da-118">-Name</span></span>
<span data-ttu-id="536da-119">Name des Daten Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="536da-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="536da-120">-ResourceGroupName</span></span>
<span data-ttu-id="536da-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="536da-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536da-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="536da-122">-ResourceId</span></span>
<span data-ttu-id="536da-123">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="536da-123">DataMigrationService Resource Id.</span></span>

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

## <span data-ttu-id="536da-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="536da-124">INPUTS</span></span>

### <span data-ttu-id="536da-125">System. String</span><span class="sxs-lookup"><span data-stu-id="536da-125">System.String</span></span>


## <span data-ttu-id="536da-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="536da-126">OUTPUTS</span></span>

### <span data-ttu-id="536da-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="536da-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="536da-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="536da-128">NOTES</span></span>

## <span data-ttu-id="536da-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="536da-129">RELATED LINKS</span></span>





