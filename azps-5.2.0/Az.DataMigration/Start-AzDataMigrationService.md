---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292283"
---
# <span data-ttu-id="9a199-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9a199-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="9a199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a199-102">SYNOPSIS</span></span>
<span data-ttu-id="9a199-103">Startet eine Instanz des Azure-Datenbankmigrationsdiensts in einem angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="9a199-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="9a199-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a199-104">SYNTAX</span></span>

### <span data-ttu-id="9a199-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a199-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a199-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a199-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a199-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a199-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a199-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a199-108">DESCRIPTION</span></span>
<span data-ttu-id="9a199-109">Das Start-AzDataMigrationService cmdlet startet eine Instanz des Azure Database Migration Service in einem angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="9a199-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="9a199-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a199-110">EXAMPLES</span></span>

### <span data-ttu-id="9a199-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a199-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="9a199-112">Im vorstehenden Beispiel wird eine Azure-Datenbankmigrationsdienstinstanz mit dem Namen "Testdienst" in einem beendeten Zustand gestartet, basierend auf dem Dienstnamen, der als Eingabe übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9a199-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="9a199-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9a199-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="9a199-114">Im vorstehenden Beispiel wird eine Instanz des Azure Database Migration Service gestartet, die auf PSDataMigrationService basiert, das als Eingabeparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a199-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="9a199-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a199-115">PARAMETERS</span></span>

### <span data-ttu-id="9a199-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a199-116">-DefaultProfile</span></span>
<span data-ttu-id="9a199-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a199-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a199-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a199-118">-InputObject</span></span>
<span data-ttu-id="9a199-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9a199-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="9a199-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a199-120">-Name</span></span>
<span data-ttu-id="9a199-121">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="9a199-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9a199-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a199-122">-PassThru</span></span>
<span data-ttu-id="9a199-123">Gibt "true/false" zurück.</span><span class="sxs-lookup"><span data-stu-id="9a199-123">Returns an true/false.</span></span>
<span data-ttu-id="9a199-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="9a199-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a199-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a199-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a199-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9a199-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a199-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a199-127">-ResourceId</span></span>
<span data-ttu-id="9a199-128">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9a199-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9a199-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a199-129">-Confirm</span></span>
<span data-ttu-id="9a199-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a199-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a199-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9a199-131">-WhatIf</span></span>
<span data-ttu-id="9a199-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a199-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a199-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a199-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a199-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a199-134">CommonParameters</span></span>
<span data-ttu-id="9a199-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a199-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a199-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a199-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a199-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a199-137">INPUTS</span></span>

### <span data-ttu-id="9a199-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9a199-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="9a199-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a199-139">System.String</span></span>

## <span data-ttu-id="9a199-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a199-140">OUTPUTS</span></span>

### <span data-ttu-id="9a199-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a199-141">System.Boolean</span></span>

## <span data-ttu-id="9a199-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9a199-142">NOTES</span></span>

## <span data-ttu-id="9a199-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9a199-143">RELATED LINKS</span></span>
