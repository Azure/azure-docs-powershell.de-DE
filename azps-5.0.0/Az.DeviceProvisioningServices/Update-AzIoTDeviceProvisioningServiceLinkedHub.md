---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175688"
---
# <span data-ttu-id="c3d14-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="c3d14-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="c3d14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3d14-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d14-103">Aktualisieren eines verknüpften viele-Hubs in einem Azure-to-Hub-Device-Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="c3d14-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c3d14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3d14-104">SYNTAX</span></span>

### <span data-ttu-id="c3d14-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3d14-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d14-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3d14-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d14-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3d14-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d14-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3d14-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d14-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c3d14-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c3d14-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3d14-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d14-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3d14-111">Example 1</span></span>
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

<span data-ttu-id="c3d14-112">Aktualisieren des verknüpften viele-Hubs "myiothub.Azure-Devices.net" in einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c3d14-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c3d14-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3d14-113">PARAMETERS</span></span>

### <span data-ttu-id="c3d14-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="c3d14-114">-AllocationWeight</span></span>
<span data-ttu-id="c3d14-115">Zuordnungs Gewicht des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="c3d14-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="c3d14-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="c3d14-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="c3d14-117">Anwenden von Zuordnungsrichtlinien auf den viel-Hub</span><span class="sxs-lookup"><span data-stu-id="c3d14-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="c3d14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d14-118">-DefaultProfile</span></span>
<span data-ttu-id="c3d14-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3d14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d14-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3d14-120">-InputObject</span></span>
<span data-ttu-id="c3d14-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="c3d14-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c3d14-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="c3d14-122">-LinkedHubName</span></span>
<span data-ttu-id="c3d14-123">Hostname des verknüpften Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="c3d14-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="c3d14-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d14-124">-Name</span></span>
<span data-ttu-id="c3d14-125">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c3d14-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c3d14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d14-126">-ResourceGroupName</span></span>
<span data-ttu-id="c3d14-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c3d14-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3d14-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3d14-128">-ResourceId</span></span>
<span data-ttu-id="c3d14-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c3d14-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c3d14-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3d14-130">-Confirm</span></span>
<span data-ttu-id="c3d14-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3d14-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d14-132">-WhatIf</span></span>
<span data-ttu-id="c3d14-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3d14-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d14-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3d14-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d14-135">CommonParameters</span></span>
<span data-ttu-id="c3d14-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d14-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d14-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d14-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3d14-138">INPUTS</span></span>

### <span data-ttu-id="c3d14-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="c3d14-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="c3d14-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d14-140">System.String</span></span>

## <span data-ttu-id="c3d14-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3d14-141">OUTPUTS</span></span>

### <span data-ttu-id="c3d14-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="c3d14-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="c3d14-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3d14-143">NOTES</span></span>

## <span data-ttu-id="c3d14-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3d14-144">RELATED LINKS</span></span>
