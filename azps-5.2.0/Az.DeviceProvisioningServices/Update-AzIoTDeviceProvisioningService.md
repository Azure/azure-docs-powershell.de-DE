---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302536"
---
# <span data-ttu-id="5d294-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="5d294-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="5d294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d294-102">SYNOPSIS</span></span>
<span data-ttu-id="5d294-103">Aktualisieren Sie einen Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5d294-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5d294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d294-104">SYNTAX</span></span>

### <span data-ttu-id="5d294-105">ResourceUpdateSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d294-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d294-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="5d294-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d294-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="5d294-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d294-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="5d294-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d294-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="5d294-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d294-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="5d294-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d294-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d294-111">DESCRIPTION</span></span>
<span data-ttu-id="5d294-112">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5d294-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5d294-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d294-113">EXAMPLES</span></span>

### <span data-ttu-id="5d294-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d294-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="5d294-115">Aktualisieren Sie die Zuweisungsrichtlinie auf "GeoLatency" eines Azure IoT Hub-Gerätebereitstellungsdiensts "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="5d294-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="5d294-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d294-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="5d294-117">Fügen Sie einem Azure IoT Hub-Gerätebereitstellungsdienst "myiotdps" Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d294-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="5d294-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5d294-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="5d294-119">Löschen Sie "Tag", und fügen Sie einem Azure IoT -Hub-Gerätebereitstellungsdienst "myiotdps" mithilfe der Pipeline neue Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d294-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="5d294-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d294-120">PARAMETERS</span></span>

### <span data-ttu-id="5d294-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5d294-121">-AllocationPolicy</span></span>
<span data-ttu-id="5d294-122">IoT Device Provisioning Service Allocation policy</span><span class="sxs-lookup"><span data-stu-id="5d294-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d294-123">-DefaultProfile</span></span>
<span data-ttu-id="5d294-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d294-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d294-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d294-125">-InputObject</span></span>
<span data-ttu-id="5d294-126">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="5d294-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5d294-127">-Name</span></span>
<span data-ttu-id="5d294-128">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="5d294-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="5d294-129">-Reset</span></span>
<span data-ttu-id="5d294-130">Zurücksetzen von IoT-Gerätebereitstellungsdiensttags</span><span class="sxs-lookup"><span data-stu-id="5d294-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d294-131">-ResourceGroupName</span></span>
<span data-ttu-id="5d294-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5d294-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d294-133">-ResourceId</span></span>
<span data-ttu-id="5d294-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5d294-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d294-135">-Tag</span></span>
<span data-ttu-id="5d294-136">IoT Device Provisioning Service Tag collection</span><span class="sxs-lookup"><span data-stu-id="5d294-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d294-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d294-137">-Confirm</span></span>
<span data-ttu-id="5d294-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d294-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d294-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d294-139">-WhatIf</span></span>
<span data-ttu-id="5d294-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d294-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d294-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d294-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d294-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d294-142">CommonParameters</span></span>
<span data-ttu-id="5d294-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d294-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d294-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d294-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d294-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d294-145">INPUTS</span></span>

### <span data-ttu-id="5d294-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5d294-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5d294-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5d294-147">System.String</span></span>

## <span data-ttu-id="5d294-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d294-148">OUTPUTS</span></span>

### <span data-ttu-id="5d294-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5d294-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="5d294-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d294-150">NOTES</span></span>

## <span data-ttu-id="5d294-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d294-151">RELATED LINKS</span></span>
