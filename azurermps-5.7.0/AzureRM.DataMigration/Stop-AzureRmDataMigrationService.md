---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505526"
---
# <span data-ttu-id="6339f-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6339f-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="6339f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6339f-102">SYNOPSIS</span></span>
<span data-ttu-id="6339f-103">Beendet eine Instanz des Azure-Daten Bank Migrations Diensts, die sich in einem aktiven Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6339f-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6339f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6339f-104">SYNTAX</span></span>

### <span data-ttu-id="6339f-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6339f-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6339f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6339f-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6339f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6339f-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6339f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6339f-108">DESCRIPTION</span></span>
<span data-ttu-id="6339f-109">Das Stop-AzureRmDataMigrationService-Cmdlet beendet eine Instanz des Azure-Daten Bank Migrations Diensts, der einen aktiven Zustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="6339f-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="6339f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6339f-110">EXAMPLES</span></span>

### <span data-ttu-id="6339f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6339f-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="6339f-112">Das obige Beispiel beendet eine Instanz des Azure Database Migration Service namens Test Service basierend auf dem Dienstnamen, der als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6339f-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="6339f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6339f-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="6339f-114">Im obigen Beispiel wird eine Instanz des Azure Database-Migrations Diensts auf Grundlage des PSDataMigrationService-Objekts beendet, das als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6339f-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="6339f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6339f-115">PARAMETERS</span></span>

### <span data-ttu-id="6339f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6339f-116">-Confirm</span></span>
<span data-ttu-id="6339f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6339f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6339f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6339f-118">-DefaultProfile</span></span>
<span data-ttu-id="6339f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6339f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6339f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6339f-120">-InputObject</span></span>
<span data-ttu-id="6339f-121">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6339f-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="6339f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6339f-122">-Name</span></span>
<span data-ttu-id="6339f-123">Name des Daten Migrations Diensts</span><span class="sxs-lookup"><span data-stu-id="6339f-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="6339f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6339f-124">-PassThru</span></span>
<span data-ttu-id="6339f-125">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="6339f-125">Returns an true/false.</span></span>
<span data-ttu-id="6339f-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6339f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6339f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6339f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6339f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6339f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6339f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6339f-129">-ResourceId</span></span>
<span data-ttu-id="6339f-130">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6339f-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="6339f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6339f-131">-WhatIf</span></span>
<span data-ttu-id="6339f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6339f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6339f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6339f-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6339f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6339f-134">INPUTS</span></span>

### <span data-ttu-id="6339f-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6339f-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="6339f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6339f-136">System.String</span></span>


## <span data-ttu-id="6339f-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6339f-137">OUTPUTS</span></span>

### <span data-ttu-id="6339f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6339f-138">System.Boolean</span></span>


## <span data-ttu-id="6339f-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6339f-139">NOTES</span></span>

## <span data-ttu-id="6339f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6339f-140">RELATED LINKS</span></span>

