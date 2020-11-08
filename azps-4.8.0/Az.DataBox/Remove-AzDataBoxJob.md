---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173066"
---
# <span data-ttu-id="b1685-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="b1685-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="b1685-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1685-102">SYNOPSIS</span></span>
<span data-ttu-id="b1685-103">Löscht den DataBox-Auftrag</span><span class="sxs-lookup"><span data-stu-id="b1685-103">Deletes the databox job</span></span>

## <span data-ttu-id="b1685-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1685-104">SYNTAX</span></span>

### <span data-ttu-id="b1685-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1685-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1685-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1685-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1685-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1685-108">DESCRIPTION</span></span>
<span data-ttu-id="b1685-109">Das Cmdlet **Remove-AzDataBoxJob** wird verwendet, um einen fertigen DataBox-Auftrag aus der Liste der DataBox-Aufträge zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b1685-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="b1685-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1685-110">EXAMPLES</span></span>

### <span data-ttu-id="b1685-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1685-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="b1685-112">Löscht den angegebenen DataBox-Auftrag</span><span class="sxs-lookup"><span data-stu-id="b1685-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="b1685-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b1685-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="b1685-114">Löschen des angegebenen DataBox-Auftrags ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="b1685-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="b1685-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b1685-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="b1685-116">Löscht den angegebenen DataBox-Auftrag</span><span class="sxs-lookup"><span data-stu-id="b1685-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="b1685-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1685-117">PARAMETERS</span></span>

### <span data-ttu-id="b1685-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1685-118">-DefaultProfile</span></span>
<span data-ttu-id="b1685-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1685-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1685-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b1685-120">-Force</span></span>
<span data-ttu-id="b1685-121">Entfernen ohne Bestätigung erzwingen</span><span class="sxs-lookup"><span data-stu-id="b1685-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="b1685-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1685-122">-InputObject</span></span>
<span data-ttu-id="b1685-123">Inputobject vom Typ PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="b1685-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="b1685-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b1685-124">-Name</span></span>
<span data-ttu-id="b1685-125">DataBox-Auftrags Name</span><span class="sxs-lookup"><span data-stu-id="b1685-125">Databox Job Name</span></span>

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

### <span data-ttu-id="b1685-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1685-126">-PassThru</span></span>
<span data-ttu-id="b1685-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="b1685-127">PassThru</span></span>

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

### <span data-ttu-id="b1685-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1685-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1685-129">Datenbox-Auftrags Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b1685-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="b1685-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b1685-130">-ResourceId</span></span>
<span data-ttu-id="b1685-131">DataBox-Auftrags Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b1685-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="b1685-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1685-132">-Confirm</span></span>
<span data-ttu-id="b1685-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1685-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1685-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1685-134">-WhatIf</span></span>
<span data-ttu-id="b1685-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1685-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1685-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1685-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1685-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1685-137">CommonParameters</span></span>
<span data-ttu-id="b1685-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1685-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1685-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1685-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1685-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1685-140">INPUTS</span></span>

### <span data-ttu-id="b1685-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b1685-141">System.String</span></span>

## <span data-ttu-id="b1685-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1685-142">OUTPUTS</span></span>

### <span data-ttu-id="b1685-143">System. void</span><span class="sxs-lookup"><span data-stu-id="b1685-143">System.Void</span></span>

## <span data-ttu-id="b1685-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1685-144">NOTES</span></span>

## <span data-ttu-id="b1685-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1685-145">RELATED LINKS</span></span>
