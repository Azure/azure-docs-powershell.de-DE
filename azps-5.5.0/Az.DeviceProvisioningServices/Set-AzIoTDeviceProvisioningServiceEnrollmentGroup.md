---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161708"
---
# <span data-ttu-id="8c0e4-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="8c0e4-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="8c0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0e4-103">Aktualisieren Sie eine Geräteregistrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="8c0e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c0e4-104">SYNTAX</span></span>

### <span data-ttu-id="8c0e4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c0e4-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c0e4-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c0e4-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0e4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c0e4-108">DESCRIPTION</span></span>
<span data-ttu-id="8c0e4-109">Aktualisieren Sie eine Registrierungsgruppe in einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8c0e4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c0e4-110">EXAMPLES</span></span>

### <span data-ttu-id="8c0e4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c0e4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="8c0e4-112">Aktualisieren Sie die Zuweisungsrichtlinie und Hubs für eine Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="8c0e4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c0e4-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="8c0e4-114">Aktualisieren Sie den anfänglichen Status einer Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="8c0e4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c0e4-115">PARAMETERS</span></span>

### <span data-ttu-id="8c0e4-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="8c0e4-116">-AllocationPolicy</span></span>
<span data-ttu-id="8c0e4-117">Der Typ der Zuordnung für das dem Hub zugewiesene Gerät.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-117">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c0e4-118">-ApiVersion</span></span>
<span data-ttu-id="8c0e4-119">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="8c0e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0e4-120">-DefaultProfile</span></span>
<span data-ttu-id="8c0e4-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c0e4-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="8c0e4-122">-Desired</span></span>
<span data-ttu-id="8c0e4-123">Initiale gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-123">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="8c0e4-124">-DpsName</span></span>
<span data-ttu-id="8c0e4-125">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="8c0e4-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8c0e4-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8c0e4-126">-DpsObject</span></span>
<span data-ttu-id="8c0e4-127">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="8c0e4-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8c0e4-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8c0e4-128">-EdgeEnabled</span></span>
<span data-ttu-id="8c0e4-129">Kennzeichnung zur Aktivierung der Kante.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="8c0e4-130">-IotHub</span></span>
<span data-ttu-id="8c0e4-131">Hostname des IoT-Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="8c0e4-132">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-132">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="8c0e4-133">-IotHubHostName</span></span>
<span data-ttu-id="8c0e4-134">Hostname des IoT-Zielhubs.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="8c0e4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="8c0e4-135">-Name</span></span>
<span data-ttu-id="8c0e4-136">Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="8c0e4-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="8c0e4-137">-ProvisioningStatus</span></span>
<span data-ttu-id="8c0e4-138">Registrierungseintrag aktivieren oder deaktivieren</span><span class="sxs-lookup"><span data-stu-id="8c0e4-138">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c0e4-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="8c0e4-140">Gerätedaten, die bei der erneuten Bereitstellung an einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0e4-141">-ResourceGroupName</span></span>
<span data-ttu-id="8c0e4-142">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8c0e4-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8c0e4-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0e4-143">-ResourceId</span></span>
<span data-ttu-id="8c0e4-144">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="8c0e4-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8c0e4-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c0e4-145">-Tag</span></span>
<span data-ttu-id="8c0e4-146">Initiale tags.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-146">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e4-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="8c0e4-147">-WebhookUrl</span></span>
<span data-ttu-id="8c0e4-148">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="8c0e4-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c0e4-149">-Confirm</span></span>
<span data-ttu-id="8c0e4-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0e4-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c0e4-151">-WhatIf</span></span>
<span data-ttu-id="8c0e4-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0e4-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0e4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0e4-154">CommonParameters</span></span>
<span data-ttu-id="8c0e4-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0e4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0e4-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c0e4-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0e4-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c0e4-157">INPUTS</span></span>

### <span data-ttu-id="8c0e4-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8c0e4-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8c0e4-159">System.String</span><span class="sxs-lookup"><span data-stu-id="8c0e4-159">System.String</span></span>

## <span data-ttu-id="8c0e4-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c0e4-160">OUTPUTS</span></span>

### <span data-ttu-id="8c0e4-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="8c0e4-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="8c0e4-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c0e4-162">NOTES</span></span>

## <span data-ttu-id="8c0e4-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c0e4-163">RELATED LINKS</span></span>
