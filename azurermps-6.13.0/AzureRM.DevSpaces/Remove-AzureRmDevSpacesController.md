---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664341"
---
# <span data-ttu-id="f516f-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="f516f-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="f516f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f516f-102">SYNOPSIS</span></span>
<span data-ttu-id="f516f-103">Löschen Sie einen "ein"-Controller.</span><span class="sxs-lookup"><span data-stu-id="f516f-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f516f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f516f-104">SYNTAX</span></span>

### <span data-ttu-id="f516f-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f516f-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f516f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f516f-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f516f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f516f-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f516f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f516f-108">DESCRIPTION</span></span>
<span data-ttu-id="f516f-109">Löschen Sie einen "ein"-Controller.</span><span class="sxs-lookup"><span data-stu-id="f516f-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="f516f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f516f-110">EXAMPLES</span></span>

### <span data-ttu-id="f516f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f516f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="f516f-112">Löschen Sie einen Untertitel-Controller mit dem Namen devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="f516f-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="f516f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f516f-113">PARAMETERS</span></span>

### <span data-ttu-id="f516f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f516f-114">-AsJob</span></span>
<span data-ttu-id="f516f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f516f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f516f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f516f-116">-DefaultProfile</span></span>
<span data-ttu-id="f516f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f516f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f516f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f516f-118">-InputObject</span></span>
<span data-ttu-id="f516f-119">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f516f-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f516f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f516f-120">-Name</span></span>
<span data-ttu-id="f516f-121">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="f516f-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="f516f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f516f-122">-PassThru</span></span>
<span data-ttu-id="f516f-123">Gibt WAHR zurück, wenn DELETE erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="f516f-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="f516f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f516f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f516f-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f516f-125">Resource group name</span></span>

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

### <span data-ttu-id="f516f-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f516f-126">-ResourceId</span></span>
<span data-ttu-id="f516f-127">Die Ressourcen-ID des Informationsbereichs</span><span class="sxs-lookup"><span data-stu-id="f516f-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="f516f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f516f-128">-Confirm</span></span>
<span data-ttu-id="f516f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f516f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f516f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f516f-130">-WhatIf</span></span>
<span data-ttu-id="f516f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f516f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f516f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f516f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f516f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f516f-133">CommonParameters</span></span>
<span data-ttu-id="f516f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f516f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f516f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f516f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f516f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f516f-136">INPUTS</span></span>

### <span data-ttu-id="f516f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f516f-137">System.String</span></span>

### <span data-ttu-id="f516f-138">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="f516f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="f516f-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f516f-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f516f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f516f-140">OUTPUTS</span></span>

### <span data-ttu-id="f516f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f516f-141">System.Boolean</span></span>

## <span data-ttu-id="f516f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f516f-142">NOTES</span></span>

## <span data-ttu-id="f516f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f516f-143">RELATED LINKS</span></span>
