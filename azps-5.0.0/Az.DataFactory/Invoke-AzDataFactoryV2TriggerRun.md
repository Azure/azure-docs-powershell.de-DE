---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298456"
---
# <span data-ttu-id="37796-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="37796-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="37796-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37796-102">SYNOPSIS</span></span>
 <span data-ttu-id="37796-103">Ruft eine andere Instanz einer Trigger-Ausführung auf.</span><span class="sxs-lookup"><span data-stu-id="37796-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="37796-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37796-104">SYNTAX</span></span>

### <span data-ttu-id="37796-105">ByFactoryNameByParameterFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="37796-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37796-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37796-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37796-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="37796-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37796-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37796-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37796-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37796-109">DESCRIPTION</span></span>
<span data-ttu-id="37796-110">Der Befehl **Invoke-AzDataFactoryV2TriggerRun** startet eine andere Instanz eines Triggers, der mit einer neuen Trigger-Lauf-ID ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37796-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="37796-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37796-111">EXAMPLES</span></span>

### <span data-ttu-id="37796-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37796-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="37796-113">Startet eine andere Instanz eines Triggers, der mit einer neuen Trigger-Lauf-ID ausgeführt wird, wobei dieselbe windowStartTime und windowEndTime wie der ursprüngliche Trigger ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37796-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="37796-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="37796-114">PARAMETERS</span></span>

### <span data-ttu-id="37796-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="37796-115">-DataFactory</span></span>
<span data-ttu-id="37796-116">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="37796-116">The data factory object.</span></span>

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

### <span data-ttu-id="37796-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="37796-117">-DataFactoryName</span></span>
<span data-ttu-id="37796-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="37796-118">The data factory name.</span></span>

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

### <span data-ttu-id="37796-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37796-119">-DefaultProfile</span></span>
<span data-ttu-id="37796-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37796-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37796-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37796-121">-InputObject</span></span>
<span data-ttu-id="37796-122">Die Informationen zum Trigger werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37796-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="37796-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37796-123">-PassThru</span></span>
<span data-ttu-id="37796-124">Wenn angegeben, schreibt das Cmdlet true, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="37796-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="37796-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37796-125">-ResourceGroupName</span></span>
<span data-ttu-id="37796-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37796-126">The resource group name.</span></span>

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

### <span data-ttu-id="37796-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="37796-127">-TriggerName</span></span>
<span data-ttu-id="37796-128">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="37796-128">The trigger name.</span></span>

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

### <span data-ttu-id="37796-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="37796-129">-TriggerRunId</span></span>
<span data-ttu-id="37796-130">Die Ausführungs-ID des Triggers.</span><span class="sxs-lookup"><span data-stu-id="37796-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="37796-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37796-131">-Confirm</span></span>
<span data-ttu-id="37796-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37796-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37796-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37796-133">-WhatIf</span></span>
<span data-ttu-id="37796-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37796-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37796-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37796-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37796-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37796-136">CommonParameters</span></span>
<span data-ttu-id="37796-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37796-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37796-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37796-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37796-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37796-139">INPUTS</span></span>

### <span data-ttu-id="37796-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="37796-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="37796-141">System. String</span><span class="sxs-lookup"><span data-stu-id="37796-141">System.String</span></span>

### <span data-ttu-id="37796-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="37796-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="37796-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37796-143">OUTPUTS</span></span>

### <span data-ttu-id="37796-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="37796-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="37796-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="37796-145">NOTES</span></span>

## <span data-ttu-id="37796-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37796-146">RELATED LINKS</span></span>
