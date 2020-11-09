---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297693"
---
# <span data-ttu-id="2f966-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2f966-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="2f966-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f966-102">SYNOPSIS</span></span>
<span data-ttu-id="2f966-103">Ruft die Eigenschaften ab, die einer Instanz des Azure Database Migration Service zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2f966-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="2f966-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f966-104">SYNTAX</span></span>

### <span data-ttu-id="2f966-105">ResourceGroupSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f966-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f966-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f966-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f966-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="2f966-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f966-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f966-108">DESCRIPTION</span></span>
<span data-ttu-id="2f966-109">Das Get-AzDataMigrationService-Cmdlet ruft die Eigenschaften ab, die einer Instanz des Azure Database-Migrations Diensts zugeordnet sind, basierend auf dem Dienstnamen und dem Namen der Azure-Ressourcengruppe als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="2f966-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="2f966-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f966-110">EXAMPLES</span></span>

### <span data-ttu-id="2f966-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f966-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="2f966-112">Im obigen Beispiel werden die Eigenschaften der Azure Database Migration Service-Instanz mit dem Namen Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f966-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="2f966-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2f966-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="2f966-114">Im obigen Beispiel werden Azure Database Migration Services in der Ressourcengruppe namens testResourceGroup abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f966-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="2f966-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f966-115">PARAMETERS</span></span>

### <span data-ttu-id="2f966-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f966-116">-DefaultProfile</span></span>
<span data-ttu-id="2f966-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f966-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f966-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2f966-118">-Name</span></span>
<span data-ttu-id="2f966-119">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="2f966-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="2f966-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f966-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f966-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f966-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f966-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2f966-122">-ResourceId</span></span>
<span data-ttu-id="2f966-123">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2f966-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="2f966-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f966-124">CommonParameters</span></span>
<span data-ttu-id="2f966-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f966-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f966-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f966-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f966-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f966-127">INPUTS</span></span>

### <span data-ttu-id="2f966-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2f966-128">System.String</span></span>

## <span data-ttu-id="2f966-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f966-129">OUTPUTS</span></span>

### <span data-ttu-id="2f966-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2f966-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="2f966-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f966-131">NOTES</span></span>

## <span data-ttu-id="2f966-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f966-132">RELATED LINKS</span></span>
