---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376968"
---
# <span data-ttu-id="95138-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="95138-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="95138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95138-102">SYNOPSIS</span></span>
<span data-ttu-id="95138-103">Löschen eines Geräteregistrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="95138-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="95138-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95138-104">SYNTAX</span></span>

### <span data-ttu-id="95138-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95138-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95138-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="95138-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95138-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="95138-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95138-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95138-108">DESCRIPTION</span></span>
<span data-ttu-id="95138-109">Löschen Sie eine Geräteregistrierung bei einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="95138-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="95138-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95138-110">EXAMPLES</span></span>

### <span data-ttu-id="95138-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95138-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="95138-112">Löschen eines angegebenen Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="95138-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="95138-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95138-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="95138-114">Löschen Sie alle Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="95138-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="95138-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95138-115">PARAMETERS</span></span>

### <span data-ttu-id="95138-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95138-116">-DefaultProfile</span></span>
<span data-ttu-id="95138-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95138-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95138-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="95138-118">-DpsName</span></span>
<span data-ttu-id="95138-119">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="95138-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="95138-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="95138-120">-DpsObject</span></span>
<span data-ttu-id="95138-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="95138-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="95138-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95138-122">-PassThru</span></span>
<span data-ttu-id="95138-123">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="95138-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="95138-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="95138-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="95138-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="95138-125">-RegistrationId</span></span>
<span data-ttu-id="95138-126">Registrierungs-ID für die individuelle Registrierung.</span><span class="sxs-lookup"><span data-stu-id="95138-126">Individual enrollment registration id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95138-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95138-127">-ResourceGroupName</span></span>
<span data-ttu-id="95138-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="95138-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="95138-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95138-129">-ResourceId</span></span>
<span data-ttu-id="95138-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="95138-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="95138-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95138-131">-Confirm</span></span>
<span data-ttu-id="95138-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95138-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95138-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95138-133">-WhatIf</span></span>
<span data-ttu-id="95138-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95138-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95138-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95138-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95138-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95138-136">CommonParameters</span></span>
<span data-ttu-id="95138-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95138-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95138-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95138-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95138-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95138-139">INPUTS</span></span>

### <span data-ttu-id="95138-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="95138-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="95138-141">System.String</span><span class="sxs-lookup"><span data-stu-id="95138-141">System.String</span></span>

## <span data-ttu-id="95138-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95138-142">OUTPUTS</span></span>

### <span data-ttu-id="95138-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95138-143">System.Boolean</span></span>

## <span data-ttu-id="95138-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95138-144">NOTES</span></span>

## <span data-ttu-id="95138-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95138-145">RELATED LINKS</span></span>
