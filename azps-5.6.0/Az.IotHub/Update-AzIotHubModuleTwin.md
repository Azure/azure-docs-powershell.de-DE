---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: 72e9b809ac2b2894b34aefeddd17473cc29d9f35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934171"
---
# <span data-ttu-id="66796-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="66796-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="66796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66796-102">SYNOPSIS</span></span>
<span data-ttu-id="66796-103">Aktualisiert Tags und gewünschte Eigenschaften eines IoT-Gerätemodul-Doppels.</span><span class="sxs-lookup"><span data-stu-id="66796-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="66796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66796-104">SYNTAX</span></span>

### <span data-ttu-id="66796-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66796-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66796-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66796-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66796-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66796-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66796-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66796-108">DESCRIPTION</span></span>
<span data-ttu-id="66796-109">Aktualisiert oder ersetzt einen Gerätezunge.</span><span class="sxs-lookup"><span data-stu-id="66796-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="66796-110">Weitere https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins Informationen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="66796-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="66796-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66796-111">EXAMPLES</span></span>

### <span data-ttu-id="66796-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66796-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="66796-113">Gibt das aktualisierte Doppelobjekt des Gerätemoduls zurück.</span><span class="sxs-lookup"><span data-stu-id="66796-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="66796-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66796-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="66796-115">Gibt das Gerätemodul-Doppelobjekt mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="66796-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="66796-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="66796-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="66796-117">Gibt das Gerätemodul-Doppelobjekt mit der Eigenschaft "Aktualisierte Tags" zurück.</span><span class="sxs-lookup"><span data-stu-id="66796-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="66796-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="66796-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="66796-119">Gibt das ersetzte Gerätemodul-Doppelobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="66796-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="66796-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66796-120">PARAMETERS</span></span>

### <span data-ttu-id="66796-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66796-121">-DefaultProfile</span></span>
<span data-ttu-id="66796-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66796-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66796-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="66796-123">-Desired</span></span>
<span data-ttu-id="66796-124">Fügen Sie die gewünschte Eigenschaft in einem Modulzungepaar hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="66796-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="66796-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="66796-125">-DeviceId</span></span>
<span data-ttu-id="66796-126">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="66796-126">Target Device Id.</span></span>

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

### <span data-ttu-id="66796-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66796-127">-InputObject</span></span>
<span data-ttu-id="66796-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="66796-128">IotHub object</span></span>

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

### <span data-ttu-id="66796-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="66796-129">-IotHubName</span></span>
<span data-ttu-id="66796-130">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="66796-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66796-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="66796-131">-ModuleId</span></span>
<span data-ttu-id="66796-132">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="66796-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66796-133">-Partielle</span><span class="sxs-lookup"><span data-stu-id="66796-133">-Partial</span></span>
<span data-ttu-id="66796-134">Ermöglicht es, die Tags und gewünschten Eigenschaften eines Modulzungspaars nur teilweise zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="66796-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="66796-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66796-135">-ResourceGroupName</span></span>
<span data-ttu-id="66796-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="66796-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66796-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66796-137">-ResourceId</span></span>
<span data-ttu-id="66796-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="66796-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66796-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="66796-139">-Tag</span></span>
<span data-ttu-id="66796-140">Fügen Sie die Tagseigenschaft in einem Modulzungepaar hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="66796-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="66796-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66796-141">-Confirm</span></span>
<span data-ttu-id="66796-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66796-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66796-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66796-143">-WhatIf</span></span>
<span data-ttu-id="66796-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66796-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66796-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66796-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66796-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66796-146">CommonParameters</span></span>
<span data-ttu-id="66796-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66796-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66796-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66796-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66796-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66796-149">INPUTS</span></span>

### <span data-ttu-id="66796-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="66796-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="66796-151">System.String</span><span class="sxs-lookup"><span data-stu-id="66796-151">System.String</span></span>

## <span data-ttu-id="66796-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66796-152">OUTPUTS</span></span>

### <span data-ttu-id="66796-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="66796-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="66796-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66796-154">NOTES</span></span>

## <span data-ttu-id="66796-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66796-155">RELATED LINKS</span></span>
