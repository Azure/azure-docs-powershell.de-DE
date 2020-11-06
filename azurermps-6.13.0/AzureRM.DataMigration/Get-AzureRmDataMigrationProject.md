---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499550"
---
# <span data-ttu-id="91b17-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="91b17-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="91b17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91b17-102">SYNOPSIS</span></span>
<span data-ttu-id="91b17-103">Ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="91b17-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91b17-104">SYNTAX</span></span>

### <span data-ttu-id="91b17-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91b17-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b17-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b17-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b17-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b17-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91b17-108">DESCRIPTION</span></span>
<span data-ttu-id="91b17-109">Das Get-AzureRmDataMigrationProject-Cmdlet ruft die Eigenschaften eines Azure-Daten Bank Migrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="91b17-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="91b17-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91b17-110">EXAMPLES</span></span>

### <span data-ttu-id="91b17-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91b17-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="91b17-112">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt namens Test Project in der Ressourcengruppe namens testResourceGroup und unter Dienst namens Test Service abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91b17-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="91b17-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="91b17-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="91b17-114">Im obigen Beispiel wird das Azure-Daten Bank Migrationsprojekt auf Grundlage des PSProject-objekteingabe Parameters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91b17-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="91b17-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="91b17-115">PARAMETERS</span></span>

### <span data-ttu-id="91b17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b17-116">-DefaultProfile</span></span>
<span data-ttu-id="91b17-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91b17-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b17-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91b17-118">-InputObject</span></span>
<span data-ttu-id="91b17-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="91b17-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="91b17-120">-Name</span><span class="sxs-lookup"><span data-stu-id="91b17-120">-Name</span></span>
<span data-ttu-id="91b17-121">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="91b17-121">The name of the project.</span></span>

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

### <span data-ttu-id="91b17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b17-122">-ResourceGroupName</span></span>
<span data-ttu-id="91b17-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91b17-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="91b17-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91b17-124">-ResourceId</span></span>
<span data-ttu-id="91b17-125">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="91b17-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="91b17-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="91b17-126">-ServiceName</span></span>
<span data-ttu-id="91b17-127">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="91b17-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="91b17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b17-128">CommonParameters</span></span>
<span data-ttu-id="91b17-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b17-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b17-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b17-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91b17-131">INPUTS</span></span>

### <span data-ttu-id="91b17-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="91b17-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="91b17-133">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91b17-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="91b17-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91b17-134">System.String</span></span>

## <span data-ttu-id="91b17-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91b17-135">OUTPUTS</span></span>

### <span data-ttu-id="91b17-136">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="91b17-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="91b17-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="91b17-137">NOTES</span></span>

## <span data-ttu-id="91b17-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91b17-138">RELATED LINKS</span></span>
