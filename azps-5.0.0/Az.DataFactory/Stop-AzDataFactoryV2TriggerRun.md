---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298180"
---
# <span data-ttu-id="af813-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="af813-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="af813-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af813-102">SYNOPSIS</span></span>
<span data-ttu-id="af813-103">Beendet einen Trigger, der in einer Data Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af813-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="af813-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af813-104">SYNTAX</span></span>

### <span data-ttu-id="af813-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="af813-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af813-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af813-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af813-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="af813-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af813-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af813-108">DESCRIPTION</span></span>
<span data-ttu-id="af813-109">Das Cmdlet **Stop-AzDataFactoryV2TriggerRun** beendet einen Trigger, der in einer mit dem Triggernamen und der Trigger Run-ID angegebenen Daten Factory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af813-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="af813-110">Wird derzeit nur für TumblingWindowTriggers im WaitingOnDependency-Zustand unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af813-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="af813-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af813-111">EXAMPLES</span></span>

### <span data-ttu-id="af813-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af813-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="af813-113">Dieser Befehl beendet den Trigger, der mit der ID ' 08586002468005888497807248799CU16 ' im Factory-WikiADF ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af813-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="af813-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="af813-114">PARAMETERS</span></span>

### <span data-ttu-id="af813-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="af813-115">-DataFactory</span></span>
<span data-ttu-id="af813-116">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af813-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="af813-117">-DataFactoryName</span></span>
<span data-ttu-id="af813-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="af813-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af813-119">-DefaultProfile</span></span>
<span data-ttu-id="af813-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af813-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af813-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="af813-121">-InputObject</span></span>
<span data-ttu-id="af813-122">Die Informationen zum Trigger werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af813-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af813-123">-PassThru</span></span>
<span data-ttu-id="af813-124">Wenn angegeben, schreibt das Cmdlet true, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="af813-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="af813-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af813-125">-ResourceGroupName</span></span>
<span data-ttu-id="af813-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="af813-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="af813-127">-TriggerName</span></span>
<span data-ttu-id="af813-128">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="af813-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="af813-129">-TriggerRunId</span></span>
<span data-ttu-id="af813-130">Die Ausführungs-ID des Triggers.</span><span class="sxs-lookup"><span data-stu-id="af813-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af813-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af813-131">-Confirm</span></span>
<span data-ttu-id="af813-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af813-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af813-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af813-133">-WhatIf</span></span>
<span data-ttu-id="af813-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af813-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af813-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af813-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af813-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af813-136">CommonParameters</span></span>
<span data-ttu-id="af813-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af813-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af813-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af813-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af813-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af813-139">INPUTS</span></span>

### <span data-ttu-id="af813-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="af813-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="af813-141">System. String</span><span class="sxs-lookup"><span data-stu-id="af813-141">System.String</span></span>

### <span data-ttu-id="af813-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="af813-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="af813-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af813-143">OUTPUTS</span></span>

### <span data-ttu-id="af813-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af813-144">System.Boolean</span></span>

## <span data-ttu-id="af813-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="af813-145">NOTES</span></span>

## <span data-ttu-id="af813-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af813-146">RELATED LINKS</span></span>
