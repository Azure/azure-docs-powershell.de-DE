---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152868"
---
# <span data-ttu-id="411ac-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="411ac-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="411ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="411ac-102">SYNOPSIS</span></span>
<span data-ttu-id="411ac-103">Löschen einer Route in IoT Hub</span><span class="sxs-lookup"><span data-stu-id="411ac-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="411ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="411ac-104">SYNTAX</span></span>

### <span data-ttu-id="411ac-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="411ac-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="411ac-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="411ac-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="411ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="411ac-108">DESCRIPTION</span></span>
<span data-ttu-id="411ac-109">Löschen von Routen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="411ac-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="411ac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="411ac-110">EXAMPLES</span></span>

### <span data-ttu-id="411ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="411ac-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="411ac-112">Löschen Sie die Route "R1" aus "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="411ac-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="411ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="411ac-113">PARAMETERS</span></span>

### <span data-ttu-id="411ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411ac-114">-DefaultProfile</span></span>
<span data-ttu-id="411ac-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="411ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="411ac-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="411ac-116">-InputObject</span></span>
<span data-ttu-id="411ac-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="411ac-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="411ac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="411ac-118">-Name</span></span>
<span data-ttu-id="411ac-119">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="411ac-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="411ac-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="411ac-120">-PassThru</span></span>
<span data-ttu-id="411ac-121">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="411ac-121">Allows to return the boolean object.</span></span> <span data-ttu-id="411ac-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="411ac-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="411ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="411ac-124">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="411ac-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="411ac-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="411ac-125">-ResourceId</span></span>
<span data-ttu-id="411ac-126">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="411ac-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="411ac-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="411ac-127">-RouteName</span></span>
<span data-ttu-id="411ac-128">Name der Route</span><span class="sxs-lookup"><span data-stu-id="411ac-128">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="411ac-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="411ac-129">-Confirm</span></span>
<span data-ttu-id="411ac-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="411ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411ac-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="411ac-131">-WhatIf</span></span>
<span data-ttu-id="411ac-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="411ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="411ac-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="411ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411ac-134">CommonParameters</span></span>
<span data-ttu-id="411ac-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="411ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411ac-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="411ac-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411ac-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="411ac-137">INPUTS</span></span>

### <span data-ttu-id="411ac-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="411ac-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="411ac-139">System.String</span><span class="sxs-lookup"><span data-stu-id="411ac-139">System.String</span></span>

## <span data-ttu-id="411ac-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="411ac-140">OUTPUTS</span></span>

### <span data-ttu-id="411ac-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="411ac-141">System.Boolean</span></span>

## <span data-ttu-id="411ac-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="411ac-142">NOTES</span></span>

## <span data-ttu-id="411ac-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="411ac-143">RELATED LINKS</span></span>
