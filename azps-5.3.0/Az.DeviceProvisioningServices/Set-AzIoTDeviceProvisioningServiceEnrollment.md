---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376927"
---
# <span data-ttu-id="d5a5a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="d5a5a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="d5a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a5a-103">Aktualisieren Sie einen Geräteregistrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="d5a5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a5a-104">SYNTAX</span></span>

### <span data-ttu-id="d5a5a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5a5a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5a5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5a5a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5a5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5a5a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a5a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="d5a5a-109">Aktualisieren Sie eine Geräteregistrierung bei einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d5a5a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="d5a5a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5a5a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="d5a5a-112">Aktualisieren Sie die Zuweisungsrichtlinie und Hubs für einen Registrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="d5a5a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5a5a-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="d5a5a-114">Aktualisieren Sie den anfänglichen Status einer Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="d5a5a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a5a-115">PARAMETERS</span></span>

### <span data-ttu-id="d5a5a-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a5a-116">-AllocationPolicy</span></span>
<span data-ttu-id="d5a5a-117">Der Typ der Zuordnung für das dem Hub zugewiesene Gerät.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="d5a5a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d5a5a-118">-ApiVersion</span></span>
<span data-ttu-id="d5a5a-119">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="d5a5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a5a-120">-DefaultProfile</span></span>
<span data-ttu-id="d5a5a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a5a-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="d5a5a-122">-Desired</span></span>
<span data-ttu-id="d5a5a-123">Anfangs gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="d5a5a-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d5a5a-124">-DeviceId</span></span>
<span data-ttu-id="d5a5a-125">IoT-Hub-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="d5a5a-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d5a5a-126">-DpsName</span></span>
<span data-ttu-id="d5a5a-127">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="d5a5a-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d5a5a-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d5a5a-128">-DpsObject</span></span>
<span data-ttu-id="d5a5a-129">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="d5a5a-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d5a5a-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="d5a5a-130">-EdgeEnabled</span></span>
<span data-ttu-id="d5a5a-131">Kennzeichnung zur Aktivierung der Kante.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="d5a5a-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d5a5a-132">-IotHub</span></span>
<span data-ttu-id="d5a5a-133">Hostname des IoT-Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="d5a5a-134">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="d5a5a-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="d5a5a-135">-IotHubHostName</span></span>
<span data-ttu-id="d5a5a-136">Hostname des IoT-Zielhubs.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="d5a5a-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="d5a5a-137">-ProvisioningStatus</span></span>
<span data-ttu-id="d5a5a-138">Registrierungseintrag aktivieren oder deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d5a5a-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="d5a5a-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="d5a5a-139">-RegistrationId</span></span>
<span data-ttu-id="d5a5a-140">Registrierungs-ID für die individuelle Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="d5a5a-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a5a-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="d5a5a-142">Gerätedaten, die bei der erneuten Bereitstellung an einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="d5a5a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a5a-143">-ResourceGroupName</span></span>
<span data-ttu-id="d5a5a-144">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d5a5a-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5a5a-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a5a-145">-ResourceId</span></span>
<span data-ttu-id="d5a5a-146">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="d5a5a-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d5a5a-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5a5a-147">-Tag</span></span>
<span data-ttu-id="d5a5a-148">Initiale tags.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="d5a5a-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="d5a5a-149">-WebhookUrl</span></span>
<span data-ttu-id="d5a5a-150">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="d5a5a-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5a5a-151">-Confirm</span></span>
<span data-ttu-id="d5a5a-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a5a-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5a5a-153">-WhatIf</span></span>
<span data-ttu-id="d5a5a-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a5a-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a5a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a5a-156">CommonParameters</span></span>
<span data-ttu-id="d5a5a-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a5a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a5a-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a5a-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a5a-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a5a-159">INPUTS</span></span>

### <span data-ttu-id="d5a5a-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d5a5a-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d5a5a-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a5a-161">System.String</span></span>

## <span data-ttu-id="d5a5a-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a5a-162">OUTPUTS</span></span>

### <span data-ttu-id="d5a5a-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="d5a5a-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="d5a5a-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5a5a-164">NOTES</span></span>

## <span data-ttu-id="d5a5a-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5a5a-165">RELATED LINKS</span></span>
