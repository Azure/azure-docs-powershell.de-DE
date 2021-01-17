---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472428"
---
# <span data-ttu-id="a1584-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a1584-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="a1584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1584-102">SYNOPSIS</span></span>
<span data-ttu-id="a1584-103">Fügen Sie dem Edgegerät Geräte, die keine Edgegeräte sind, als untere Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1584-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="a1584-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1584-104">SYNTAX</span></span>

### <span data-ttu-id="a1584-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1584-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1584-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1584-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1584-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1584-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1584-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1584-108">DESCRIPTION</span></span>
<span data-ttu-id="a1584-109">Fügen Sie eine angegebene durch Kommas getrennte Liste von nicht edge-Geräte-IDs als "Children" eines angegebenen Edgegeräts hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1584-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="a1584-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1584-110">EXAMPLES</span></span>

### <span data-ttu-id="a1584-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1584-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="a1584-112">Fügen Sie dem Edgegerät Geräte, die keine Edgegeräte sind, als untere Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1584-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="a1584-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a1584-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="a1584-114">Fügen Sie Nicht-Edge-Geräte als untergeordnete Geräte zum Edgegerät hinzu, unabhängig davon, ob das Nicht-Edge-Gerät bereits untergeordnetes Gerät eines anderen Edgegeräts ist.</span><span class="sxs-lookup"><span data-stu-id="a1584-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="a1584-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1584-115">PARAMETERS</span></span>

### <span data-ttu-id="a1584-116">-Children</span><span class="sxs-lookup"><span data-stu-id="a1584-116">-Children</span></span>
<span data-ttu-id="a1584-117">Die Liste untergeordneter Geräte (durch Kommas getrennt) schließt nur Geräte ein, die keine Edgegeräte sind.</span><span class="sxs-lookup"><span data-stu-id="a1584-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1584-118">-DefaultProfile</span></span>
<span data-ttu-id="a1584-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1584-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1584-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a1584-120">-DeviceId</span></span>
<span data-ttu-id="a1584-121">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="a1584-121">Id of edge device.</span></span>

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

### <span data-ttu-id="a1584-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a1584-122">-Force</span></span>
<span data-ttu-id="a1584-123">Überschreibt das übergeordnete Gerät des Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a1584-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="a1584-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1584-124">-InputObject</span></span>
<span data-ttu-id="a1584-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="a1584-125">IotHub object</span></span>

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

### <span data-ttu-id="a1584-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a1584-126">-IotHubName</span></span>
<span data-ttu-id="a1584-127">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="a1584-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1584-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1584-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1584-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a1584-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1584-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1584-130">-ResourceId</span></span>
<span data-ttu-id="a1584-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a1584-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a1584-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1584-132">-Confirm</span></span>
<span data-ttu-id="a1584-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1584-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1584-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a1584-134">-WhatIf</span></span>
<span data-ttu-id="a1584-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1584-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1584-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1584-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1584-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1584-137">CommonParameters</span></span>
<span data-ttu-id="a1584-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1584-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1584-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1584-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1584-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1584-140">INPUTS</span></span>

### <span data-ttu-id="a1584-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a1584-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a1584-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a1584-142">System.String</span></span>

## <span data-ttu-id="a1584-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1584-143">OUTPUTS</span></span>

### <span data-ttu-id="a1584-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice1</span><span class="sxs-lookup"><span data-stu-id="a1584-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="a1584-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1584-145">NOTES</span></span>

## <span data-ttu-id="a1584-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1584-146">RELATED LINKS</span></span>
