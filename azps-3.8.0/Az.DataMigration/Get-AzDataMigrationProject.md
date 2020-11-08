---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997273"
---
# <span data-ttu-id="81e80-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="81e80-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="81e80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81e80-102">SYNOPSIS</span></span>
<span data-ttu-id="81e80-103">Ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="81e80-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="81e80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81e80-104">SYNTAX</span></span>

### <span data-ttu-id="81e80-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="81e80-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81e80-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e80-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81e80-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e80-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81e80-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81e80-108">DESCRIPTION</span></span>
<span data-ttu-id="81e80-109">Das Get-AzDataMigrationProject-Cmdlet ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="81e80-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="81e80-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81e80-110">EXAMPLES</span></span>

### <span data-ttu-id="81e80-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81e80-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="81e80-112">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt namens Test Project in der Ressourcengruppe namens testResourceGroup und unter Dienst namens Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81e80-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="81e80-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81e80-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="81e80-114">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt auf Grundlage des PSProject-objekteingabe Parameters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81e80-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="81e80-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="81e80-115">PARAMETERS</span></span>

### <span data-ttu-id="81e80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e80-116">-DefaultProfile</span></span>
<span data-ttu-id="81e80-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81e80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e80-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81e80-118">-InputObject</span></span>
<span data-ttu-id="81e80-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="81e80-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="81e80-120">-Name</span><span class="sxs-lookup"><span data-stu-id="81e80-120">-Name</span></span>
<span data-ttu-id="81e80-121">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="81e80-121">The name of the project.</span></span>

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

### <span data-ttu-id="81e80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e80-122">-ResourceGroupName</span></span>
<span data-ttu-id="81e80-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81e80-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="81e80-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="81e80-124">-ResourceId</span></span>
<span data-ttu-id="81e80-125">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="81e80-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="81e80-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81e80-126">-ServiceName</span></span>
<span data-ttu-id="81e80-127">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="81e80-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="81e80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e80-128">CommonParameters</span></span>
<span data-ttu-id="81e80-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e80-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e80-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e80-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81e80-131">INPUTS</span></span>

### <span data-ttu-id="81e80-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="81e80-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="81e80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="81e80-133">System.String</span></span>

## <span data-ttu-id="81e80-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81e80-134">OUTPUTS</span></span>

### <span data-ttu-id="81e80-135">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="81e80-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="81e80-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="81e80-136">NOTES</span></span>

## <span data-ttu-id="81e80-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81e80-137">RELATED LINKS</span></span>
