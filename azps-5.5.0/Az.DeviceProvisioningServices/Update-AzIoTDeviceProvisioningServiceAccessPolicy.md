---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161700"
---
# <span data-ttu-id="abe3e-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="abe3e-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="abe3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe3e-102">SYNOPSIS</span></span>
<span data-ttu-id="abe3e-103">Aktualisieren sie eine Richtlinie für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="abe3e-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="abe3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abe3e-104">SYNTAX</span></span>

### <span data-ttu-id="abe3e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="abe3e-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abe3e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="abe3e-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe3e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="abe3e-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe3e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abe3e-108">DESCRIPTION</span></span>
<span data-ttu-id="abe3e-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="abe3e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="abe3e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abe3e-110">EXAMPLES</span></span>

### <span data-ttu-id="abe3e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abe3e-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="abe3e-112">Aktualisieren Sie die Zugriffsrichtlinie "mypolicy" in einem Azure IoT Hub-Gerätebereitstellungsdienst mit RegistrierungSWrite rechts.</span><span class="sxs-lookup"><span data-stu-id="abe3e-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="abe3e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abe3e-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="abe3e-114">Aktualisieren Sie die Zugriffsrichtlinie "mypolicy" in einem Azure IoT Hub-Gerätebereitstellungsdienst mit EnrollmentWrite direkt über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="abe3e-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="abe3e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abe3e-115">PARAMETERS</span></span>

### <span data-ttu-id="abe3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe3e-116">-DefaultProfile</span></span>
<span data-ttu-id="abe3e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abe3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abe3e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abe3e-118">-InputObject</span></span>
<span data-ttu-id="abe3e-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="abe3e-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abe3e-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="abe3e-120">-KeyName</span></span>
<span data-ttu-id="abe3e-121">Name der Zugriffsrichtlinie für die IoT-Gerätebereitstellungsdienst-Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="abe3e-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="abe3e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="abe3e-122">-Name</span></span>
<span data-ttu-id="abe3e-123">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="abe3e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="abe3e-124">-Permissions</span><span class="sxs-lookup"><span data-stu-id="abe3e-124">-Permissions</span></span>
<span data-ttu-id="abe3e-125">Zugriffsrichtlinienberechtigungen für die IoT-Gerätebereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="abe3e-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe3e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe3e-126">-ResourceGroupName</span></span>
<span data-ttu-id="abe3e-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="abe3e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="abe3e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abe3e-128">-ResourceId</span></span>
<span data-ttu-id="abe3e-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="abe3e-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="abe3e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abe3e-130">-Confirm</span></span>
<span data-ttu-id="abe3e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abe3e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe3e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="abe3e-132">-WhatIf</span></span>
<span data-ttu-id="abe3e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abe3e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe3e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abe3e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe3e-135">CommonParameters</span></span>
<span data-ttu-id="abe3e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe3e-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe3e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe3e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abe3e-138">INPUTS</span></span>

### <span data-ttu-id="abe3e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="abe3e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="abe3e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="abe3e-140">System.String</span></span>

## <span data-ttu-id="abe3e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abe3e-141">OUTPUTS</span></span>

### <span data-ttu-id="abe3e-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="abe3e-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="abe3e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="abe3e-143">NOTES</span></span>

## <span data-ttu-id="abe3e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="abe3e-144">RELATED LINKS</span></span>
