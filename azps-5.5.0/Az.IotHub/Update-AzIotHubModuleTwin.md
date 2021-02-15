---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167281"
---
# <span data-ttu-id="54d73-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="54d73-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="54d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d73-102">SYNOPSIS</span></span>
<span data-ttu-id="54d73-103">Aktualisiert Tags und gewünschte Eigenschaften eines IoT-Gerätemodul-Moduls.</span><span class="sxs-lookup"><span data-stu-id="54d73-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="54d73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54d73-104">SYNTAX</span></span>

### <span data-ttu-id="54d73-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54d73-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d73-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54d73-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54d73-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54d73-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54d73-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54d73-108">DESCRIPTION</span></span>
<span data-ttu-id="54d73-109">Aktualisiert oder ersetzt ein Gerätegerät.</span><span class="sxs-lookup"><span data-stu-id="54d73-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="54d73-110">Weitere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="54d73-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="54d73-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54d73-111">EXAMPLES</span></span>

### <span data-ttu-id="54d73-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54d73-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="54d73-113">Gibt das aktualisierte Gerätemodulobjekt "." zurück.</span><span class="sxs-lookup"><span data-stu-id="54d73-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="54d73-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54d73-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="54d73-115">Gibt das Gerätemodul-Objekt mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="54d73-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="54d73-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="54d73-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="54d73-117">Gibt das Objekt des Gerätemoduls "module" mit der Eigenschaft "updated tags" zurück.</span><span class="sxs-lookup"><span data-stu-id="54d73-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="54d73-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="54d73-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="54d73-119">Gibt das ersetzte Gerätemodulobjekt "." zurück.</span><span class="sxs-lookup"><span data-stu-id="54d73-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="54d73-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d73-120">PARAMETERS</span></span>

### <span data-ttu-id="54d73-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d73-121">-DefaultProfile</span></span>
<span data-ttu-id="54d73-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54d73-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d73-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="54d73-123">-Desired</span></span>
<span data-ttu-id="54d73-124">Fügen Sie die gewünschte Eigenschaft in einem Modul eines Moduls hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="54d73-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="54d73-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="54d73-125">-DeviceId</span></span>
<span data-ttu-id="54d73-126">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="54d73-126">Target Device Id.</span></span>

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

### <span data-ttu-id="54d73-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54d73-127">-InputObject</span></span>
<span data-ttu-id="54d73-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="54d73-128">IotHub object</span></span>

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

### <span data-ttu-id="54d73-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="54d73-129">-IotHubName</span></span>
<span data-ttu-id="54d73-130">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="54d73-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="54d73-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="54d73-131">-ModuleId</span></span>
<span data-ttu-id="54d73-132">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="54d73-132">Target Module Id.</span></span>

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

### <span data-ttu-id="54d73-133">-Partiell</span><span class="sxs-lookup"><span data-stu-id="54d73-133">-Partial</span></span>
<span data-ttu-id="54d73-134">Ermöglicht es, die Tags und gewünschten Eigenschaften eines Moduls nur teilweise zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="54d73-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="54d73-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d73-135">-ResourceGroupName</span></span>
<span data-ttu-id="54d73-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="54d73-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54d73-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54d73-137">-ResourceId</span></span>
<span data-ttu-id="54d73-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="54d73-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="54d73-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="54d73-139">-Tag</span></span>
<span data-ttu-id="54d73-140">Fügen Sie die Tageigenschaft in einem Modul hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="54d73-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="54d73-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54d73-141">-Confirm</span></span>
<span data-ttu-id="54d73-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54d73-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d73-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="54d73-143">-WhatIf</span></span>
<span data-ttu-id="54d73-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d73-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54d73-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54d73-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d73-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d73-146">CommonParameters</span></span>
<span data-ttu-id="54d73-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d73-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d73-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d73-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d73-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54d73-149">INPUTS</span></span>

### <span data-ttu-id="54d73-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="54d73-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="54d73-151">System.String</span><span class="sxs-lookup"><span data-stu-id="54d73-151">System.String</span></span>

## <span data-ttu-id="54d73-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54d73-152">OUTPUTS</span></span>

### <span data-ttu-id="54d73-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="54d73-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="54d73-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54d73-154">NOTES</span></span>

## <span data-ttu-id="54d73-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54d73-155">RELATED LINKS</span></span>
