---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 2a94d74fb8c6ba6cc9f6c2873269f3009c2f7e9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661166"
---
# <span data-ttu-id="12fef-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="12fef-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="12fef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12fef-102">SYNOPSIS</span></span>
<span data-ttu-id="12fef-103">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="12fef-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="12fef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12fef-104">SYNTAX</span></span>

### <span data-ttu-id="12fef-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12fef-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fef-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fef-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fef-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fef-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fef-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12fef-108">DESCRIPTION</span></span>
<span data-ttu-id="12fef-109">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="12fef-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="12fef-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12fef-110">EXAMPLES</span></span>

### <span data-ttu-id="12fef-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12fef-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="12fef-112">Beschriften Sie eine Unterwelt-Nummer.</span><span class="sxs-lookup"><span data-stu-id="12fef-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="12fef-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="12fef-113">PARAMETERS</span></span>

### <span data-ttu-id="12fef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fef-114">-DefaultProfile</span></span>
<span data-ttu-id="12fef-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12fef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12fef-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12fef-116">-InputObject</span></span>
<span data-ttu-id="12fef-117">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="12fef-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="12fef-118">-Name</span><span class="sxs-lookup"><span data-stu-id="12fef-118">-Name</span></span>
<span data-ttu-id="12fef-119">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="12fef-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="12fef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fef-120">-ResourceGroupName</span></span>
<span data-ttu-id="12fef-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="12fef-121">Resource group name</span></span>

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

### <span data-ttu-id="12fef-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12fef-122">-ResourceId</span></span>
<span data-ttu-id="12fef-123">Die Ressourcen-ID des Informationsbereichs</span><span class="sxs-lookup"><span data-stu-id="12fef-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="12fef-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="12fef-124">-Tag</span></span>
<span data-ttu-id="12fef-125">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="12fef-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="12fef-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12fef-126">-Confirm</span></span>
<span data-ttu-id="12fef-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12fef-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fef-128">-WhatIf</span></span>
<span data-ttu-id="12fef-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12fef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fef-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12fef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fef-131">CommonParameters</span></span>
<span data-ttu-id="12fef-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fef-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fef-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12fef-134">INPUTS</span></span>

### <span data-ttu-id="12fef-135">System. String</span><span class="sxs-lookup"><span data-stu-id="12fef-135">System.String</span></span>

### <span data-ttu-id="12fef-136">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="12fef-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="12fef-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12fef-137">OUTPUTS</span></span>

### <span data-ttu-id="12fef-138">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="12fef-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="12fef-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="12fef-139">NOTES</span></span>

## <span data-ttu-id="12fef-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12fef-140">RELATED LINKS</span></span>
