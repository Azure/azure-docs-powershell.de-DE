---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 2da931326b9f900dbf3af3cfcb2e504b413cef33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651269"
---
# <span data-ttu-id="16e5d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="16e5d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="16e5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="16e5d-103">Aktualisieren einer gemeinsamen Zugriffsrichtlinie in einem Azure viel-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="16e5d-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="16e5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e5d-104">SYNTAX</span></span>

### <span data-ttu-id="16e5d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="16e5d-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16e5d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16e5d-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e5d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16e5d-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e5d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16e5d-108">DESCRIPTION</span></span>
<span data-ttu-id="16e5d-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="16e5d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="16e5d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16e5d-110">EXAMPLES</span></span>

### <span data-ttu-id="16e5d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16e5d-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="16e5d-112">Update-Zugriffsrichtlinie "MyPolicy" in einem Azure-viel-Hub-Device-Bereitstellungsdienst mit EnrollmentWrite right.</span><span class="sxs-lookup"><span data-stu-id="16e5d-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="16e5d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16e5d-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="16e5d-114">Update-Zugriffsrichtlinie "MyPolicy" in einem Azure-viel-Hub-Device-Bereitstellungsdienst mit EnrollmentWrite right mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="16e5d-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="16e5d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e5d-115">PARAMETERS</span></span>

### <span data-ttu-id="16e5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e5d-116">-DefaultProfile</span></span>
<span data-ttu-id="16e5d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16e5d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e5d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16e5d-118">-InputObject</span></span>
<span data-ttu-id="16e5d-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="16e5d-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="16e5d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="16e5d-120">-KeyName</span></span>
<span data-ttu-id="16e5d-121">Dienstzugriffs Richtlinien-Schlüsselname für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="16e5d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="16e5d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16e5d-122">-Name</span></span>
<span data-ttu-id="16e5d-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="16e5d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="16e5d-124">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="16e5d-124">-Permissions</span></span>
<span data-ttu-id="16e5d-125">Zugriffsrichtlinien Berechtigungen für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="16e5d-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="16e5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="16e5d-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="16e5d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16e5d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16e5d-128">-ResourceId</span></span>
<span data-ttu-id="16e5d-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="16e5d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="16e5d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16e5d-130">-Confirm</span></span>
<span data-ttu-id="16e5d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16e5d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e5d-132">-WhatIf</span></span>
<span data-ttu-id="16e5d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16e5d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e5d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16e5d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e5d-135">CommonParameters</span></span>
<span data-ttu-id="16e5d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e5d-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e5d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e5d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16e5d-138">INPUTS</span></span>

### <span data-ttu-id="16e5d-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="16e5d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="16e5d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="16e5d-140">System.String</span></span>

## <span data-ttu-id="16e5d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16e5d-141">OUTPUTS</span></span>

### <span data-ttu-id="16e5d-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="16e5d-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="16e5d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="16e5d-143">NOTES</span></span>

## <span data-ttu-id="16e5d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16e5d-144">RELATED LINKS</span></span>
