---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ae7335c6430001affa76894dac6334036d1f04d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661117"
---
# <span data-ttu-id="c268f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="c268f-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="c268f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c268f-102">SYNOPSIS</span></span>
<span data-ttu-id="c268f-103">Löschen eines verknüpften viele-Hubs in einem Azure-viel-Hub-Device-Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="c268f-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c268f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c268f-104">SYNTAX</span></span>

### <span data-ttu-id="c268f-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c268f-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c268f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c268f-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c268f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c268f-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c268f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c268f-108">DESCRIPTION</span></span>
<span data-ttu-id="c268f-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c268f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c268f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c268f-110">EXAMPLES</span></span>

### <span data-ttu-id="c268f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c268f-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="c268f-112">Löschen des verknüpften viel-Hubs "myiothub" in einem Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c268f-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c268f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c268f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="c268f-114">Löschen Sie den verknüpften viel-Hub "myiothub" in einem Azure-to-Hub-Device-Bereitstellungsdienst mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c268f-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="c268f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c268f-115">PARAMETERS</span></span>

### <span data-ttu-id="c268f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c268f-116">-DefaultProfile</span></span>
<span data-ttu-id="c268f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c268f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c268f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c268f-118">-InputObject</span></span>
<span data-ttu-id="c268f-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="c268f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c268f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="c268f-120">-LinkedHubName</span></span>
<span data-ttu-id="c268f-121">Hostname des verknüpften Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="c268f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="c268f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c268f-122">-Name</span></span>
<span data-ttu-id="c268f-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c268f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c268f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c268f-124">-PassThru</span></span>
<span data-ttu-id="c268f-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c268f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c268f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c268f-126">-ResourceGroupName</span></span>
<span data-ttu-id="c268f-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c268f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c268f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c268f-128">-ResourceId</span></span>
<span data-ttu-id="c268f-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c268f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c268f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c268f-130">-Confirm</span></span>
<span data-ttu-id="c268f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c268f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c268f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c268f-132">-WhatIf</span></span>
<span data-ttu-id="c268f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c268f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c268f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c268f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c268f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c268f-135">CommonParameters</span></span>
<span data-ttu-id="c268f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c268f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c268f-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c268f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c268f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c268f-138">INPUTS</span></span>

### <span data-ttu-id="c268f-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="c268f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="c268f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c268f-140">System.String</span></span>

## <span data-ttu-id="c268f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c268f-141">OUTPUTS</span></span>

### <span data-ttu-id="c268f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c268f-142">System.Boolean</span></span>

## <span data-ttu-id="c268f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="c268f-143">NOTES</span></span>

## <span data-ttu-id="c268f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c268f-144">RELATED LINKS</span></span>
