---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505401"
---
# <span data-ttu-id="3cb45-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3cb45-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="3cb45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cb45-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb45-103">Startet eine Instanz des Azure Database Migration Service im Zustand Stopped.</span><span class="sxs-lookup"><span data-stu-id="3cb45-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb45-104">SYNTAX</span></span>

### <span data-ttu-id="3cb45-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cb45-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb45-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cb45-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb45-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cb45-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb45-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cb45-108">DESCRIPTION</span></span>
<span data-ttu-id="3cb45-109">Mit dem Start-AzureRmDataMigrationService-Cmdlet wird eine Instanz des Azure Database Migration Service im Zustand Stopped gestartet.</span><span class="sxs-lookup"><span data-stu-id="3cb45-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="3cb45-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cb45-110">EXAMPLES</span></span>

### <span data-ttu-id="3cb45-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cb45-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="3cb45-112">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz mit dem Namen Test Dienst in einem Stopped-Zustand basierend auf dem als Eingabe übergebenen Dienstnamen gestartet.</span><span class="sxs-lookup"><span data-stu-id="3cb45-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="3cb45-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3cb45-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="3cb45-114">Im obigen Beispiel wird eine Azure Database Migration Service-Instanz auf Grundlage von PSDataMigrationService gestartet, die als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3cb45-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="3cb45-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb45-115">PARAMETERS</span></span>

### <span data-ttu-id="3cb45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb45-116">-DefaultProfile</span></span>
<span data-ttu-id="3cb45-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cb45-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb45-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cb45-118">-InputObject</span></span>
<span data-ttu-id="3cb45-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb45-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="3cb45-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb45-120">-Name</span></span>
<span data-ttu-id="3cb45-121">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="3cb45-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3cb45-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cb45-122">-PassThru</span></span>
<span data-ttu-id="3cb45-123">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="3cb45-123">Returns an true/false.</span></span>
<span data-ttu-id="3cb45-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3cb45-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3cb45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb45-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cb45-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cb45-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cb45-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3cb45-127">-ResourceId</span></span>
<span data-ttu-id="3cb45-128">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3cb45-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="3cb45-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cb45-129">-Confirm</span></span>
<span data-ttu-id="3cb45-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cb45-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb45-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb45-131">-WhatIf</span></span>
<span data-ttu-id="3cb45-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cb45-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb45-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cb45-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb45-134">CommonParameters</span></span>
<span data-ttu-id="3cb45-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb45-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb45-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb45-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cb45-137">INPUTS</span></span>

### <span data-ttu-id="3cb45-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3cb45-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="3cb45-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3cb45-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3cb45-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb45-140">System.String</span></span>

## <span data-ttu-id="3cb45-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cb45-141">OUTPUTS</span></span>

### <span data-ttu-id="3cb45-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cb45-142">System.Boolean</span></span>

## <span data-ttu-id="3cb45-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cb45-143">NOTES</span></span>

## <span data-ttu-id="3cb45-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cb45-144">RELATED LINKS</span></span>
