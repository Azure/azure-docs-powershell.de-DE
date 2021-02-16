---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163609"
---
# <span data-ttu-id="205fd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="205fd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="205fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205fd-102">SYNOPSIS</span></span>
<span data-ttu-id="205fd-103">Löscht die Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="205fd-103">Deletes the device registration.</span></span>

## <span data-ttu-id="205fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="205fd-104">SYNTAX</span></span>

### <span data-ttu-id="205fd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="205fd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="205fd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="205fd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="205fd-108">DESCRIPTION</span></span>
<span data-ttu-id="205fd-109">Löschen Sie eine Geräteregistrierung in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="205fd-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="205fd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="205fd-110">EXAMPLES</span></span>

### <span data-ttu-id="205fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="205fd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="205fd-112">Löschen Sie eine Geräteregistrierung in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="205fd-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="205fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="205fd-113">PARAMETERS</span></span>

### <span data-ttu-id="205fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205fd-114">-DefaultProfile</span></span>
<span data-ttu-id="205fd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="205fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205fd-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="205fd-116">-DpsName</span></span>
<span data-ttu-id="205fd-117">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="205fd-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="205fd-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="205fd-118">-DpsObject</span></span>
<span data-ttu-id="205fd-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="205fd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="205fd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="205fd-120">-PassThru</span></span>
<span data-ttu-id="205fd-121">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="205fd-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="205fd-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="205fd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="205fd-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="205fd-123">-RegistrationId</span></span>
<span data-ttu-id="205fd-124">ID der Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="205fd-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="205fd-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="205fd-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="205fd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="205fd-127">-ResourceId</span></span>
<span data-ttu-id="205fd-128">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="205fd-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="205fd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="205fd-129">-Confirm</span></span>
<span data-ttu-id="205fd-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="205fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205fd-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="205fd-131">-WhatIf</span></span>
<span data-ttu-id="205fd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="205fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205fd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="205fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205fd-134">CommonParameters</span></span>
<span data-ttu-id="205fd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205fd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205fd-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="205fd-137">INPUTS</span></span>

### <span data-ttu-id="205fd-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="205fd-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="205fd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="205fd-139">System.String</span></span>

## <span data-ttu-id="205fd-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="205fd-140">OUTPUTS</span></span>

### <span data-ttu-id="205fd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="205fd-141">System.Boolean</span></span>

## <span data-ttu-id="205fd-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="205fd-142">NOTES</span></span>

## <span data-ttu-id="205fd-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="205fd-143">RELATED LINKS</span></span>
