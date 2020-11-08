---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008499"
---
# <span data-ttu-id="d4ca9-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d4ca9-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="d4ca9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ca9-103">Aktualisieren einer Geräte Registrierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d4ca9-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="d4ca9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ca9-104">SYNTAX</span></span>

### <span data-ttu-id="d4ca9-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4ca9-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4ca9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4ca9-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4ca9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4ca9-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ca9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="d4ca9-109">Aktualisieren einer Registrierungsgruppe in einem Azure viel-Bereitstellungsdienst für Hub-Geräte</span><span class="sxs-lookup"><span data-stu-id="d4ca9-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d4ca9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="d4ca9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4ca9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="d4ca9-112">Aktualisieren von Zuordnungsrichtlinien und Hubs für eine Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="d4ca9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4ca9-113">PARAMETERS</span></span>

### <span data-ttu-id="d4ca9-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d4ca9-114">-AllocationPolicy</span></span>
<span data-ttu-id="d4ca9-115">Der Typ der Zuordnung für das Gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="d4ca9-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4ca9-116">-ApiVersion</span></span>
<span data-ttu-id="d4ca9-117">Die API-Version des Bereitstellungs Diensts in der benutzerdefinierten Zuordnungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="d4ca9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ca9-118">-DefaultProfile</span></span>
<span data-ttu-id="d4ca9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4ca9-120">-Erwünscht</span><span class="sxs-lookup"><span data-stu-id="d4ca9-120">-Desired</span></span>
<span data-ttu-id="d4ca9-121">Anfängliche Zwillings gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="d4ca9-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d4ca9-122">-DpsName</span></span>
<span data-ttu-id="d4ca9-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="d4ca9-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d4ca9-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d4ca9-124">-DpsObject</span></span>
<span data-ttu-id="d4ca9-125">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="d4ca9-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d4ca9-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="d4ca9-126">-EdgeEnabled</span></span>
<span data-ttu-id="d4ca9-127">Kennzeichen, das die Kanten Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="d4ca9-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d4ca9-128">-IotHub</span></span>
<span data-ttu-id="d4ca9-129">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="d4ca9-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="d4ca9-130">Verwenden Sie die durch Leerzeichen getrennte Liste für mehrere viele Hubs.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="d4ca9-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="d4ca9-131">-IotHubHostName</span></span>
<span data-ttu-id="d4ca9-132">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="d4ca9-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="d4ca9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d4ca9-133">-Name</span></span>
<span data-ttu-id="d4ca9-134">Der Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="d4ca9-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="d4ca9-135">-ProvisioningStatus</span></span>
<span data-ttu-id="d4ca9-136">Aktivieren oder Deaktivieren des Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="d4ca9-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="d4ca9-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4ca9-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="d4ca9-138">Gerätedaten, die bei der erneuten Bereitstellung an unterschiedlichen viel Hub gehandhabt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="d4ca9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ca9-139">-ResourceGroupName</span></span>
<span data-ttu-id="d4ca9-140">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d4ca9-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4ca9-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4ca9-141">-ResourceId</span></span>
<span data-ttu-id="d4ca9-142">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="d4ca9-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d4ca9-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4ca9-143">-Tag</span></span>
<span data-ttu-id="d4ca9-144">Anfängliche Twin-Tags.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="d4ca9-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="d4ca9-145">-WebhookUrl</span></span>
<span data-ttu-id="d4ca9-146">Die webhook-URL, die für benutzerdefinierte Zuordnungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="d4ca9-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4ca9-147">-Confirm</span></span>
<span data-ttu-id="d4ca9-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ca9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ca9-149">-WhatIf</span></span>
<span data-ttu-id="d4ca9-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ca9-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ca9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ca9-152">CommonParameters</span></span>
<span data-ttu-id="d4ca9-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ca9-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ca9-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ca9-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4ca9-155">INPUTS</span></span>

### <span data-ttu-id="d4ca9-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d4ca9-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d4ca9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ca9-157">System.String</span></span>

## <span data-ttu-id="d4ca9-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4ca9-158">OUTPUTS</span></span>

### <span data-ttu-id="d4ca9-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d4ca9-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="d4ca9-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4ca9-160">NOTES</span></span>

## <span data-ttu-id="d4ca9-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4ca9-161">RELATED LINKS</span></span>
