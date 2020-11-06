---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476785"
---
# <span data-ttu-id="5b4e2-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5b4e2-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="5b4e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4e2-103">Startet eine Instanz des Azure Database Migration Service im Zustand Stopped.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b4e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b4e2-104">SYNTAX</span></span>

### <span data-ttu-id="5b4e2-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b4e2-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5b4e2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b4e2-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5b4e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b4e2-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5b4e2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b4e2-108">DESCRIPTION</span></span>
<span data-ttu-id="5b4e2-109">Mit dem Start-AzureRmDataMigrationService-Cmdlet wird eine Instanz des Azure Database Migration Service im Zustand Stopped gestartet.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="5b4e2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b4e2-110">EXAMPLES</span></span>

### <span data-ttu-id="5b4e2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b4e2-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="5b4e2-112">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz mit dem Namen Test Dienst in einem Stopped-Zustand basierend auf dem als Eingabe übergebenen Dienstnamen gestartet.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="5b4e2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b4e2-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="5b4e2-114">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz auf Grundlage von PSDataMigrationService gestartet, die als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="5b4e2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b4e2-115">PARAMETERS</span></span>

### <span data-ttu-id="5b4e2-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b4e2-116">-Confirm</span></span>
<span data-ttu-id="5b4e2-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4e2-118">-DefaultProfile</span></span>
<span data-ttu-id="5b4e2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b4e2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b4e2-120">-InputObject</span></span>
<span data-ttu-id="5b4e2-121">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="5b4e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4e2-122">-Name</span></span>
<span data-ttu-id="5b4e2-123">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="5b4e2-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b4e2-124">-PassThru</span></span>
<span data-ttu-id="5b4e2-125">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-125">Returns an true/false.</span></span>
<span data-ttu-id="5b4e2-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b4e2-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5b4e2-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b4e2-129">-ResourceId</span></span>
<span data-ttu-id="5b4e2-130">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5b4e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4e2-131">-WhatIf</span></span>
<span data-ttu-id="5b4e2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4e2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b4e2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5b4e2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b4e2-134">INPUTS</span></span>

### <span data-ttu-id="5b4e2-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5b4e2-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="5b4e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5b4e2-136">System.String</span></span>


## <span data-ttu-id="5b4e2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b4e2-137">OUTPUTS</span></span>

### <span data-ttu-id="5b4e2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b4e2-138">System.Boolean</span></span>


## <span data-ttu-id="5b4e2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b4e2-139">NOTES</span></span>

## <span data-ttu-id="5b4e2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b4e2-140">RELATED LINKS</span></span>


