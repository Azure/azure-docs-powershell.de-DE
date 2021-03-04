---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 9b27875e19837d7e3b69770234bdcd19648c3130
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935251"
---
# <span data-ttu-id="60a2a-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="60a2a-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="60a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="60a2a-103">Löschen Sie eine Geräteregistrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="60a2a-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="60a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60a2a-104">SYNTAX</span></span>

### <span data-ttu-id="60a2a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60a2a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a2a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="60a2a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a2a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60a2a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a2a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="60a2a-109">Löschen Sie eine Registrierungsgruppe in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="60a2a-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="60a2a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60a2a-110">EXAMPLES</span></span>

### <span data-ttu-id="60a2a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60a2a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="60a2a-112">Löschen Sie eine angegebene Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="60a2a-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="60a2a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="60a2a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="60a2a-114">Löschen Sie alle Registrierungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="60a2a-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="60a2a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="60a2a-115">PARAMETERS</span></span>

### <span data-ttu-id="60a2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a2a-116">-DefaultProfile</span></span>
<span data-ttu-id="60a2a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60a2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a2a-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="60a2a-118">-DpsName</span></span>
<span data-ttu-id="60a2a-119">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="60a2a-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="60a2a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="60a2a-120">-DpsObject</span></span>
<span data-ttu-id="60a2a-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="60a2a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="60a2a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="60a2a-122">-Name</span></span>
<span data-ttu-id="60a2a-123">Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="60a2a-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="60a2a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60a2a-124">-PassThru</span></span>
<span data-ttu-id="60a2a-125">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="60a2a-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="60a2a-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="60a2a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60a2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="60a2a-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="60a2a-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="60a2a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a2a-129">-ResourceId</span></span>
<span data-ttu-id="60a2a-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="60a2a-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="60a2a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60a2a-131">-Confirm</span></span>
<span data-ttu-id="60a2a-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60a2a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a2a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a2a-133">-WhatIf</span></span>
<span data-ttu-id="60a2a-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60a2a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a2a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60a2a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a2a-136">CommonParameters</span></span>
<span data-ttu-id="60a2a-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a2a-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a2a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a2a-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60a2a-139">INPUTS</span></span>

### <span data-ttu-id="60a2a-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="60a2a-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="60a2a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="60a2a-141">System.String</span></span>

## <span data-ttu-id="60a2a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60a2a-142">OUTPUTS</span></span>

### <span data-ttu-id="60a2a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60a2a-143">System.Boolean</span></span>

## <span data-ttu-id="60a2a-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="60a2a-144">NOTES</span></span>

## <span data-ttu-id="60a2a-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="60a2a-145">RELATED LINKS</span></span>
