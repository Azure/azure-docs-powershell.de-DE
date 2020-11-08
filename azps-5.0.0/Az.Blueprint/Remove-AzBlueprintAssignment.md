---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176303"
---
# <span data-ttu-id="0907b-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0907b-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="0907b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0907b-102">SYNOPSIS</span></span>
<span data-ttu-id="0907b-103">Entfernen einer Blueprint-Aufgabe aus einem Abonnement oder einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0907b-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="0907b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0907b-104">SYNTAX</span></span>

### <span data-ttu-id="0907b-105">BySubscriptionAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0907b-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0907b-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0907b-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0907b-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="0907b-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0907b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0907b-108">DESCRIPTION</span></span>
<span data-ttu-id="0907b-109">Entfernen eines Blueprints, der einem Abonnement zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0907b-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="0907b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0907b-110">EXAMPLES</span></span>

### <span data-ttu-id="0907b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0907b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="0907b-112">Entfernen Sie die durch den Namen angegebene Blueprint-Aufgabe aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0907b-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="0907b-113">Das Cmdlet fordert zur Bestätigung auf, bevor der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0907b-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="0907b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0907b-114">PARAMETERS</span></span>

### <span data-ttu-id="0907b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0907b-115">-DefaultProfile</span></span>
<span data-ttu-id="0907b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0907b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0907b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0907b-117">-InputObject</span></span>
<span data-ttu-id="0907b-118">Blueprint-Zuordnungsobjekt</span><span class="sxs-lookup"><span data-stu-id="0907b-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0907b-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0907b-119">-ManagementGroupId</span></span>
<span data-ttu-id="0907b-120">Die ID der Verwaltungsgruppe, in der die Blueprint-Zuordnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0907b-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0907b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0907b-121">-Name</span></span>
<span data-ttu-id="0907b-122">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="0907b-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0907b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0907b-123">-PassThru</span></span>
<span data-ttu-id="0907b-124">Wenn diese Einstellung eingestellt ist, gibt das Cmdlet ein Objekt zurück, das die entfernte Blueprint-Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="0907b-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="0907b-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0907b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0907b-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0907b-126">-SubscriptionId</span></span>
<span data-ttu-id="0907b-127">Die Abonnement-ID, in der die Blueprint-Aufgabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0907b-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0907b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0907b-128">-Confirm</span></span>
<span data-ttu-id="0907b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0907b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0907b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0907b-130">-WhatIf</span></span>
<span data-ttu-id="0907b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0907b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0907b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0907b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0907b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0907b-133">CommonParameters</span></span>
<span data-ttu-id="0907b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0907b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0907b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0907b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0907b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0907b-136">INPUTS</span></span>

### <span data-ttu-id="0907b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0907b-137">System.String</span></span>

### <span data-ttu-id="0907b-138">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="0907b-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="0907b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0907b-139">OUTPUTS</span></span>

### <span data-ttu-id="0907b-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="0907b-140">System.Object</span></span>
## <span data-ttu-id="0907b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0907b-141">NOTES</span></span>

## <span data-ttu-id="0907b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0907b-142">RELATED LINKS</span></span>
