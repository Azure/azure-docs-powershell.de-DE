---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298882"
---
# <span data-ttu-id="13852-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="13852-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="13852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13852-102">SYNOPSIS</span></span>
<span data-ttu-id="13852-103">Bricht einen laufenden DataBox-Auftrag ab, wenn sich der Auftrag im Status "Abbrechen" befindet.</span><span class="sxs-lookup"><span data-stu-id="13852-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="13852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13852-104">SYNTAX</span></span>

### <span data-ttu-id="13852-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="13852-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13852-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13852-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13852-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13852-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13852-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13852-108">DESCRIPTION</span></span>
<span data-ttu-id="13852-109">Das Cmdlet **Stop-AzDataBoxJob** wird verwendet, um einen DataBox-Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="13852-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="13852-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13852-110">EXAMPLES</span></span>

### <span data-ttu-id="13852-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13852-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="13852-112">Bricht den angegebenen DataBox-Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="13852-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="13852-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="13852-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="13852-114">Bricht den angegebenen DataBox-Auftrag ohne Bestätigung gewaltsam ab</span><span class="sxs-lookup"><span data-stu-id="13852-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="13852-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="13852-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="13852-116">Bricht den angegebenen DataBox-Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="13852-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="13852-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="13852-117">PARAMETERS</span></span>

### <span data-ttu-id="13852-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13852-118">-DefaultProfile</span></span>
<span data-ttu-id="13852-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13852-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13852-120">-Force</span><span class="sxs-lookup"><span data-stu-id="13852-120">-Force</span></span>
<span data-ttu-id="13852-121">Stopp ohne Bestätigung erzwingen</span><span class="sxs-lookup"><span data-stu-id="13852-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="13852-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13852-122">-InputObject</span></span>
<span data-ttu-id="13852-123">Inputobject vom Typ PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="13852-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13852-124">-Name</span><span class="sxs-lookup"><span data-stu-id="13852-124">-Name</span></span>
<span data-ttu-id="13852-125">DataBox-Auftrags Name</span><span class="sxs-lookup"><span data-stu-id="13852-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13852-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13852-126">-PassThru</span></span>
<span data-ttu-id="13852-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="13852-127">PassThru</span></span>

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

### <span data-ttu-id="13852-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="13852-128">-Reason</span></span>
<span data-ttu-id="13852-129">Grund für Stornierung</span><span class="sxs-lookup"><span data-stu-id="13852-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13852-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13852-130">-ResourceGroupName</span></span>
<span data-ttu-id="13852-131">Datenbox-Auftrags Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="13852-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13852-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="13852-132">-ResourceId</span></span>
<span data-ttu-id="13852-133">DataBox-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="13852-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13852-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13852-134">-Confirm</span></span>
<span data-ttu-id="13852-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13852-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13852-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13852-136">-WhatIf</span></span>
<span data-ttu-id="13852-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13852-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13852-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13852-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13852-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13852-139">CommonParameters</span></span>
<span data-ttu-id="13852-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13852-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13852-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13852-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13852-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13852-142">INPUTS</span></span>

### <span data-ttu-id="13852-143">System. String</span><span class="sxs-lookup"><span data-stu-id="13852-143">System.String</span></span>

## <span data-ttu-id="13852-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13852-144">OUTPUTS</span></span>

### <span data-ttu-id="13852-145">System. void</span><span class="sxs-lookup"><span data-stu-id="13852-145">System.Void</span></span>

## <span data-ttu-id="13852-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="13852-146">NOTES</span></span>

## <span data-ttu-id="13852-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13852-147">RELATED LINKS</span></span>
