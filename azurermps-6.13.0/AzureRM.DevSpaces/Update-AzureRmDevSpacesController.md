---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664338"
---
# <span data-ttu-id="c3320-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="c3320-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="c3320-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3320-102">SYNOPSIS</span></span>
<span data-ttu-id="c3320-103">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c3320-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3320-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3320-104">SYNTAX</span></span>

### <span data-ttu-id="c3320-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3320-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3320-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3320-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3320-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3320-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3320-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3320-108">DESCRIPTION</span></span>
<span data-ttu-id="c3320-109">Aktualisieren Sie den Daten-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c3320-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="c3320-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3320-110">EXAMPLES</span></span>

### <span data-ttu-id="c3320-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3320-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="c3320-112">Beschriften Sie eine Unterwelt-Nummer.</span><span class="sxs-lookup"><span data-stu-id="c3320-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="c3320-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3320-113">PARAMETERS</span></span>

### <span data-ttu-id="c3320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3320-114">-DefaultProfile</span></span>
<span data-ttu-id="c3320-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3320-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3320-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3320-116">-InputObject</span></span>
<span data-ttu-id="c3320-117">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3320-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3320-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c3320-118">-Name</span></span>
<span data-ttu-id="c3320-119">Name des Domänencontrollers</span><span class="sxs-lookup"><span data-stu-id="c3320-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="c3320-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3320-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3320-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c3320-121">Resource group name</span></span>

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

### <span data-ttu-id="c3320-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3320-122">-ResourceId</span></span>
<span data-ttu-id="c3320-123">Die Ressourcen-ID des Informationsbereichs</span><span class="sxs-lookup"><span data-stu-id="c3320-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="c3320-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3320-124">-Tag</span></span>
<span data-ttu-id="c3320-125">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3320-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="c3320-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3320-126">-Confirm</span></span>
<span data-ttu-id="c3320-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3320-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3320-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3320-128">-WhatIf</span></span>
<span data-ttu-id="c3320-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3320-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3320-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3320-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3320-131">CommonParameters</span></span>
<span data-ttu-id="c3320-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3320-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3320-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3320-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3320-134">INPUTS</span></span>

### <span data-ttu-id="c3320-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c3320-135">System.String</span></span>

### <span data-ttu-id="c3320-136">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="c3320-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="c3320-137">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3320-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c3320-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3320-138">OUTPUTS</span></span>

### <span data-ttu-id="c3320-139">Microsoft. Azure. Commands .Bereiche. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="c3320-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="c3320-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3320-140">NOTES</span></span>

## <span data-ttu-id="c3320-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3320-141">RELATED LINKS</span></span>
