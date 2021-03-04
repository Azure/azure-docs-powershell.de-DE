---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: 9a6d2ba213054ea6b670205e84e3fd3893c59eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931896"
---
# <span data-ttu-id="66dee-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="66dee-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="66dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66dee-102">SYNOPSIS</span></span>
<span data-ttu-id="66dee-103">Beendet eine Instanz des Azure-Datenbankmigrationsdiensts, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="66dee-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="66dee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66dee-104">SYNTAX</span></span>

### <span data-ttu-id="66dee-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66dee-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66dee-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66dee-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66dee-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66dee-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66dee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66dee-108">DESCRIPTION</span></span>
<span data-ttu-id="66dee-109">Das Stop-AzDataMigrationService-Cmdlet beendet eine Instanz des Azure-Datenbankmigrationsdiensts, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="66dee-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="66dee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66dee-110">EXAMPLES</span></span>

### <span data-ttu-id="66dee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66dee-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="66dee-112">Im obigen Beispiel wird eine Instanz des Azure Database Migration Service namens TestService basierend auf dem als Eingabeparameter übergebenen Dienstnamen beendet.</span><span class="sxs-lookup"><span data-stu-id="66dee-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="66dee-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66dee-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="66dee-114">Im vorstehenden Beispiel wird eine Instanz des Azure Database Migration Service beendet, die auf dem PSDataMigrationService-Objekt basiert, das als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="66dee-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="66dee-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66dee-115">PARAMETERS</span></span>

### <span data-ttu-id="66dee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dee-116">-DefaultProfile</span></span>
<span data-ttu-id="66dee-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66dee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66dee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66dee-118">-InputObject</span></span>
<span data-ttu-id="66dee-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="66dee-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="66dee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66dee-120">-Name</span></span>
<span data-ttu-id="66dee-121">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="66dee-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66dee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66dee-122">-PassThru</span></span>
<span data-ttu-id="66dee-123">Gibt den Wert "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="66dee-123">Returns an true/false.</span></span>
<span data-ttu-id="66dee-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="66dee-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66dee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dee-125">-ResourceGroupName</span></span>
<span data-ttu-id="66dee-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66dee-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="66dee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66dee-127">-ResourceId</span></span>
<span data-ttu-id="66dee-128">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="66dee-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="66dee-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66dee-129">-Confirm</span></span>
<span data-ttu-id="66dee-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66dee-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66dee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66dee-131">-WhatIf</span></span>
<span data-ttu-id="66dee-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66dee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66dee-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66dee-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66dee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dee-134">CommonParameters</span></span>
<span data-ttu-id="66dee-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66dee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dee-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66dee-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dee-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66dee-137">INPUTS</span></span>

### <span data-ttu-id="66dee-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="66dee-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="66dee-139">System.String</span><span class="sxs-lookup"><span data-stu-id="66dee-139">System.String</span></span>

## <span data-ttu-id="66dee-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66dee-140">OUTPUTS</span></span>

### <span data-ttu-id="66dee-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66dee-141">System.Boolean</span></span>

## <span data-ttu-id="66dee-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66dee-142">NOTES</span></span>

## <span data-ttu-id="66dee-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66dee-143">RELATED LINKS</span></span>
