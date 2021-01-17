---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376899"
---
# <span data-ttu-id="09cbc-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="09cbc-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="09cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="09cbc-103">Aktualisieren Sie einen verknüpften IoT-Hub in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="09cbc-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="09cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09cbc-104">SYNTAX</span></span>

### <span data-ttu-id="09cbc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09cbc-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09cbc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="09cbc-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09cbc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="09cbc-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09cbc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="09cbc-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="09cbc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="09cbc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="09cbc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09cbc-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="09cbc-112">Aktualisieren Sie den verknüpften "myiothub.azure-devices.net" eines Azure IoT Hub-Gerätebereitstellungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="09cbc-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="09cbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09cbc-113">PARAMETERS</span></span>

### <span data-ttu-id="09cbc-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="09cbc-114">-AllocationWeight</span></span>
<span data-ttu-id="09cbc-115">Gewichtung der Zuordnung des IoT Hub</span><span class="sxs-lookup"><span data-stu-id="09cbc-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="09cbc-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="09cbc-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="09cbc-117">Anwenden einer Zuweisungsrichtlinie auf den IoT Hub</span><span class="sxs-lookup"><span data-stu-id="09cbc-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="09cbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cbc-118">-DefaultProfile</span></span>
<span data-ttu-id="09cbc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09cbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09cbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09cbc-120">-InputObject</span></span>
<span data-ttu-id="09cbc-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="09cbc-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09cbc-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="09cbc-122">-LinkedHubName</span></span>
<span data-ttu-id="09cbc-123">Hostname des verknüpften IoT Hubs</span><span class="sxs-lookup"><span data-stu-id="09cbc-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cbc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="09cbc-124">-Name</span></span>
<span data-ttu-id="09cbc-125">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="09cbc-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="09cbc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09cbc-126">-ResourceGroupName</span></span>
<span data-ttu-id="09cbc-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="09cbc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09cbc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09cbc-128">-ResourceId</span></span>
<span data-ttu-id="09cbc-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="09cbc-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="09cbc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09cbc-130">-Confirm</span></span>
<span data-ttu-id="09cbc-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09cbc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09cbc-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09cbc-132">-WhatIf</span></span>
<span data-ttu-id="09cbc-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09cbc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09cbc-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09cbc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09cbc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cbc-135">CommonParameters</span></span>
<span data-ttu-id="09cbc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09cbc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cbc-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09cbc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cbc-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09cbc-138">INPUTS</span></span>

### <span data-ttu-id="09cbc-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="09cbc-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="09cbc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="09cbc-140">System.String</span></span>

## <span data-ttu-id="09cbc-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09cbc-141">OUTPUTS</span></span>

### <span data-ttu-id="09cbc-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="09cbc-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="09cbc-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09cbc-143">NOTES</span></span>

## <span data-ttu-id="09cbc-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09cbc-144">RELATED LINKS</span></span>
