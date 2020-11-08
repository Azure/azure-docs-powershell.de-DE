---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008513"
---
# <span data-ttu-id="8bfe4-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bfe4-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="8bfe4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bfe4-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfe4-103">Fügen Sie eine neue freigegebene Zugriffsrichtlinie in einem Azure viel Hub-Device-Bereitstellungsdienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8bfe4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bfe4-104">SYNTAX</span></span>

### <span data-ttu-id="8bfe4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bfe4-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bfe4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bfe4-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bfe4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bfe4-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bfe4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bfe4-108">DESCRIPTION</span></span>
<span data-ttu-id="8bfe4-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8bfe4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8bfe4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bfe4-110">EXAMPLES</span></span>

### <span data-ttu-id="8bfe4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bfe4-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="8bfe4-112">Fügen Sie eine neue freigegebene Zugriffsrichtlinie in einem Azure viel Hub-Device-Bereitstellungsdienst mit EnrollmentWrite-und ServiceConfig-rechten hinzu.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="8bfe4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8bfe4-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="8bfe4-114">Fügen Sie eine neue freigegebene Zugriffsrichtlinie in einem Azure viel Hub-Device-Bereitstellungsdienst mit EnrollmentRead right hinzu.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="8bfe4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bfe4-115">PARAMETERS</span></span>

### <span data-ttu-id="8bfe4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfe4-116">-DefaultProfile</span></span>
<span data-ttu-id="8bfe4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bfe4-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8bfe4-118">-DpsObject</span></span>
<span data-ttu-id="8bfe4-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="8bfe4-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8bfe4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8bfe4-120">-KeyName</span></span>
<span data-ttu-id="8bfe4-121">Dienstzugriffs Richtlinien-Schlüsselname für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="8bfe4-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bfe4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8bfe4-122">-Name</span></span>
<span data-ttu-id="8bfe4-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="8bfe4-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8bfe4-124">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="8bfe4-124">-Permissions</span></span>
<span data-ttu-id="8bfe4-125">Zugriffsrichtlinien Berechtigungen für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="8bfe4-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="8bfe4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bfe4-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bfe4-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8bfe4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8bfe4-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8bfe4-128">-ResourceId</span></span>
<span data-ttu-id="8bfe4-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="8bfe4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8bfe4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bfe4-130">-Confirm</span></span>
<span data-ttu-id="8bfe4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bfe4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bfe4-132">-WhatIf</span></span>
<span data-ttu-id="8bfe4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bfe4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bfe4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfe4-135">CommonParameters</span></span>
<span data-ttu-id="8bfe4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bfe4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfe4-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bfe4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfe4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bfe4-138">INPUTS</span></span>

### <span data-ttu-id="8bfe4-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8bfe4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8bfe4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8bfe4-140">System.String</span></span>

## <span data-ttu-id="8bfe4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bfe4-141">OUTPUTS</span></span>

### <span data-ttu-id="8bfe4-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="8bfe4-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="8bfe4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bfe4-143">NOTES</span></span>

## <span data-ttu-id="8bfe4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bfe4-144">RELATED LINKS</span></span>
