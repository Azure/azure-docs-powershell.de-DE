---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931856"
---
# <span data-ttu-id="a6f25-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="a6f25-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="a6f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f25-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f25-103">Aktualisiert Tags und gewünschte Eigenschaften eines Gerätezungepaars.</span><span class="sxs-lookup"><span data-stu-id="a6f25-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="a6f25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6f25-104">SYNTAX</span></span>

### <span data-ttu-id="a6f25-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6f25-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6f25-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6f25-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6f25-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6f25-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f25-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6f25-108">DESCRIPTION</span></span>
<span data-ttu-id="a6f25-109">Aktualisiert oder ersetzt einen Gerätezunge.</span><span class="sxs-lookup"><span data-stu-id="a6f25-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="a6f25-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="a6f25-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="a6f25-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6f25-111">EXAMPLES</span></span>

### <span data-ttu-id="a6f25-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6f25-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="a6f25-113">Gibt das aktualisierte Gerätezungeobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f25-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="a6f25-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a6f25-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="a6f25-115">Gibt das Gerätezungeobjekt mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f25-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="a6f25-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a6f25-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="a6f25-117">Gibt das Gerätezungeobjekt mit der Eigenschaft "aktualisierte Tags" zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f25-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="a6f25-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a6f25-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="a6f25-119">Gibt das ersetzte Gerätezungeobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a6f25-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="a6f25-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a6f25-120">PARAMETERS</span></span>

### <span data-ttu-id="a6f25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f25-121">-DefaultProfile</span></span>
<span data-ttu-id="a6f25-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f25-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="a6f25-123">-Desired</span></span>
<span data-ttu-id="a6f25-124">Fügen Sie die gewünschte Eigenschaft in einem Gerätezunge hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="a6f25-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="a6f25-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a6f25-125">-DeviceId</span></span>
<span data-ttu-id="a6f25-126">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="a6f25-126">Target Device Id.</span></span>

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

### <span data-ttu-id="a6f25-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6f25-127">-InputObject</span></span>
<span data-ttu-id="a6f25-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="a6f25-128">IotHub object</span></span>

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

### <span data-ttu-id="a6f25-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a6f25-129">-IotHubName</span></span>
<span data-ttu-id="a6f25-130">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="a6f25-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a6f25-131">-Partielle</span><span class="sxs-lookup"><span data-stu-id="a6f25-131">-Partial</span></span>
<span data-ttu-id="a6f25-132">Ermöglicht es, die Tags und gewünschten Eigenschaften eines Gerätezungepaars nur teilweise zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a6f25-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="a6f25-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6f25-133">-ResourceGroupName</span></span>
<span data-ttu-id="a6f25-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a6f25-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6f25-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6f25-135">-ResourceId</span></span>
<span data-ttu-id="a6f25-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a6f25-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a6f25-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6f25-137">-Tag</span></span>
<span data-ttu-id="a6f25-138">Fügen Sie die Tagseigenschaft in einem Gerätezunge hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="a6f25-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="a6f25-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6f25-139">-Confirm</span></span>
<span data-ttu-id="a6f25-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6f25-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f25-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f25-141">-WhatIf</span></span>
<span data-ttu-id="a6f25-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6f25-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6f25-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6f25-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f25-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f25-144">CommonParameters</span></span>
<span data-ttu-id="a6f25-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f25-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f25-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f25-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f25-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6f25-147">INPUTS</span></span>

### <span data-ttu-id="a6f25-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a6f25-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a6f25-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a6f25-149">System.String</span></span>

## <span data-ttu-id="a6f25-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6f25-150">OUTPUTS</span></span>

### <span data-ttu-id="a6f25-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a6f25-151">System.String</span></span>

## <span data-ttu-id="a6f25-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a6f25-152">NOTES</span></span>

## <span data-ttu-id="a6f25-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a6f25-153">RELATED LINKS</span></span>
