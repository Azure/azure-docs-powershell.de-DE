---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175601"
---
# <span data-ttu-id="af989-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="af989-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="af989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af989-102">SYNOPSIS</span></span>
<span data-ttu-id="af989-103">Löschen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="af989-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="af989-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af989-104">SYNTAX</span></span>

### <span data-ttu-id="af989-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af989-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af989-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af989-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af989-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af989-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af989-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af989-108">DESCRIPTION</span></span>
<span data-ttu-id="af989-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="af989-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="af989-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af989-110">EXAMPLES</span></span>

### <span data-ttu-id="af989-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af989-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="af989-112">Löschen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="af989-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="af989-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="af989-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="af989-114">Löschen Sie einen Azure IoT Hub-Gerätebereitstellungsdienst "myiotdps" mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="af989-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="af989-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af989-115">PARAMETERS</span></span>

### <span data-ttu-id="af989-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af989-116">-DefaultProfile</span></span>
<span data-ttu-id="af989-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af989-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af989-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af989-118">-InputObject</span></span>
<span data-ttu-id="af989-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="af989-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="af989-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af989-120">-Name</span></span>
<span data-ttu-id="af989-121">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="af989-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="af989-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af989-122">-PassThru</span></span>
<span data-ttu-id="af989-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="af989-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="af989-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af989-124">-ResourceGroupName</span></span>
<span data-ttu-id="af989-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="af989-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af989-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af989-126">-ResourceId</span></span>
<span data-ttu-id="af989-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="af989-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="af989-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af989-128">-Confirm</span></span>
<span data-ttu-id="af989-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af989-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af989-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="af989-130">-WhatIf</span></span>
<span data-ttu-id="af989-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af989-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af989-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af989-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af989-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af989-133">CommonParameters</span></span>
<span data-ttu-id="af989-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af989-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af989-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af989-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af989-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af989-136">INPUTS</span></span>

### <span data-ttu-id="af989-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="af989-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="af989-138">System.String</span><span class="sxs-lookup"><span data-stu-id="af989-138">System.String</span></span>

## <span data-ttu-id="af989-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af989-139">OUTPUTS</span></span>

### <span data-ttu-id="af989-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af989-140">System.Boolean</span></span>

## <span data-ttu-id="af989-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af989-141">NOTES</span></span>

## <span data-ttu-id="af989-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af989-142">RELATED LINKS</span></span>
