---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661247"
---
# <span data-ttu-id="7987e-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="7987e-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="7987e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7987e-102">SYNOPSIS</span></span>
<span data-ttu-id="7987e-103">Ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="7987e-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="7987e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7987e-104">SYNTAX</span></span>

### <span data-ttu-id="7987e-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7987e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7987e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7987e-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7987e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7987e-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7987e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7987e-108">DESCRIPTION</span></span>
<span data-ttu-id="7987e-109">Das Get-AzDataMigrationProject-Cmdlet ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="7987e-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="7987e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7987e-110">EXAMPLES</span></span>

### <span data-ttu-id="7987e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7987e-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="7987e-112">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt namens Test Project in der Ressourcengruppe namens testResourceGroup und unter Dienst namens Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7987e-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="7987e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7987e-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="7987e-114">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt auf Grundlage des PSProject-objekteingabe Parameters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7987e-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="7987e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7987e-115">PARAMETERS</span></span>

### <span data-ttu-id="7987e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7987e-116">-DefaultProfile</span></span>
<span data-ttu-id="7987e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7987e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7987e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7987e-118">-InputObject</span></span>
<span data-ttu-id="7987e-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7987e-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="7987e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7987e-120">-Name</span></span>
<span data-ttu-id="7987e-121">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7987e-121">The name of the project.</span></span>

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

### <span data-ttu-id="7987e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7987e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7987e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7987e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="7987e-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7987e-124">-ResourceId</span></span>
<span data-ttu-id="7987e-125">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7987e-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="7987e-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7987e-126">-ServiceName</span></span>
<span data-ttu-id="7987e-127">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="7987e-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="7987e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7987e-128">CommonParameters</span></span>
<span data-ttu-id="7987e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7987e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7987e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7987e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7987e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7987e-131">INPUTS</span></span>

### <span data-ttu-id="7987e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="7987e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="7987e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7987e-133">System.String</span></span>

## <span data-ttu-id="7987e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7987e-134">OUTPUTS</span></span>

### <span data-ttu-id="7987e-135">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="7987e-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="7987e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7987e-136">NOTES</span></span>

## <span data-ttu-id="7987e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7987e-137">RELATED LINKS</span></span>
