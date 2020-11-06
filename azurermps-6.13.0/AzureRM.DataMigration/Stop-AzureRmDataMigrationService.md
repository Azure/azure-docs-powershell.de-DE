---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482505"
---
# <span data-ttu-id="59ce8-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="59ce8-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="59ce8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="59ce8-103">Beendet eine Instanz des Azure-Daten Bank Migrations Diensts, die sich in einem aktiven Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="59ce8-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59ce8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59ce8-104">SYNTAX</span></span>

### <span data-ttu-id="59ce8-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59ce8-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ce8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ce8-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ce8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ce8-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ce8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="59ce8-109">Das Stop-AzureRmDataMigrationService-Cmdlet beendet eine Instanz des Azure-Daten Bank Migrations Diensts, der einen aktiven Zustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="59ce8-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="59ce8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59ce8-110">EXAMPLES</span></span>

### <span data-ttu-id="59ce8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59ce8-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="59ce8-112">Das obige Beispiel beendet eine Instanz des Azure Database Migration Service namens Test Service basierend auf dem Dienstnamen, der als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59ce8-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="59ce8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59ce8-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="59ce8-114">Im obigen Beispiel wird eine Instanz des Azure Database-Migrations Diensts auf Grundlage des PSDataMigrationService-Objekts beendet, das als Eingabeparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59ce8-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="59ce8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="59ce8-115">PARAMETERS</span></span>

### <span data-ttu-id="59ce8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ce8-116">-DefaultProfile</span></span>
<span data-ttu-id="59ce8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59ce8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59ce8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="59ce8-118">-InputObject</span></span>
<span data-ttu-id="59ce8-119">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="59ce8-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="59ce8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="59ce8-120">-Name</span></span>
<span data-ttu-id="59ce8-121">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="59ce8-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="59ce8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59ce8-122">-PassThru</span></span>
<span data-ttu-id="59ce8-123">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="59ce8-123">Returns an true/false.</span></span>
<span data-ttu-id="59ce8-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="59ce8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59ce8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ce8-125">-ResourceGroupName</span></span>
<span data-ttu-id="59ce8-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59ce8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="59ce8-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59ce8-127">-ResourceId</span></span>
<span data-ttu-id="59ce8-128">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="59ce8-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="59ce8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59ce8-129">-Confirm</span></span>
<span data-ttu-id="59ce8-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59ce8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59ce8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ce8-131">-WhatIf</span></span>
<span data-ttu-id="59ce8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59ce8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59ce8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59ce8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59ce8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ce8-134">CommonParameters</span></span>
<span data-ttu-id="59ce8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ce8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ce8-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ce8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ce8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59ce8-137">INPUTS</span></span>

### <span data-ttu-id="59ce8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="59ce8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="59ce8-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59ce8-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="59ce8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="59ce8-140">System.String</span></span>

## <span data-ttu-id="59ce8-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59ce8-141">OUTPUTS</span></span>

### <span data-ttu-id="59ce8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59ce8-142">System.Boolean</span></span>

## <span data-ttu-id="59ce8-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="59ce8-143">NOTES</span></span>

## <span data-ttu-id="59ce8-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59ce8-144">RELATED LINKS</span></span>
