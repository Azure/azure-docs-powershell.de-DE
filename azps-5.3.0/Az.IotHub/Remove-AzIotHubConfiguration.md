---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386741"
---
# <span data-ttu-id="fcfdd-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcfdd-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="fcfdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfdd-103">Löschen sie eine IoT-Gerätekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="fcfdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcfdd-104">SYNTAX</span></span>

### <span data-ttu-id="fcfdd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcfdd-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfdd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fcfdd-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfdd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fcfdd-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcfdd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcfdd-108">DESCRIPTION</span></span>
<span data-ttu-id="fcfdd-109">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="fcfdd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcfdd-110">EXAMPLES</span></span>

### <span data-ttu-id="fcfdd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcfdd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="fcfdd-112">Löschen sie eine IoT-Gerätekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="fcfdd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcfdd-113">PARAMETERS</span></span>

### <span data-ttu-id="fcfdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfdd-114">-DefaultProfile</span></span>
<span data-ttu-id="fcfdd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcfdd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcfdd-116">-InputObject</span></span>
<span data-ttu-id="fcfdd-117">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="fcfdd-117">IotHub object</span></span>

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

### <span data-ttu-id="fcfdd-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fcfdd-118">-IotHubName</span></span>
<span data-ttu-id="fcfdd-119">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="fcfdd-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fcfdd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fcfdd-120">-Name</span></span>
<span data-ttu-id="fcfdd-121">Id für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="fcfdd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcfdd-122">-PassThru</span></span>
<span data-ttu-id="fcfdd-123">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="fcfdd-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcfdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcfdd-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fcfdd-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fcfdd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcfdd-127">-ResourceId</span></span>
<span data-ttu-id="fcfdd-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fcfdd-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fcfdd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcfdd-129">-Confirm</span></span>
<span data-ttu-id="fcfdd-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfdd-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fcfdd-131">-WhatIf</span></span>
<span data-ttu-id="fcfdd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcfdd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcfdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfdd-134">CommonParameters</span></span>
<span data-ttu-id="fcfdd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfdd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfdd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfdd-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcfdd-137">INPUTS</span></span>

### <span data-ttu-id="fcfdd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fcfdd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fcfdd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fcfdd-139">System.String</span></span>

## <span data-ttu-id="fcfdd-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcfdd-140">OUTPUTS</span></span>

### <span data-ttu-id="fcfdd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcfdd-141">System.Boolean</span></span>

## <span data-ttu-id="fcfdd-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcfdd-142">NOTES</span></span>

## <span data-ttu-id="fcfdd-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcfdd-143">RELATED LINKS</span></span>
