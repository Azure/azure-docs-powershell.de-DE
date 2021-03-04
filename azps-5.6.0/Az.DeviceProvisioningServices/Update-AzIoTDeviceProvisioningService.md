---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935200"
---
# <span data-ttu-id="661f6-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="661f6-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="661f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661f6-102">SYNOPSIS</span></span>
<span data-ttu-id="661f6-103">Aktualisieren eines Azure IoT Hub-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="661f6-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="661f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="661f6-104">SYNTAX</span></span>

### <span data-ttu-id="661f6-105">ResourceUpdateSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="661f6-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661f6-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="661f6-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661f6-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="661f6-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="661f6-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="661f6-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661f6-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="661f6-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="661f6-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="661f6-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="661f6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="661f6-111">DESCRIPTION</span></span>
<span data-ttu-id="661f6-112">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="661f6-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="661f6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="661f6-113">EXAMPLES</span></span>

### <span data-ttu-id="661f6-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="661f6-114">Example 1</span></span>
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

<span data-ttu-id="661f6-115">Aktualisieren Sie die Zuweisungsrichtlinie auf "GeoLatency" eines Azure IoT Hub-Gerätebereitstellungsdiensts "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="661f6-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="661f6-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="661f6-116">Example 2</span></span>
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

<span data-ttu-id="661f6-117">Fügen Sie einem Azure IoT Hub-Gerätebereitstellungsdienst "myiotdps" Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="661f6-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="661f6-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="661f6-118">Example 3</span></span>
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

<span data-ttu-id="661f6-119">Löschen Sie Tag, und fügen Sie einem Azure IoT Hub-Gerätebereitstellungsdienst "myiotdps" mithilfe der Pipeline neue Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="661f6-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="661f6-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="661f6-120">PARAMETERS</span></span>

### <span data-ttu-id="661f6-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="661f6-121">-AllocationPolicy</span></span>
<span data-ttu-id="661f6-122">IoT Device Provisioning Service Allocation policy</span><span class="sxs-lookup"><span data-stu-id="661f6-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="661f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661f6-123">-DefaultProfile</span></span>
<span data-ttu-id="661f6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="661f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="661f6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="661f6-125">-InputObject</span></span>
<span data-ttu-id="661f6-126">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="661f6-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="661f6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="661f6-127">-Name</span></span>
<span data-ttu-id="661f6-128">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="661f6-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="661f6-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="661f6-129">-Reset</span></span>
<span data-ttu-id="661f6-130">Zurücksetzen von IoT-Gerätebereitstellungsdiensttags</span><span class="sxs-lookup"><span data-stu-id="661f6-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="661f6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661f6-131">-ResourceGroupName</span></span>
<span data-ttu-id="661f6-132">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="661f6-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="661f6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="661f6-133">-ResourceId</span></span>
<span data-ttu-id="661f6-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="661f6-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="661f6-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="661f6-135">-Tag</span></span>
<span data-ttu-id="661f6-136">IoT Device Provisioning Service Tag Collection</span><span class="sxs-lookup"><span data-stu-id="661f6-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="661f6-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="661f6-137">-Confirm</span></span>
<span data-ttu-id="661f6-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="661f6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661f6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661f6-139">-WhatIf</span></span>
<span data-ttu-id="661f6-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="661f6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661f6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="661f6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661f6-142">CommonParameters</span></span>
<span data-ttu-id="661f6-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661f6-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661f6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661f6-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="661f6-145">INPUTS</span></span>

### <span data-ttu-id="661f6-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="661f6-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="661f6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="661f6-147">System.String</span></span>

## <span data-ttu-id="661f6-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="661f6-148">OUTPUTS</span></span>

### <span data-ttu-id="661f6-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="661f6-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="661f6-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="661f6-150">NOTES</span></span>

## <span data-ttu-id="661f6-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="661f6-151">RELATED LINKS</span></span>
