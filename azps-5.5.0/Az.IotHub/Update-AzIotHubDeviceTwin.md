---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152820"
---
# <span data-ttu-id="193b0-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="193b0-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="193b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="193b0-102">SYNOPSIS</span></span>
<span data-ttu-id="193b0-103">Aktualisiert Tags und die gewünschten Eigenschaften eines Gerätegeräts.</span><span class="sxs-lookup"><span data-stu-id="193b0-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="193b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="193b0-104">SYNTAX</span></span>

### <span data-ttu-id="193b0-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="193b0-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="193b0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="193b0-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="193b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="193b0-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="193b0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="193b0-108">DESCRIPTION</span></span>
<span data-ttu-id="193b0-109">Aktualisiert oder ersetzt ein Gerätegerät.</span><span class="sxs-lookup"><span data-stu-id="193b0-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="193b0-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="193b0-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="193b0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="193b0-111">EXAMPLES</span></span>

### <span data-ttu-id="193b0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="193b0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="193b0-113">Gibt das aktualisierte Geräteobjekt "." zurück.</span><span class="sxs-lookup"><span data-stu-id="193b0-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="193b0-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="193b0-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="193b0-115">Gibt das Gerät -Objekt mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="193b0-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="193b0-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="193b0-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="193b0-117">Gibt das Objekt "device" mit der Eigenschaft "updated tags" zurück.</span><span class="sxs-lookup"><span data-stu-id="193b0-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="193b0-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="193b0-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="193b0-119">Gibt das ersetzte Geräteobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="193b0-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="193b0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="193b0-120">PARAMETERS</span></span>

### <span data-ttu-id="193b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193b0-121">-DefaultProfile</span></span>
<span data-ttu-id="193b0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="193b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="193b0-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="193b0-123">-Desired</span></span>
<span data-ttu-id="193b0-124">Fügen Sie die gewünschte Eigenschaft in einem Gerätegerät hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="193b0-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="193b0-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="193b0-125">-DeviceId</span></span>
<span data-ttu-id="193b0-126">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="193b0-126">Target Device Id.</span></span>

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

### <span data-ttu-id="193b0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="193b0-127">-InputObject</span></span>
<span data-ttu-id="193b0-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="193b0-128">IotHub object</span></span>

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

### <span data-ttu-id="193b0-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="193b0-129">-IotHubName</span></span>
<span data-ttu-id="193b0-130">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="193b0-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="193b0-131">-Partiell</span><span class="sxs-lookup"><span data-stu-id="193b0-131">-Partial</span></span>
<span data-ttu-id="193b0-132">Ermöglicht es, die Tags und gewünschten Eigenschaften eines Gerätegeräts nur teilweise zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="193b0-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="193b0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="193b0-133">-ResourceGroupName</span></span>
<span data-ttu-id="193b0-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="193b0-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="193b0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="193b0-135">-ResourceId</span></span>
<span data-ttu-id="193b0-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="193b0-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="193b0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="193b0-137">-Tag</span></span>
<span data-ttu-id="193b0-138">Fügen Sie die Tageigenschaft in einem Gerätegerät hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="193b0-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="193b0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="193b0-139">-Confirm</span></span>
<span data-ttu-id="193b0-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="193b0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="193b0-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="193b0-141">-WhatIf</span></span>
<span data-ttu-id="193b0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="193b0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="193b0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="193b0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="193b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193b0-144">CommonParameters</span></span>
<span data-ttu-id="193b0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="193b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193b0-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="193b0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193b0-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="193b0-147">INPUTS</span></span>

### <span data-ttu-id="193b0-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="193b0-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="193b0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="193b0-149">System.String</span></span>

## <span data-ttu-id="193b0-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="193b0-150">OUTPUTS</span></span>

### <span data-ttu-id="193b0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="193b0-151">System.String</span></span>

## <span data-ttu-id="193b0-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="193b0-152">NOTES</span></span>

## <span data-ttu-id="193b0-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="193b0-153">RELATED LINKS</span></span>
