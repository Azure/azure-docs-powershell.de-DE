---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942531"
---
# <span data-ttu-id="a07a6-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a07a6-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="a07a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a07a6-103">Fügen Sie dem Edgegerät Nicht-Edge-Geräte als untere Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a07a6-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="a07a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a07a6-104">SYNTAX</span></span>

### <span data-ttu-id="a07a6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a07a6-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a07a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a07a6-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a07a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a07a6-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07a6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a07a6-108">DESCRIPTION</span></span>
<span data-ttu-id="a07a6-109">Fügen Sie eine angegebene durch Kommas getrennte Liste der nicht edge-Geräte-ID als Unter-n des angegebenen Edgegeräts hinzu.</span><span class="sxs-lookup"><span data-stu-id="a07a6-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="a07a6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a07a6-110">EXAMPLES</span></span>

### <span data-ttu-id="a07a6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a07a6-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="a07a6-112">Fügen Sie dem Edgegerät Nicht-Edge-Geräte als untere Geräte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a07a6-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="a07a6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a07a6-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="a07a6-114">Fügen Sie dem Edgegerät Nicht-Edge-Geräte als untergeordnete Geräte hinzu, unabhängig davon, ob das Nicht-Edge-Gerät bereits ein Untergeordnetes eines anderen Edgegeräts ist.</span><span class="sxs-lookup"><span data-stu-id="a07a6-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="a07a6-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a07a6-115">PARAMETERS</span></span>

### <span data-ttu-id="a07a6-116">-Kinder</span><span class="sxs-lookup"><span data-stu-id="a07a6-116">-Children</span></span>
<span data-ttu-id="a07a6-117">Die Liste der untergeordneten Geräte (durch Kommas getrennt) umfasst nur Nicht-Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="a07a6-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="a07a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07a6-118">-DefaultProfile</span></span>
<span data-ttu-id="a07a6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a07a6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07a6-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a07a6-120">-DeviceId</span></span>
<span data-ttu-id="a07a6-121">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="a07a6-121">Id of edge device.</span></span>

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

### <span data-ttu-id="a07a6-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a07a6-122">-Force</span></span>
<span data-ttu-id="a07a6-123">Überschreibt das übergeordnete Gerät des Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a07a6-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="a07a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a07a6-124">-InputObject</span></span>
<span data-ttu-id="a07a6-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="a07a6-125">IotHub object</span></span>

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

### <span data-ttu-id="a07a6-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a07a6-126">-IotHubName</span></span>
<span data-ttu-id="a07a6-127">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="a07a6-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a07a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="a07a6-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a07a6-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a07a6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a07a6-130">-ResourceId</span></span>
<span data-ttu-id="a07a6-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a07a6-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a07a6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a07a6-132">-Confirm</span></span>
<span data-ttu-id="a07a6-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a07a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07a6-134">-WhatIf</span></span>
<span data-ttu-id="a07a6-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a07a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07a6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a07a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07a6-137">CommonParameters</span></span>
<span data-ttu-id="a07a6-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07a6-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07a6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07a6-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a07a6-140">INPUTS</span></span>

### <span data-ttu-id="a07a6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a07a6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a07a6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a07a6-142">System.String</span></span>

## <span data-ttu-id="a07a6-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a07a6-143">OUTPUTS</span></span>

### <span data-ttu-id="a07a6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a07a6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="a07a6-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a07a6-145">NOTES</span></span>

## <span data-ttu-id="a07a6-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a07a6-146">RELATED LINKS</span></span>
