---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298392"
---
# <span data-ttu-id="e8490-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="e8490-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="e8490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8490-102">SYNOPSIS</span></span>
<span data-ttu-id="e8490-103">Löschen Sie einen verknüpften IoT-Hub in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e8490-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e8490-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8490-104">SYNTAX</span></span>

### <span data-ttu-id="e8490-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8490-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8490-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8490-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8490-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8490-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8490-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8490-108">DESCRIPTION</span></span>
<span data-ttu-id="e8490-109">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e8490-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e8490-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8490-110">EXAMPLES</span></span>

### <span data-ttu-id="e8490-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8490-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="e8490-112">Löschen Sie den verknüpften IoT-Hub "myiothub" in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e8490-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="e8490-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e8490-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="e8490-114">Löschen Sie den verknüpften "myiothub"-IoT-Hub in einem Azure IoT Hub-Gerätebereitstellungsdienst mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8490-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="e8490-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8490-115">PARAMETERS</span></span>

### <span data-ttu-id="e8490-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8490-116">-DefaultProfile</span></span>
<span data-ttu-id="e8490-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8490-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8490-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8490-118">-InputObject</span></span>
<span data-ttu-id="e8490-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="e8490-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e8490-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="e8490-120">-LinkedHubName</span></span>
<span data-ttu-id="e8490-121">Hostname des verknüpften IoT Hubs</span><span class="sxs-lookup"><span data-stu-id="e8490-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="e8490-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8490-122">-Name</span></span>
<span data-ttu-id="e8490-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="e8490-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e8490-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8490-124">-PassThru</span></span>
<span data-ttu-id="e8490-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e8490-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e8490-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8490-126">-ResourceGroupName</span></span>
<span data-ttu-id="e8490-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e8490-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e8490-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8490-128">-ResourceId</span></span>
<span data-ttu-id="e8490-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="e8490-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e8490-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8490-130">-Confirm</span></span>
<span data-ttu-id="e8490-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8490-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8490-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e8490-132">-WhatIf</span></span>
<span data-ttu-id="e8490-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8490-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8490-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8490-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8490-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8490-135">CommonParameters</span></span>
<span data-ttu-id="e8490-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8490-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8490-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8490-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8490-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8490-138">INPUTS</span></span>

### <span data-ttu-id="e8490-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="e8490-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="e8490-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e8490-140">System.String</span></span>

## <span data-ttu-id="e8490-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8490-141">OUTPUTS</span></span>

### <span data-ttu-id="e8490-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8490-142">System.Boolean</span></span>

## <span data-ttu-id="e8490-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8490-143">NOTES</span></span>

## <span data-ttu-id="e8490-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8490-144">RELATED LINKS</span></span>
