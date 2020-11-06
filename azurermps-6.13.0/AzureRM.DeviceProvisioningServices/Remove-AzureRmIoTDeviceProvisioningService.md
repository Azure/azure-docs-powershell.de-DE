---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482462"
---
# <span data-ttu-id="bb114-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="bb114-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="bb114-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb114-102">SYNOPSIS</span></span>
<span data-ttu-id="bb114-103">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="bb114-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb114-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb114-104">SYNTAX</span></span>

### <span data-ttu-id="bb114-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb114-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb114-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb114-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb114-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb114-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb114-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb114-108">DESCRIPTION</span></span>
<span data-ttu-id="bb114-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="bb114-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="bb114-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb114-110">EXAMPLES</span></span>

### <span data-ttu-id="bb114-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb114-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="bb114-112">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="bb114-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="bb114-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb114-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="bb114-114">Löschen Sie einen Azure-viel-Hub-Device-Bereitstellungsdienst "myiotdps" mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb114-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="bb114-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb114-115">PARAMETERS</span></span>

### <span data-ttu-id="bb114-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb114-116">-DefaultProfile</span></span>
<span data-ttu-id="bb114-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb114-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb114-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb114-118">-InputObject</span></span>
<span data-ttu-id="bb114-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="bb114-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bb114-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bb114-120">-Name</span></span>
<span data-ttu-id="bb114-121">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="bb114-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bb114-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb114-122">-PassThru</span></span>
<span data-ttu-id="bb114-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bb114-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bb114-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb114-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb114-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bb114-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb114-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bb114-126">-ResourceId</span></span>
<span data-ttu-id="bb114-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="bb114-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bb114-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb114-128">-Confirm</span></span>
<span data-ttu-id="bb114-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb114-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb114-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb114-130">-WhatIf</span></span>
<span data-ttu-id="bb114-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb114-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb114-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb114-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb114-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb114-133">CommonParameters</span></span>
<span data-ttu-id="bb114-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb114-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb114-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb114-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb114-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb114-136">INPUTS</span></span>

### <span data-ttu-id="bb114-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bb114-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="bb114-138">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb114-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bb114-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bb114-139">System.String</span></span>

## <span data-ttu-id="bb114-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb114-140">OUTPUTS</span></span>

### <span data-ttu-id="bb114-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb114-141">System.Boolean</span></span>

## <span data-ttu-id="bb114-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb114-142">NOTES</span></span>

## <span data-ttu-id="bb114-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb114-143">RELATED LINKS</span></span>
