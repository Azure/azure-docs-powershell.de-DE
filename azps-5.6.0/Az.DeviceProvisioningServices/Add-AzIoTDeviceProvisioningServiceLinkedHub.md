---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 8b5a42110c99a4572b411d082879f4f2853bac0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934392"
---
# <span data-ttu-id="2582a-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="2582a-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="2582a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2582a-102">SYNOPSIS</span></span>
<span data-ttu-id="2582a-103">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="2582a-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2582a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2582a-104">SYNTAX</span></span>

### <span data-ttu-id="2582a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2582a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2582a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2582a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2582a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2582a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2582a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2582a-108">DESCRIPTION</span></span>
<span data-ttu-id="2582a-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2582a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2582a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2582a-110">EXAMPLES</span></span>

### <span data-ttu-id="2582a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2582a-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="2582a-112">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="2582a-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="2582a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2582a-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="2582a-114">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst mit AllocationWeight und ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="2582a-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="2582a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2582a-115">PARAMETERS</span></span>

### <span data-ttu-id="2582a-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="2582a-116">-AllocationWeight</span></span>
<span data-ttu-id="2582a-117">Zuordnungsgewichtung des IoT Hub</span><span class="sxs-lookup"><span data-stu-id="2582a-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2582a-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2582a-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="2582a-119">Ein boolescher Wert, der angibt, ob eine Zuweisungsrichtlinie auf den IoT Hub angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="2582a-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="2582a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2582a-120">-DefaultProfile</span></span>
<span data-ttu-id="2582a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2582a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2582a-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2582a-122">-DpsObject</span></span>
<span data-ttu-id="2582a-123">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="2582a-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2582a-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2582a-124">-IotHubConnectionString</span></span>
<span data-ttu-id="2582a-125">Verbindungszeichenfolge der Iot Hub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2582a-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="2582a-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="2582a-126">-IotHubLocation</span></span>
<span data-ttu-id="2582a-127">Standort des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="2582a-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2582a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2582a-128">-Name</span></span>
<span data-ttu-id="2582a-129">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="2582a-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2582a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2582a-130">-ResourceGroupName</span></span>
<span data-ttu-id="2582a-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2582a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2582a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2582a-132">-ResourceId</span></span>
<span data-ttu-id="2582a-133">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="2582a-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2582a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2582a-134">-Confirm</span></span>
<span data-ttu-id="2582a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2582a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2582a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2582a-136">-WhatIf</span></span>
<span data-ttu-id="2582a-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2582a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2582a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2582a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2582a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2582a-139">CommonParameters</span></span>
<span data-ttu-id="2582a-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2582a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2582a-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2582a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2582a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2582a-142">INPUTS</span></span>

### <span data-ttu-id="2582a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2582a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2582a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2582a-144">System.String</span></span>

## <span data-ttu-id="2582a-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2582a-145">OUTPUTS</span></span>

### <span data-ttu-id="2582a-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="2582a-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="2582a-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="2582a-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="2582a-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2582a-148">NOTES</span></span>

## <span data-ttu-id="2582a-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2582a-149">RELATED LINKS</span></span>
