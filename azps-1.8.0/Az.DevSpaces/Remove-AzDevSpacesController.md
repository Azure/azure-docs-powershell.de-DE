---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: b6fb42ccafe5b70316ea29251a87b76ea65dda7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661167"
---
# <span data-ttu-id="fa515-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="fa515-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="fa515-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa515-102">SYNOPSIS</span></span>
<span data-ttu-id="fa515-103">Löschen Sie einen "ein"-Controller.</span><span class="sxs-lookup"><span data-stu-id="fa515-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="fa515-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa515-104">SYNTAX</span></span>

### <span data-ttu-id="fa515-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa515-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa515-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa515-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa515-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa515-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa515-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa515-108">DESCRIPTION</span></span>
<span data-ttu-id="fa515-109">Löschen Sie einen "ein"-Controller.</span><span class="sxs-lookup"><span data-stu-id="fa515-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="fa515-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa515-110">EXAMPLES</span></span>

### <span data-ttu-id="fa515-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa515-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="fa515-112">Löschen Sie einen Untertitel-Controller mit dem Namen devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="fa515-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="fa515-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa515-113">PARAMETERS</span></span>

### <span data-ttu-id="fa515-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa515-114">-AsJob</span></span>
<span data-ttu-id="fa515-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa515-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa515-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa515-116">-DefaultProfile</span></span>
<span data-ttu-id="fa515-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa515-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa515-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa515-118">-InputObject</span></span>
<span data-ttu-id="fa515-119">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa515-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa515-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fa515-120">-Name</span></span>
<span data-ttu-id="fa515-121">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="fa515-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa515-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa515-122">-PassThru</span></span>
<span data-ttu-id="fa515-123">Gibt WAHR zurück, wenn DELETE erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="fa515-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="fa515-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa515-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa515-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fa515-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa515-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fa515-126">-ResourceId</span></span>
<span data-ttu-id="fa515-127">Die Ressourcen-ID des Informationsbereichs</span><span class="sxs-lookup"><span data-stu-id="fa515-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa515-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa515-128">-Confirm</span></span>
<span data-ttu-id="fa515-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa515-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa515-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa515-130">-WhatIf</span></span>
<span data-ttu-id="fa515-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa515-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa515-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa515-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa515-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa515-133">CommonParameters</span></span>
<span data-ttu-id="fa515-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa515-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa515-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa515-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa515-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa515-136">INPUTS</span></span>

### <span data-ttu-id="fa515-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fa515-137">System.String</span></span>

### <span data-ttu-id="fa515-138">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="fa515-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="fa515-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa515-139">OUTPUTS</span></span>

### <span data-ttu-id="fa515-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa515-140">System.Boolean</span></span>

## <span data-ttu-id="fa515-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa515-141">NOTES</span></span>

## <span data-ttu-id="fa515-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa515-142">RELATED LINKS</span></span>
