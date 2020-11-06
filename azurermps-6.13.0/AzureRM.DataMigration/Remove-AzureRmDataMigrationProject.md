---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 5aada0f82b8d2a11486e3dde2f4b806f735979e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502942"
---
# <span data-ttu-id="dbb86-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="dbb86-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="dbb86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbb86-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb86-103">Entfernt ein Azure Database Migration Service-Projekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb86-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbb86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbb86-104">SYNTAX</span></span>

### <span data-ttu-id="dbb86-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbb86-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbb86-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbb86-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbb86-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbb86-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbb86-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbb86-108">DESCRIPTION</span></span>
<span data-ttu-id="dbb86-109">Das Remove-AzureRmDataMigrationProject-Cmdlet entfernt ein Azure-Datenbank-Migrationsdienst Projekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb86-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="dbb86-110">Durch die Bereitstellung des DeleteRunningTask-Parameters werden alle Azure-Datenbank-Migrationsdienst Aufgaben entfernt, die dem zu entfernenden Projekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dbb86-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="dbb86-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbb86-111">EXAMPLES</span></span>

### <span data-ttu-id="dbb86-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbb86-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="dbb86-113">Im obigen Beispiel wird das Azure Database Migration Service-Projekt namens myDMProject aus Azure basierend auf Name als Eingabeparameter entfernt</span><span class="sxs-lookup"><span data-stu-id="dbb86-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="dbb86-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dbb86-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="dbb86-115">Im obigen Beispiel wird das Azure Database Migration Service-Projekt auf Grundlage des PSProject-Objekts als Eingabeparameter entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbb86-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="dbb86-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbb86-116">PARAMETERS</span></span>

### <span data-ttu-id="dbb86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb86-117">-DefaultProfile</span></span>
<span data-ttu-id="dbb86-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbb86-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbb86-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="dbb86-119">-DeleteRunningTask</span></span>
<span data-ttu-id="dbb86-120">Löschen einer ausgeführten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="dbb86-120">Delete any running task</span></span>

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

### <span data-ttu-id="dbb86-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dbb86-121">-Force</span></span>
<span data-ttu-id="dbb86-122">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="dbb86-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dbb86-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbb86-123">-InputObject</span></span>
<span data-ttu-id="dbb86-124">PSProject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dbb86-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb86-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dbb86-125">-Name</span></span>
<span data-ttu-id="dbb86-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="dbb86-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbb86-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbb86-127">-PassThru</span></span>
<span data-ttu-id="dbb86-128">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="dbb86-128">Returns an true/false.</span></span>
<span data-ttu-id="dbb86-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="dbb86-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbb86-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb86-130">-ResourceGroupName</span></span>
<span data-ttu-id="dbb86-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbb86-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="dbb86-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dbb86-132">-ResourceId</span></span>
<span data-ttu-id="dbb86-133">Projekt Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dbb86-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="dbb86-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dbb86-134">-ServiceName</span></span>
<span data-ttu-id="dbb86-135">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="dbb86-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="dbb86-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbb86-136">-Confirm</span></span>
<span data-ttu-id="dbb86-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbb86-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbb86-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbb86-138">-WhatIf</span></span>
<span data-ttu-id="dbb86-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbb86-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbb86-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbb86-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbb86-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb86-141">CommonParameters</span></span>
<span data-ttu-id="dbb86-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb86-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb86-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb86-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb86-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbb86-144">INPUTS</span></span>

### <span data-ttu-id="dbb86-145">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="dbb86-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="dbb86-146">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dbb86-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dbb86-147">System. String</span><span class="sxs-lookup"><span data-stu-id="dbb86-147">System.String</span></span>

## <span data-ttu-id="dbb86-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbb86-148">OUTPUTS</span></span>

### <span data-ttu-id="dbb86-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbb86-149">System.Boolean</span></span>

## <span data-ttu-id="dbb86-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbb86-150">NOTES</span></span>

## <span data-ttu-id="dbb86-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbb86-151">RELATED LINKS</span></span>
