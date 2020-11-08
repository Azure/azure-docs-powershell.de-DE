---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172997"
---
# <span data-ttu-id="3fa82-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3fa82-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="3fa82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fa82-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa82-103">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3fa82-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="3fa82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fa82-104">SYNTAX</span></span>

### <span data-ttu-id="3fa82-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fa82-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa82-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa82-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa82-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa82-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fa82-108">DESCRIPTION</span></span>
<span data-ttu-id="3fa82-109">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3fa82-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="3fa82-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fa82-110">EXAMPLES</span></span>

### <span data-ttu-id="3fa82-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fa82-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3fa82-112">Kennzeichnen Sie einen Unterkategorien-Controller.</span><span class="sxs-lookup"><span data-stu-id="3fa82-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="3fa82-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa82-113">PARAMETERS</span></span>

### <span data-ttu-id="3fa82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa82-114">-DefaultProfile</span></span>
<span data-ttu-id="3fa82-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fa82-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa82-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fa82-116">-InputObject</span></span>
<span data-ttu-id="3fa82-117">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3fa82-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fa82-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3fa82-118">-Name</span></span>
<span data-ttu-id="3fa82-119">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="3fa82-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="3fa82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa82-120">-ResourceGroupName</span></span>
<span data-ttu-id="3fa82-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3fa82-121">Resource group name</span></span>

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

### <span data-ttu-id="3fa82-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3fa82-122">-ResourceId</span></span>
<span data-ttu-id="3fa82-123">Die Ressourcen-ID des Informationsbereichs</span><span class="sxs-lookup"><span data-stu-id="3fa82-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="3fa82-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fa82-124">-Tag</span></span>
<span data-ttu-id="3fa82-125">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fa82-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa82-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fa82-126">-Confirm</span></span>
<span data-ttu-id="3fa82-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fa82-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa82-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa82-128">-WhatIf</span></span>
<span data-ttu-id="3fa82-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fa82-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa82-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fa82-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa82-131">CommonParameters</span></span>
<span data-ttu-id="3fa82-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa82-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa82-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa82-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fa82-134">INPUTS</span></span>

### <span data-ttu-id="3fa82-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3fa82-135">System.String</span></span>

### <span data-ttu-id="3fa82-136">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="3fa82-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3fa82-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fa82-137">OUTPUTS</span></span>

### <span data-ttu-id="3fa82-138">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="3fa82-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3fa82-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fa82-139">NOTES</span></span>

## <span data-ttu-id="3fa82-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fa82-140">RELATED LINKS</span></span>
