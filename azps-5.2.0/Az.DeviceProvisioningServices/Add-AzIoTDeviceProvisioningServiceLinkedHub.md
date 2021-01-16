---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296927"
---
# <span data-ttu-id="534f9-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="534f9-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="534f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="534f9-102">SYNOPSIS</span></span>
<span data-ttu-id="534f9-103">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="534f9-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="534f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="534f9-104">SYNTAX</span></span>

### <span data-ttu-id="534f9-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="534f9-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534f9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="534f9-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="534f9-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="534f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="534f9-108">DESCRIPTION</span></span>
<span data-ttu-id="534f9-109">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="534f9-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="534f9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="534f9-110">EXAMPLES</span></span>

### <span data-ttu-id="534f9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="534f9-111">Example 1</span></span>
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

<span data-ttu-id="534f9-112">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="534f9-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="534f9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="534f9-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="534f9-114">Verknüpfter IoT-Hub mit einem Azure IoT Hub-Gerätebereitstellungsdienst mit AllocationWeight und ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="534f9-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="534f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="534f9-115">PARAMETERS</span></span>

### <span data-ttu-id="534f9-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="534f9-116">-AllocationWeight</span></span>
<span data-ttu-id="534f9-117">Gewichtung der Zuordnung des IoT Hub</span><span class="sxs-lookup"><span data-stu-id="534f9-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="534f9-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="534f9-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="534f9-119">Ein boolescher Wert, der angibt, ob eine Zuweisungsrichtlinie auf den IoT Hub angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="534f9-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="534f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534f9-120">-DefaultProfile</span></span>
<span data-ttu-id="534f9-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="534f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534f9-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="534f9-122">-DpsObject</span></span>
<span data-ttu-id="534f9-123">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="534f9-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="534f9-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="534f9-124">-IotHubConnectionString</span></span>
<span data-ttu-id="534f9-125">Verbindungszeichenfolge der Iot-Hub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="534f9-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="534f9-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="534f9-126">-IotHubLocation</span></span>
<span data-ttu-id="534f9-127">Position des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="534f9-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="534f9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="534f9-128">-Name</span></span>
<span data-ttu-id="534f9-129">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="534f9-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="534f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="534f9-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="534f9-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="534f9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="534f9-132">-ResourceId</span></span>
<span data-ttu-id="534f9-133">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="534f9-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="534f9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="534f9-134">-Confirm</span></span>
<span data-ttu-id="534f9-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="534f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534f9-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="534f9-136">-WhatIf</span></span>
<span data-ttu-id="534f9-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="534f9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="534f9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="534f9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="534f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534f9-139">CommonParameters</span></span>
<span data-ttu-id="534f9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534f9-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534f9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534f9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="534f9-142">INPUTS</span></span>

### <span data-ttu-id="534f9-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="534f9-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="534f9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="534f9-144">System.String</span></span>

## <span data-ttu-id="534f9-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="534f9-145">OUTPUTS</span></span>

### <span data-ttu-id="534f9-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="534f9-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="534f9-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="534f9-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="534f9-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="534f9-148">NOTES</span></span>

## <span data-ttu-id="534f9-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="534f9-149">RELATED LINKS</span></span>
