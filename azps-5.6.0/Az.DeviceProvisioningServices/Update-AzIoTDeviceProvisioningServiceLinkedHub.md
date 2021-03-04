---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 4065e44d9ec0ed2512438356231176a1de10e7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935192"
---
# <span data-ttu-id="9ca92-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="9ca92-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="9ca92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca92-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca92-103">Aktualisieren Sie einen verknüpften IoT-Hub in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="9ca92-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9ca92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ca92-104">SYNTAX</span></span>

### <span data-ttu-id="9ca92-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ca92-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca92-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ca92-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca92-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ca92-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca92-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ca92-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca92-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9ca92-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9ca92-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ca92-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca92-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ca92-111">Example 1</span></span>
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

<span data-ttu-id="9ca92-112">Aktualisieren Sie verknüpfte IoT hub "myiothub.azure-devices.net" in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="9ca92-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9ca92-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ca92-113">PARAMETERS</span></span>

### <span data-ttu-id="9ca92-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="9ca92-114">-AllocationWeight</span></span>
<span data-ttu-id="9ca92-115">Zuordnungsgewichtung des IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9ca92-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="9ca92-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9ca92-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="9ca92-117">Anwenden einer Zuweisungsrichtlinie auf den IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9ca92-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="9ca92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca92-118">-DefaultProfile</span></span>
<span data-ttu-id="9ca92-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ca92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca92-120">-InputObject</span></span>
<span data-ttu-id="9ca92-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="9ca92-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9ca92-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="9ca92-122">-LinkedHubName</span></span>
<span data-ttu-id="9ca92-123">Hostname des verknüpften IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9ca92-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="9ca92-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9ca92-124">-Name</span></span>
<span data-ttu-id="9ca92-125">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="9ca92-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9ca92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca92-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ca92-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9ca92-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ca92-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca92-128">-ResourceId</span></span>
<span data-ttu-id="9ca92-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="9ca92-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9ca92-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ca92-130">-Confirm</span></span>
<span data-ttu-id="9ca92-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ca92-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca92-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca92-132">-WhatIf</span></span>
<span data-ttu-id="9ca92-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ca92-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca92-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ca92-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca92-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca92-135">CommonParameters</span></span>
<span data-ttu-id="9ca92-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca92-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca92-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca92-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca92-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ca92-138">INPUTS</span></span>

### <span data-ttu-id="9ca92-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="9ca92-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="9ca92-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9ca92-140">System.String</span></span>

## <span data-ttu-id="9ca92-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ca92-141">OUTPUTS</span></span>

### <span data-ttu-id="9ca92-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="9ca92-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="9ca92-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ca92-143">NOTES</span></span>

## <span data-ttu-id="9ca92-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ca92-144">RELATED LINKS</span></span>
