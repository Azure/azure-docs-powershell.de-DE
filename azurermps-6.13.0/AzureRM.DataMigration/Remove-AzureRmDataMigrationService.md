---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502945"
---
# <span data-ttu-id="a0f51-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a0f51-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="a0f51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0f51-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f51-103">Entfernt eine Instanz des Azure Database Migration Service aus Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f51-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0f51-104">SYNTAX</span></span>

### <span data-ttu-id="a0f51-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0f51-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f51-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f51-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f51-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0f51-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f51-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0f51-108">DESCRIPTION</span></span>
<span data-ttu-id="a0f51-109">Das Remove-AzureRmDataMigrationService-Cmdlet entfernt eine Instanz des Azure Database Migration Service aus Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f51-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="a0f51-110">Durch die Bereitstellung des DeleteRunningTask-Parameters werden alle Azure-Daten Bank Migrationsdienst Aufgaben entfernt, die dem zu entfernenden Dienst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0f51-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="a0f51-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0f51-111">EXAMPLES</span></span>

### <span data-ttu-id="a0f51-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0f51-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="a0f51-113">Im obigen Beispiel wird eine Instanz des Azure Database Migration Service mit dem Namen Test Service entfernt, die in einer Azure-Ressourcengruppe mit dem Namen myresourcegroup enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a0f51-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="a0f51-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0f51-114">PARAMETERS</span></span>

### <span data-ttu-id="a0f51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f51-115">-DefaultProfile</span></span>
<span data-ttu-id="a0f51-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0f51-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f51-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="a0f51-117">-DeleteRunningTask</span></span>
<span data-ttu-id="a0f51-118">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a0f51-118">Delete any running task</span></span>

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

### <span data-ttu-id="a0f51-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a0f51-119">-Force</span></span>
<span data-ttu-id="a0f51-120">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="a0f51-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a0f51-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0f51-121">-InputObject</span></span>
<span data-ttu-id="a0f51-122">PSDataMigrationService-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a0f51-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="a0f51-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a0f51-123">-Name</span></span>
<span data-ttu-id="a0f51-124">Der Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="a0f51-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="a0f51-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0f51-125">-PassThru</span></span>
<span data-ttu-id="a0f51-126">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="a0f51-126">Returns an true/false.</span></span>
<span data-ttu-id="a0f51-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a0f51-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0f51-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f51-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0f51-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0f51-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0f51-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0f51-130">-ResourceId</span></span>
<span data-ttu-id="a0f51-131">DataMigrationService-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a0f51-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="a0f51-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0f51-132">-Confirm</span></span>
<span data-ttu-id="a0f51-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0f51-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f51-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f51-134">-WhatIf</span></span>
<span data-ttu-id="a0f51-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f51-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f51-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0f51-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f51-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f51-137">CommonParameters</span></span>
<span data-ttu-id="a0f51-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f51-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f51-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f51-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f51-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0f51-140">INPUTS</span></span>

### <span data-ttu-id="a0f51-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a0f51-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="a0f51-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0f51-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a0f51-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f51-143">System.String</span></span>

## <span data-ttu-id="a0f51-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0f51-144">OUTPUTS</span></span>

### <span data-ttu-id="a0f51-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0f51-145">System.Boolean</span></span>

## <span data-ttu-id="a0f51-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0f51-146">NOTES</span></span>

## <span data-ttu-id="a0f51-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0f51-147">RELATED LINKS</span></span>
