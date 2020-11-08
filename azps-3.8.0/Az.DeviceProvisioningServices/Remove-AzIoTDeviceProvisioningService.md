---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996613"
---
# <span data-ttu-id="32af6-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="32af6-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="32af6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32af6-102">SYNOPSIS</span></span>
<span data-ttu-id="32af6-103">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="32af6-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="32af6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32af6-104">SYNTAX</span></span>

### <span data-ttu-id="32af6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32af6-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32af6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="32af6-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32af6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="32af6-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32af6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32af6-108">DESCRIPTION</span></span>
<span data-ttu-id="32af6-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="32af6-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="32af6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32af6-110">EXAMPLES</span></span>

### <span data-ttu-id="32af6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32af6-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="32af6-112">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="32af6-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="32af6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32af6-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="32af6-114">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst "myiotdps" mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="32af6-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="32af6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="32af6-115">PARAMETERS</span></span>

### <span data-ttu-id="32af6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32af6-116">-DefaultProfile</span></span>
<span data-ttu-id="32af6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32af6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32af6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32af6-118">-InputObject</span></span>
<span data-ttu-id="32af6-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="32af6-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="32af6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="32af6-120">-Name</span></span>
<span data-ttu-id="32af6-121">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="32af6-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="32af6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32af6-122">-PassThru</span></span>
<span data-ttu-id="32af6-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="32af6-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32af6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32af6-124">-ResourceGroupName</span></span>
<span data-ttu-id="32af6-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="32af6-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="32af6-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="32af6-126">-ResourceId</span></span>
<span data-ttu-id="32af6-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="32af6-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="32af6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32af6-128">-Confirm</span></span>
<span data-ttu-id="32af6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32af6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32af6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32af6-130">-WhatIf</span></span>
<span data-ttu-id="32af6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32af6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32af6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32af6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32af6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32af6-133">CommonParameters</span></span>
<span data-ttu-id="32af6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32af6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32af6-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32af6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32af6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32af6-136">INPUTS</span></span>

### <span data-ttu-id="32af6-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="32af6-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="32af6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="32af6-138">System.String</span></span>

## <span data-ttu-id="32af6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32af6-139">OUTPUTS</span></span>

### <span data-ttu-id="32af6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32af6-140">System.Boolean</span></span>

## <span data-ttu-id="32af6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="32af6-141">NOTES</span></span>

## <span data-ttu-id="32af6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32af6-142">RELATED LINKS</span></span>
