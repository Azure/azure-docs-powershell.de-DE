---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: fc1b8bbe14fb35e7613ac1ed09ecf87624920081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935240"
---
# <span data-ttu-id="5d130-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5d130-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5d130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d130-102">SYNOPSIS</span></span>
<span data-ttu-id="5d130-103">Löschen Sie einen verknüpften IoT-Hub in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5d130-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5d130-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d130-104">SYNTAX</span></span>

### <span data-ttu-id="5d130-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d130-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d130-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d130-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d130-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d130-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d130-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d130-108">DESCRIPTION</span></span>
<span data-ttu-id="5d130-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5d130-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5d130-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d130-110">EXAMPLES</span></span>

### <span data-ttu-id="5d130-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d130-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="5d130-112">Löschen Sie den verknüpften IoT-Hub "myiothub" in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5d130-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5d130-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d130-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="5d130-114">Löschen Sie den verknüpften IoT-Hub "myiothub" in einem Azure IoT Hub-Gerätebereitstellungsdienst mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d130-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="5d130-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5d130-115">PARAMETERS</span></span>

### <span data-ttu-id="5d130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d130-116">-DefaultProfile</span></span>
<span data-ttu-id="5d130-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d130-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d130-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d130-118">-InputObject</span></span>
<span data-ttu-id="5d130-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="5d130-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5d130-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5d130-120">-LinkedHubName</span></span>
<span data-ttu-id="5d130-121">Hostname des verknüpften IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5d130-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5d130-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5d130-122">-Name</span></span>
<span data-ttu-id="5d130-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5d130-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5d130-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d130-124">-PassThru</span></span>
<span data-ttu-id="5d130-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d130-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d130-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d130-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d130-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5d130-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5d130-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d130-128">-ResourceId</span></span>
<span data-ttu-id="5d130-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5d130-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5d130-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d130-130">-Confirm</span></span>
<span data-ttu-id="5d130-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d130-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d130-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d130-132">-WhatIf</span></span>
<span data-ttu-id="5d130-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d130-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d130-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d130-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d130-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d130-135">CommonParameters</span></span>
<span data-ttu-id="5d130-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d130-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d130-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d130-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d130-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d130-138">INPUTS</span></span>

### <span data-ttu-id="5d130-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5d130-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5d130-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5d130-140">System.String</span></span>

## <span data-ttu-id="5d130-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d130-141">OUTPUTS</span></span>

### <span data-ttu-id="5d130-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d130-142">System.Boolean</span></span>

## <span data-ttu-id="5d130-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5d130-143">NOTES</span></span>

## <span data-ttu-id="5d130-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5d130-144">RELATED LINKS</span></span>
