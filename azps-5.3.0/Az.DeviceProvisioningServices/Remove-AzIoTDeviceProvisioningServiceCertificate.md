---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458796"
---
# <span data-ttu-id="92925-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="92925-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="92925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92925-102">SYNOPSIS</span></span>
<span data-ttu-id="92925-103">Löschen Sie ein Azure IoT Hub Device Provisioning Service-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="92925-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="92925-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92925-104">SYNTAX</span></span>

### <span data-ttu-id="92925-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92925-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92925-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92925-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92925-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92925-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92925-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92925-108">DESCRIPTION</span></span>
<span data-ttu-id="92925-109">Eine ausführliche Erläuterung der Zertifizierungsstellenzertifikate im Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="92925-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="92925-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92925-110">EXAMPLES</span></span>

### <span data-ttu-id="92925-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92925-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="92925-112">Löschen Sie "mycertificate" in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="92925-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="92925-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92925-113">PARAMETERS</span></span>

### <span data-ttu-id="92925-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="92925-114">-CertificateName</span></span>
<span data-ttu-id="92925-115">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="92925-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92925-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92925-116">-DefaultProfile</span></span>
<span data-ttu-id="92925-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92925-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92925-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="92925-118">-Etag</span></span>
<span data-ttu-id="92925-119">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="92925-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="92925-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92925-120">-InputObject</span></span>
<span data-ttu-id="92925-121">IoT Device Provisioning Service Certificate Object</span><span class="sxs-lookup"><span data-stu-id="92925-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92925-122">-Name</span><span class="sxs-lookup"><span data-stu-id="92925-122">-Name</span></span>
<span data-ttu-id="92925-123">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="92925-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="92925-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92925-124">-PassThru</span></span>
<span data-ttu-id="92925-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="92925-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="92925-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92925-126">-ResourceGroupName</span></span>
<span data-ttu-id="92925-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="92925-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92925-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92925-128">-ResourceId</span></span>
<span data-ttu-id="92925-129">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="92925-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="92925-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92925-130">-Confirm</span></span>
<span data-ttu-id="92925-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92925-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92925-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="92925-132">-WhatIf</span></span>
<span data-ttu-id="92925-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92925-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92925-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92925-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92925-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92925-135">CommonParameters</span></span>
<span data-ttu-id="92925-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92925-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92925-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92925-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92925-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92925-138">INPUTS</span></span>

### <span data-ttu-id="92925-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="92925-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="92925-140">System.String</span><span class="sxs-lookup"><span data-stu-id="92925-140">System.String</span></span>

## <span data-ttu-id="92925-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92925-141">OUTPUTS</span></span>

### <span data-ttu-id="92925-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92925-142">System.Boolean</span></span>

## <span data-ttu-id="92925-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="92925-143">NOTES</span></span>

## <span data-ttu-id="92925-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="92925-144">RELATED LINKS</span></span>
