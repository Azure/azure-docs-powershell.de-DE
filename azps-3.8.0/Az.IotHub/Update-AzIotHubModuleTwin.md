---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996777"
---
# <span data-ttu-id="478dc-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="478dc-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="478dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="478dc-102">SYNOPSIS</span></span>
<span data-ttu-id="478dc-103">Aktualisiert Tags und gewünschte Eigenschaften eines viel Geräte Moduls Twin.</span><span class="sxs-lookup"><span data-stu-id="478dc-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="478dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="478dc-104">SYNTAX</span></span>

### <span data-ttu-id="478dc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="478dc-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="478dc-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="478dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="478dc-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="478dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="478dc-108">DESCRIPTION</span></span>
<span data-ttu-id="478dc-109">Aktualisiert oder ersetzt ein Gerät Twin.</span><span class="sxs-lookup"><span data-stu-id="478dc-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="478dc-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins .</span><span class="sxs-lookup"><span data-stu-id="478dc-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="478dc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="478dc-111">EXAMPLES</span></span>

### <span data-ttu-id="478dc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="478dc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="478dc-113">Gibt das aktualisierte Gerätemodul Twin-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="478dc-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="478dc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="478dc-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="478dc-115">Gibt das Doppel Objekt des Geräte Moduls mit aktualisierten gewünschten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="478dc-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="478dc-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="478dc-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="478dc-117">Gibt das Doppel Objekt des Geräte Moduls mit der aktualisierten Tags-Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="478dc-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="478dc-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="478dc-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="478dc-119">Gibt das ersetzte Gerätemodul Twin-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="478dc-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="478dc-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="478dc-120">PARAMETERS</span></span>

### <span data-ttu-id="478dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478dc-121">-DefaultProfile</span></span>
<span data-ttu-id="478dc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="478dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478dc-123">-Erwünscht</span><span class="sxs-lookup"><span data-stu-id="478dc-123">-Desired</span></span>
<span data-ttu-id="478dc-124">Hinzufügen oder Aktualisieren der gewünschten Eigenschaft in einem Modul Twin</span><span class="sxs-lookup"><span data-stu-id="478dc-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="478dc-125">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="478dc-125">-DeviceId</span></span>
<span data-ttu-id="478dc-126">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="478dc-126">Target Device Id.</span></span>

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

### <span data-ttu-id="478dc-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="478dc-127">-InputObject</span></span>
<span data-ttu-id="478dc-128">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="478dc-128">IotHub object</span></span>

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

### <span data-ttu-id="478dc-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="478dc-129">-IotHubName</span></span>
<span data-ttu-id="478dc-130">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="478dc-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="478dc-131">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="478dc-131">-ModuleId</span></span>
<span data-ttu-id="478dc-132">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="478dc-132">Target Module Id.</span></span>

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

### <span data-ttu-id="478dc-133">-Teilweise</span><span class="sxs-lookup"><span data-stu-id="478dc-133">-Partial</span></span>
<span data-ttu-id="478dc-134">Ermöglicht das nur teilweise Aktualisieren der Tags und der gewünschten Eigenschaften eines Moduls Twin.</span><span class="sxs-lookup"><span data-stu-id="478dc-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="478dc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478dc-135">-ResourceGroupName</span></span>
<span data-ttu-id="478dc-136">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="478dc-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="478dc-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="478dc-137">-ResourceId</span></span>
<span data-ttu-id="478dc-138">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="478dc-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="478dc-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="478dc-139">-Tag</span></span>
<span data-ttu-id="478dc-140">Fügen Sie die Tags-Eigenschaft in einem Modul Twin hinzu, oder aktualisieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="478dc-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="478dc-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="478dc-141">-Confirm</span></span>
<span data-ttu-id="478dc-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="478dc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478dc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478dc-143">-WhatIf</span></span>
<span data-ttu-id="478dc-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="478dc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478dc-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="478dc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478dc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478dc-146">CommonParameters</span></span>
<span data-ttu-id="478dc-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478dc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478dc-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478dc-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478dc-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="478dc-149">INPUTS</span></span>

### <span data-ttu-id="478dc-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="478dc-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="478dc-151">System. String</span><span class="sxs-lookup"><span data-stu-id="478dc-151">System.String</span></span>

## <span data-ttu-id="478dc-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="478dc-152">OUTPUTS</span></span>

### <span data-ttu-id="478dc-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="478dc-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="478dc-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="478dc-154">NOTES</span></span>

## <span data-ttu-id="478dc-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="478dc-155">RELATED LINKS</span></span>
