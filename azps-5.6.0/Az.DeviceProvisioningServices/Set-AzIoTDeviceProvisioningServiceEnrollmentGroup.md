---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935203"
---
# <span data-ttu-id="70b51-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="70b51-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="70b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70b51-102">SYNOPSIS</span></span>
<span data-ttu-id="70b51-103">Aktualisieren einer Geräteregistrierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="70b51-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="70b51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70b51-104">SYNTAX</span></span>

### <span data-ttu-id="70b51-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="70b51-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70b51-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70b51-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70b51-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="70b51-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70b51-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70b51-108">DESCRIPTION</span></span>
<span data-ttu-id="70b51-109">Aktualisieren Sie eine Registrierungsgruppe in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="70b51-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="70b51-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70b51-110">EXAMPLES</span></span>

### <span data-ttu-id="70b51-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70b51-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="70b51-112">Aktualisieren sie die Zuweisungsrichtlinie und Hubs für eine Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="70b51-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="70b51-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="70b51-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="70b51-114">Aktualisieren Sie den ursprünglichen Partnerstatus einer Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="70b51-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="70b51-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="70b51-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="70b51-116">Aktualisieren der Primär- und Sekundärschlüssel einer Gruppe für die Registrierung symmetrischer Schlüssel</span><span class="sxs-lookup"><span data-stu-id="70b51-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="70b51-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="70b51-117">PARAMETERS</span></span>

### <span data-ttu-id="70b51-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="70b51-118">-AllocationPolicy</span></span>
<span data-ttu-id="70b51-119">Typ der Zuweisung für gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="70b51-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="70b51-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="70b51-120">-ApiVersion</span></span>
<span data-ttu-id="70b51-121">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="70b51-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="70b51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b51-122">-DefaultProfile</span></span>
<span data-ttu-id="70b51-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70b51-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b51-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="70b51-124">-Desired</span></span>
<span data-ttu-id="70b51-125">Ursprüngliche eigenschaften des Doppelpaars.</span><span class="sxs-lookup"><span data-stu-id="70b51-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="70b51-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="70b51-126">-DpsName</span></span>
<span data-ttu-id="70b51-127">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="70b51-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="70b51-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="70b51-128">-DpsObject</span></span>
<span data-ttu-id="70b51-129">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="70b51-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="70b51-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="70b51-130">-EdgeEnabled</span></span>
<span data-ttu-id="70b51-131">Kennzeichnen, das die Edge-Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="70b51-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="70b51-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="70b51-132">-IotHub</span></span>
<span data-ttu-id="70b51-133">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="70b51-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="70b51-134">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="70b51-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="70b51-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="70b51-135">-IotHubHostName</span></span>
<span data-ttu-id="70b51-136">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="70b51-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="70b51-137">-Name</span><span class="sxs-lookup"><span data-stu-id="70b51-137">-Name</span></span>
<span data-ttu-id="70b51-138">Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="70b51-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="70b51-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="70b51-139">-PrimaryCAName</span></span>
<span data-ttu-id="70b51-140">Der Name des primären Stammzertifizierungsstellenzertifikats.</span><span class="sxs-lookup"><span data-stu-id="70b51-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="70b51-141">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70b51-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="70b51-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="70b51-142">-PrimaryCertificate</span></span>
<span data-ttu-id="70b51-143">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="70b51-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="70b51-144">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="70b51-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="70b51-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="70b51-145">-PrimaryKey</span></span>
<span data-ttu-id="70b51-146">Der primäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="70b51-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="70b51-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="70b51-147">-ProvisioningStatus</span></span>
<span data-ttu-id="70b51-148">Aktivieren oder Deaktivieren der Registrierungseingabe.</span><span class="sxs-lookup"><span data-stu-id="70b51-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="70b51-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="70b51-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="70b51-150">Gerätedaten, die bei der erneuten Bereitstellung für einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70b51-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="70b51-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b51-151">-ResourceGroupName</span></span>
<span data-ttu-id="70b51-152">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="70b51-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70b51-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70b51-153">-ResourceId</span></span>
<span data-ttu-id="70b51-154">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="70b51-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="70b51-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="70b51-155">-RootCertificate</span></span>
<span data-ttu-id="70b51-156">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="70b51-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="70b51-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="70b51-157">-SecondaryCAName</span></span>
<span data-ttu-id="70b51-158">Der Name des zertifikats der sekundären Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="70b51-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="70b51-159">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70b51-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="70b51-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="70b51-160">-SecondaryCertificate</span></span>
<span data-ttu-id="70b51-161">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="70b51-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="70b51-162">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="70b51-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="70b51-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="70b51-163">-SecondaryKey</span></span>
<span data-ttu-id="70b51-164">Der im Base64-Format gespeicherte sekundäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="70b51-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="70b51-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="70b51-165">-Tag</span></span>
<span data-ttu-id="70b51-166">Initiale Doppeltags.</span><span class="sxs-lookup"><span data-stu-id="70b51-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="70b51-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="70b51-167">-WebhookUrl</span></span>
<span data-ttu-id="70b51-168">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70b51-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="70b51-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70b51-169">-Confirm</span></span>
<span data-ttu-id="70b51-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70b51-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b51-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b51-171">-WhatIf</span></span>
<span data-ttu-id="70b51-172">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70b51-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b51-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70b51-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b51-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b51-174">CommonParameters</span></span>
<span data-ttu-id="70b51-175">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b51-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b51-176">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b51-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b51-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70b51-177">INPUTS</span></span>

### <span data-ttu-id="70b51-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="70b51-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="70b51-179">System.String</span><span class="sxs-lookup"><span data-stu-id="70b51-179">System.String</span></span>

## <span data-ttu-id="70b51-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70b51-180">OUTPUTS</span></span>

### <span data-ttu-id="70b51-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="70b51-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="70b51-182">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="70b51-182">NOTES</span></span>

## <span data-ttu-id="70b51-183">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="70b51-183">RELATED LINKS</span></span>
