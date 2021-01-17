---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302515"
---
# <span data-ttu-id="0a730-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a730-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0a730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a730-102">SYNOPSIS</span></span>
<span data-ttu-id="0a730-103">Aktualisieren sie eine Richtlinie für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="0a730-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0a730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a730-104">SYNTAX</span></span>

### <span data-ttu-id="0a730-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a730-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a730-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0a730-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a730-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0a730-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a730-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a730-108">DESCRIPTION</span></span>
<span data-ttu-id="0a730-109">Eine Einführung in den Bereitstellungsdienst für Azure IoT-Hub-Geräte finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0a730-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0a730-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a730-110">EXAMPLES</span></span>

### <span data-ttu-id="0a730-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a730-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="0a730-112">Aktualisieren Sie die Zugriffsrichtlinie "mypolicy" in einem Azure IoT Hub-Gerätebereitstellungsdienst mit RegistrierungSWrite rechts.</span><span class="sxs-lookup"><span data-stu-id="0a730-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="0a730-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a730-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="0a730-114">Aktualisieren Sie die Zugriffsrichtlinie "mypolicy" in einem Azure IoT Hub-Gerätebereitstellungsdienst mit RegistrierungSWrite direkt über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a730-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="0a730-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a730-115">PARAMETERS</span></span>

### <span data-ttu-id="0a730-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a730-116">-DefaultProfile</span></span>
<span data-ttu-id="0a730-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a730-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a730-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a730-118">-InputObject</span></span>
<span data-ttu-id="0a730-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="0a730-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0a730-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0a730-120">-KeyName</span></span>
<span data-ttu-id="0a730-121">Name der Zugriffsrichtlinie für die IoT-Gerätebereitstellungsdienst-Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0a730-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0a730-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0a730-122">-Name</span></span>
<span data-ttu-id="0a730-123">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="0a730-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0a730-124">-Permissions</span><span class="sxs-lookup"><span data-stu-id="0a730-124">-Permissions</span></span>
<span data-ttu-id="0a730-125">Zugriffsrichtlinienberechtigungen für die IoT-Gerätebereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="0a730-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="0a730-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a730-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a730-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0a730-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0a730-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a730-128">-ResourceId</span></span>
<span data-ttu-id="0a730-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="0a730-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0a730-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a730-130">-Confirm</span></span>
<span data-ttu-id="0a730-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a730-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a730-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a730-132">-WhatIf</span></span>
<span data-ttu-id="0a730-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a730-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a730-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a730-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a730-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a730-135">CommonParameters</span></span>
<span data-ttu-id="0a730-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a730-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a730-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a730-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a730-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a730-138">INPUTS</span></span>

### <span data-ttu-id="0a730-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0a730-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="0a730-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0a730-140">System.String</span></span>

## <span data-ttu-id="0a730-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a730-141">OUTPUTS</span></span>

### <span data-ttu-id="0a730-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0a730-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="0a730-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a730-143">NOTES</span></span>

## <span data-ttu-id="0a730-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a730-144">RELATED LINKS</span></span>
