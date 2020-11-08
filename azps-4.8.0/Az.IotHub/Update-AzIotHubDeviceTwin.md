---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166591"
---
# <span data-ttu-id="517b8-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="517b8-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="517b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="517b8-102">SYNOPSIS</span></span>
<span data-ttu-id="517b8-103">Aktualisiert Tags und die gewünschten Eigenschaften eines Geräte Zwillings.</span><span class="sxs-lookup"><span data-stu-id="517b8-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="517b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="517b8-104">SYNTAX</span></span>

### <span data-ttu-id="517b8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="517b8-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517b8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="517b8-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="517b8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="517b8-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517b8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="517b8-108">DESCRIPTION</span></span>
<span data-ttu-id="517b8-109">Aktualisiert oder ersetzt ein Gerät Twin.</span><span class="sxs-lookup"><span data-stu-id="517b8-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="517b8-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins .</span><span class="sxs-lookup"><span data-stu-id="517b8-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="517b8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="517b8-111">EXAMPLES</span></span>

### <span data-ttu-id="517b8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="517b8-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="517b8-113">Gibt das aktualisierte Device Twin-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="517b8-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="517b8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="517b8-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="517b8-115">Gibt das Device Twin-Objekt mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="517b8-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="517b8-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="517b8-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="517b8-117">Gibt das Device Twin-Objekt mit der aktualisierten Tags-Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="517b8-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="517b8-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="517b8-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="517b8-119">Gibt das ersetzte Device Twin-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="517b8-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="517b8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="517b8-120">PARAMETERS</span></span>

### <span data-ttu-id="517b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517b8-121">-DefaultProfile</span></span>
<span data-ttu-id="517b8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="517b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517b8-123">-Erwünscht</span><span class="sxs-lookup"><span data-stu-id="517b8-123">-Desired</span></span>
<span data-ttu-id="517b8-124">Hinzufügen oder Aktualisieren der gewünschten Eigenschaft in einem Geräte-Twin</span><span class="sxs-lookup"><span data-stu-id="517b8-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="517b8-125">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="517b8-125">-DeviceId</span></span>
<span data-ttu-id="517b8-126">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="517b8-126">Target Device Id.</span></span>

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

### <span data-ttu-id="517b8-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="517b8-127">-InputObject</span></span>
<span data-ttu-id="517b8-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="517b8-128">IotHub object</span></span>

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

### <span data-ttu-id="517b8-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="517b8-129">-IotHubName</span></span>
<span data-ttu-id="517b8-130">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="517b8-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="517b8-131">-Teilweise</span><span class="sxs-lookup"><span data-stu-id="517b8-131">-Partial</span></span>
<span data-ttu-id="517b8-132">Ermöglicht es, die Tags und die gewünschten Eigenschaften eines Geräte Zwillings nur teilweise zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="517b8-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="517b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="517b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="517b8-134">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="517b8-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="517b8-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="517b8-135">-ResourceId</span></span>
<span data-ttu-id="517b8-136">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="517b8-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="517b8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="517b8-137">-Tag</span></span>
<span data-ttu-id="517b8-138">Hinzufügen oder Aktualisieren der Tags-Eigenschaft in einem Geräte-Twin</span><span class="sxs-lookup"><span data-stu-id="517b8-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="517b8-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="517b8-139">-Confirm</span></span>
<span data-ttu-id="517b8-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="517b8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517b8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517b8-141">-WhatIf</span></span>
<span data-ttu-id="517b8-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="517b8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517b8-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="517b8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517b8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517b8-144">CommonParameters</span></span>
<span data-ttu-id="517b8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517b8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517b8-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517b8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517b8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="517b8-147">INPUTS</span></span>

### <span data-ttu-id="517b8-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="517b8-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="517b8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="517b8-149">System.String</span></span>

## <span data-ttu-id="517b8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="517b8-150">OUTPUTS</span></span>

### <span data-ttu-id="517b8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="517b8-151">System.String</span></span>

## <span data-ttu-id="517b8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="517b8-152">NOTES</span></span>

## <span data-ttu-id="517b8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="517b8-153">RELATED LINKS</span></span>
