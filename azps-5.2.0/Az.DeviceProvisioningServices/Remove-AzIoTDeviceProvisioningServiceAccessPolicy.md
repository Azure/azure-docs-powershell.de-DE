---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298411"
---
# <span data-ttu-id="98678-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98678-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="98678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98678-102">SYNOPSIS</span></span>
<span data-ttu-id="98678-103">Löschen Sie eine freigegebene Zugriffsrichtlinien in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="98678-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="98678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98678-104">SYNTAX</span></span>

### <span data-ttu-id="98678-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="98678-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98678-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="98678-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98678-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="98678-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98678-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98678-108">DESCRIPTION</span></span>
<span data-ttu-id="98678-109">Eine Einführung in den Azure IoT Hub Device Provisioning Service finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="98678-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="98678-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98678-110">EXAMPLES</span></span>

### <span data-ttu-id="98678-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98678-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="98678-112">Löschen sie die Richtlinie "mypolicy" für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="98678-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="98678-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98678-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="98678-114">Löschen Sie die Richtlinie "mypolicy" für den freigegebenen Zugriff in einem Azure IoT Hub-Gerätebereitstellungsdienst mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="98678-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="98678-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98678-115">PARAMETERS</span></span>

### <span data-ttu-id="98678-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98678-116">-DefaultProfile</span></span>
<span data-ttu-id="98678-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98678-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98678-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98678-118">-InputObject</span></span>
<span data-ttu-id="98678-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="98678-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="98678-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="98678-120">-KeyName</span></span>
<span data-ttu-id="98678-121">Name der Zugriffsrichtlinie für die IoT-Gerätebereitstellungsdienst-Zugriffsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="98678-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="98678-122">-Name</span><span class="sxs-lookup"><span data-stu-id="98678-122">-Name</span></span>
<span data-ttu-id="98678-123">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="98678-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="98678-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98678-124">-PassThru</span></span>
<span data-ttu-id="98678-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="98678-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="98678-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98678-126">-ResourceGroupName</span></span>
<span data-ttu-id="98678-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="98678-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="98678-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98678-128">-ResourceId</span></span>
<span data-ttu-id="98678-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="98678-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="98678-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98678-130">-Confirm</span></span>
<span data-ttu-id="98678-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98678-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98678-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="98678-132">-WhatIf</span></span>
<span data-ttu-id="98678-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98678-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98678-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98678-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98678-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98678-135">CommonParameters</span></span>
<span data-ttu-id="98678-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98678-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98678-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98678-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98678-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98678-138">INPUTS</span></span>

### <span data-ttu-id="98678-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="98678-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="98678-140">System.String</span><span class="sxs-lookup"><span data-stu-id="98678-140">System.String</span></span>

## <span data-ttu-id="98678-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98678-141">OUTPUTS</span></span>

### <span data-ttu-id="98678-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98678-142">System.Boolean</span></span>

## <span data-ttu-id="98678-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="98678-143">NOTES</span></span>

## <span data-ttu-id="98678-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="98678-144">RELATED LINKS</span></span>
