---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847623"
---
# <span data-ttu-id="8ae44-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8ae44-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="8ae44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ae44-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae44-103">Bricht einen laufenden DataBox-Auftrag ab, wenn sich der Auftrag im Status "Abbrechen" befindet.</span><span class="sxs-lookup"><span data-stu-id="8ae44-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="8ae44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae44-104">SYNTAX</span></span>

### <span data-ttu-id="8ae44-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ae44-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae44-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae44-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae44-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae44-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae44-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ae44-108">DESCRIPTION</span></span>
<span data-ttu-id="8ae44-109">Das Cmdlet **Stop-AzDataBoxJob** wird verwendet, um einen DataBox-Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="8ae44-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="8ae44-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ae44-110">EXAMPLES</span></span>

### <span data-ttu-id="8ae44-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ae44-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="8ae44-112">Bricht den angegebenen DataBox-Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="8ae44-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="8ae44-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8ae44-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="8ae44-114">Bricht den angegebenen DataBox-Auftrag ohne Bestätigung gewaltsam ab</span><span class="sxs-lookup"><span data-stu-id="8ae44-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="8ae44-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8ae44-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="8ae44-116">Bricht den angegebenen DataBox-Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="8ae44-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="8ae44-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ae44-117">PARAMETERS</span></span>

### <span data-ttu-id="8ae44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae44-118">-DefaultProfile</span></span>
<span data-ttu-id="8ae44-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ae44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae44-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8ae44-120">-Force</span></span>
<span data-ttu-id="8ae44-121">Stopp ohne Bestätigung erzwingen</span><span class="sxs-lookup"><span data-stu-id="8ae44-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="8ae44-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ae44-122">-InputObject</span></span>
<span data-ttu-id="8ae44-123">Inputobject vom Typ PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8ae44-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="8ae44-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8ae44-124">-Name</span></span>
<span data-ttu-id="8ae44-125">DataBox-Auftrags Name</span><span class="sxs-lookup"><span data-stu-id="8ae44-125">Databox Job Name</span></span>

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

### <span data-ttu-id="8ae44-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ae44-126">-PassThru</span></span>
<span data-ttu-id="8ae44-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="8ae44-127">PassThru</span></span>

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

### <span data-ttu-id="8ae44-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="8ae44-128">-Reason</span></span>
<span data-ttu-id="8ae44-129">Grund für Stornierung</span><span class="sxs-lookup"><span data-stu-id="8ae44-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="8ae44-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae44-130">-ResourceGroupName</span></span>
<span data-ttu-id="8ae44-131">Datenbox-Auftrags Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8ae44-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="8ae44-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8ae44-132">-ResourceId</span></span>
<span data-ttu-id="8ae44-133">DataBox-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8ae44-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="8ae44-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ae44-134">-Confirm</span></span>
<span data-ttu-id="8ae44-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ae44-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae44-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae44-136">-WhatIf</span></span>
<span data-ttu-id="8ae44-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae44-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ae44-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ae44-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae44-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae44-139">CommonParameters</span></span>
<span data-ttu-id="8ae44-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae44-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae44-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ae44-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae44-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ae44-142">INPUTS</span></span>

### <span data-ttu-id="8ae44-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8ae44-143">System.String</span></span>

## <span data-ttu-id="8ae44-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ae44-144">OUTPUTS</span></span>

### <span data-ttu-id="8ae44-145">System. void</span><span class="sxs-lookup"><span data-stu-id="8ae44-145">System.Void</span></span>

## <span data-ttu-id="8ae44-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ae44-146">NOTES</span></span>

## <span data-ttu-id="8ae44-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ae44-147">RELATED LINKS</span></span>
