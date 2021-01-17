---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386657"
---
# <span data-ttu-id="3ca56-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3ca56-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="3ca56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca56-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca56-103">Löschen Sie Module auf einem Ziel-IoT-Gerät in einem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="3ca56-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="3ca56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ca56-104">SYNTAX</span></span>

### <span data-ttu-id="3ca56-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ca56-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca56-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ca56-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca56-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ca56-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca56-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ca56-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca56-109">Löschen Sie Module auf einem Ziel-IoT-Gerät in einem IoT-Hub.</span><span class="sxs-lookup"><span data-stu-id="3ca56-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="3ca56-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ca56-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca56-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ca56-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="3ca56-112">Löschen Sie ein Iot-Gerätemodul.</span><span class="sxs-lookup"><span data-stu-id="3ca56-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="3ca56-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3ca56-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="3ca56-114">Löschen Sie alle Iot-Gerätemodule.</span><span class="sxs-lookup"><span data-stu-id="3ca56-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="3ca56-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ca56-115">PARAMETERS</span></span>

### <span data-ttu-id="3ca56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca56-116">-DefaultProfile</span></span>
<span data-ttu-id="3ca56-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca56-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3ca56-118">-DeviceId</span></span>
<span data-ttu-id="3ca56-119">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="3ca56-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca56-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca56-120">-InputObject</span></span>
<span data-ttu-id="3ca56-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="3ca56-121">IotHub object</span></span>

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

### <span data-ttu-id="3ca56-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3ca56-122">-IotHubName</span></span>
<span data-ttu-id="3ca56-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="3ca56-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3ca56-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="3ca56-124">-ModuleId</span></span>
<span data-ttu-id="3ca56-125">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="3ca56-125">Target Module Id.</span></span>

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

### <span data-ttu-id="3ca56-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca56-126">-PassThru</span></span>
<span data-ttu-id="3ca56-127">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ca56-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="3ca56-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3ca56-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3ca56-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca56-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ca56-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3ca56-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3ca56-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca56-131">-ResourceId</span></span>
<span data-ttu-id="3ca56-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3ca56-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3ca56-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca56-133">-Confirm</span></span>
<span data-ttu-id="3ca56-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ca56-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca56-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ca56-135">-WhatIf</span></span>
<span data-ttu-id="3ca56-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca56-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca56-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ca56-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca56-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca56-138">CommonParameters</span></span>
<span data-ttu-id="3ca56-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca56-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca56-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca56-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca56-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ca56-141">INPUTS</span></span>

### <span data-ttu-id="3ca56-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3ca56-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3ca56-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca56-143">System.String</span></span>

## <span data-ttu-id="3ca56-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ca56-144">OUTPUTS</span></span>

### <span data-ttu-id="3ca56-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ca56-145">System.Boolean</span></span>

## <span data-ttu-id="3ca56-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ca56-146">NOTES</span></span>

## <span data-ttu-id="3ca56-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ca56-147">RELATED LINKS</span></span>
