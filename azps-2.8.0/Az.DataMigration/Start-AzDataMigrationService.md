---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 67194bfc9a7ce1971817c7f80e7a5ee61caf6db0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651452"
---
# <span data-ttu-id="23f18-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="23f18-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="23f18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23f18-102">SYNOPSIS</span></span>
<span data-ttu-id="23f18-103">Startet eine Instanz des Azure Database Migration Service im Zustand Stopped.</span><span class="sxs-lookup"><span data-stu-id="23f18-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="23f18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23f18-104">SYNTAX</span></span>

### <span data-ttu-id="23f18-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23f18-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f18-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f18-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f18-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f18-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f18-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23f18-108">DESCRIPTION</span></span>
<span data-ttu-id="23f18-109">Mit dem Start-AzDataMigrationService-Cmdlet wird eine Instanz des Azure Database Migration Service im Zustand Stopped gestartet.</span><span class="sxs-lookup"><span data-stu-id="23f18-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="23f18-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23f18-110">EXAMPLES</span></span>

### <span data-ttu-id="23f18-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23f18-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="23f18-112">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz mit dem Namen Test Dienst in einem Stopped-Zustand basierend auf dem als Eingabe übergebenen Dienstnamen gestartet.</span><span class="sxs-lookup"><span data-stu-id="23f18-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="23f18-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23f18-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="23f18-114">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz auf Grundlage von PSDataMigrationService gestartet, die als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="23f18-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="23f18-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="23f18-115">PARAMETERS</span></span>

### <span data-ttu-id="23f18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f18-116">-DefaultProfile</span></span>
<span data-ttu-id="23f18-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23f18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f18-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23f18-118">-InputObject</span></span>
<span data-ttu-id="23f18-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="23f18-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="23f18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="23f18-120">-Name</span></span>
<span data-ttu-id="23f18-121">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="23f18-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="23f18-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23f18-122">-PassThru</span></span>
<span data-ttu-id="23f18-123">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="23f18-123">Returns an true/false.</span></span>
<span data-ttu-id="23f18-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="23f18-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23f18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f18-125">-ResourceGroupName</span></span>
<span data-ttu-id="23f18-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="23f18-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="23f18-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="23f18-127">-ResourceId</span></span>
<span data-ttu-id="23f18-128">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="23f18-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="23f18-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23f18-129">-Confirm</span></span>
<span data-ttu-id="23f18-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23f18-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f18-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f18-131">-WhatIf</span></span>
<span data-ttu-id="23f18-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23f18-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f18-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23f18-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f18-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f18-134">CommonParameters</span></span>
<span data-ttu-id="23f18-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f18-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f18-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f18-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f18-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23f18-137">INPUTS</span></span>

### <span data-ttu-id="23f18-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="23f18-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="23f18-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23f18-139">System.String</span></span>

## <span data-ttu-id="23f18-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23f18-140">OUTPUTS</span></span>

### <span data-ttu-id="23f18-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23f18-141">System.Boolean</span></span>

## <span data-ttu-id="23f18-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="23f18-142">NOTES</span></span>

## <span data-ttu-id="23f18-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23f18-143">RELATED LINKS</span></span>
