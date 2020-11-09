---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297580"
---
# <span data-ttu-id="117c4-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="117c4-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="117c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="117c4-102">SYNOPSIS</span></span>
<span data-ttu-id="117c4-103">Beendet eine Azure-Datenbank-Migrationsdienst Aufgabe, die sich in einem aktiven Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="117c4-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="117c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="117c4-104">SYNTAX</span></span>

### <span data-ttu-id="117c4-105">ComponentNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="117c4-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="117c4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="117c4-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="117c4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="117c4-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="117c4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="117c4-108">DESCRIPTION</span></span>
<span data-ttu-id="117c4-109">Stop-AzDataMigrationTask-Cmdlet beendet die Daten Bank Migrations Aktivität im aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="117c4-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="117c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="117c4-110">EXAMPLES</span></span>

### <span data-ttu-id="117c4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="117c4-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="117c4-112">Im obigen Beispiel wird die Azure-Daten Bank Migrationsdienst Aufgabe mit dem Namen "myDMSTask" beendet, die mit Project myDMSProject und Azure Database Migration Service Instance namens Test Service verbunden ist</span><span class="sxs-lookup"><span data-stu-id="117c4-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="117c4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="117c4-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="117c4-114">Im obigen Beispiel wird die Azure-Daten Bank Migrationsdienst Aufgabe als Eingabeparameter PSProjectTask-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="117c4-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="117c4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="117c4-115">PARAMETERS</span></span>

### <span data-ttu-id="117c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117c4-116">-DefaultProfile</span></span>
<span data-ttu-id="117c4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="117c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117c4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="117c4-118">-InputObject</span></span>
<span data-ttu-id="117c4-119">PSProjectTask-Objekt.</span><span class="sxs-lookup"><span data-stu-id="117c4-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="117c4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="117c4-120">-Name</span></span>
<span data-ttu-id="117c4-121">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="117c4-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117c4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="117c4-122">-PassThru</span></span>
<span data-ttu-id="117c4-123">Gibt einen Wert vom Wert true/false zurück.</span><span class="sxs-lookup"><span data-stu-id="117c4-123">Returns an true/false.</span></span>
<span data-ttu-id="117c4-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="117c4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="117c4-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="117c4-125">-ProjectName</span></span>
<span data-ttu-id="117c4-126">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="117c4-126">The name of the project.</span></span>

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

### <span data-ttu-id="117c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="117c4-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="117c4-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="117c4-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="117c4-129">-ResourceId</span></span>
<span data-ttu-id="117c4-130">ProjectTask-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="117c4-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="117c4-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="117c4-131">-ServiceName</span></span>
<span data-ttu-id="117c4-132">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="117c4-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="117c4-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="117c4-133">-Confirm</span></span>
<span data-ttu-id="117c4-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="117c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117c4-135">-WhatIf</span></span>
<span data-ttu-id="117c4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="117c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="117c4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="117c4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117c4-138">CommonParameters</span></span>
<span data-ttu-id="117c4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117c4-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117c4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117c4-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="117c4-141">INPUTS</span></span>

### <span data-ttu-id="117c4-142">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="117c4-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="117c4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="117c4-143">System.String</span></span>

## <span data-ttu-id="117c4-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="117c4-144">OUTPUTS</span></span>

### <span data-ttu-id="117c4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="117c4-145">System.Boolean</span></span>

## <span data-ttu-id="117c4-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="117c4-146">NOTES</span></span>

## <span data-ttu-id="117c4-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="117c4-147">RELATED LINKS</span></span>
