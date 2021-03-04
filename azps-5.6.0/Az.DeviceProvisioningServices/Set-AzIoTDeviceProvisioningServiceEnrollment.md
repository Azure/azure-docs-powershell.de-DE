---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935208"
---
# <span data-ttu-id="1bba7-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="1bba7-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="1bba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bba7-102">SYNOPSIS</span></span>
<span data-ttu-id="1bba7-103">Aktualisieren eines Geräteregistrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="1bba7-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="1bba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bba7-104">SYNTAX</span></span>

### <span data-ttu-id="1bba7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1bba7-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bba7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1bba7-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bba7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1bba7-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bba7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bba7-108">DESCRIPTION</span></span>
<span data-ttu-id="1bba7-109">Aktualisieren Sie eine Geräteregistrierung in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="1bba7-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1bba7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1bba7-110">EXAMPLES</span></span>

### <span data-ttu-id="1bba7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bba7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="1bba7-112">Aktualisieren sie die Zuweisungsrichtlinie und Hubs für einen Registrierungsdatensatz.</span><span class="sxs-lookup"><span data-stu-id="1bba7-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="1bba7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1bba7-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="1bba7-114">Aktualisieren Sie den ursprünglichen Partnerstatus einer Registrierung.</span><span class="sxs-lookup"><span data-stu-id="1bba7-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="1bba7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1bba7-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="1bba7-116">Aktualisieren der primären und sekundären Zertifikate einer symmetrischen Schlüsselregistrierung</span><span class="sxs-lookup"><span data-stu-id="1bba7-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="1bba7-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1bba7-117">PARAMETERS</span></span>

### <span data-ttu-id="1bba7-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1bba7-118">-AllocationPolicy</span></span>
<span data-ttu-id="1bba7-119">Typ der Zuweisung für gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1bba7-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="1bba7-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1bba7-120">-ApiVersion</span></span>
<span data-ttu-id="1bba7-121">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="1bba7-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="1bba7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bba7-122">-DefaultProfile</span></span>
<span data-ttu-id="1bba7-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bba7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bba7-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="1bba7-124">-Desired</span></span>
<span data-ttu-id="1bba7-125">Ursprüngliche eigenschaften des Doppelpaars.</span><span class="sxs-lookup"><span data-stu-id="1bba7-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="1bba7-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1bba7-126">-DeviceId</span></span>
<span data-ttu-id="1bba7-127">IoT Hub-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="1bba7-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="1bba7-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="1bba7-128">-DpsName</span></span>
<span data-ttu-id="1bba7-129">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="1bba7-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1bba7-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1bba7-130">-DpsObject</span></span>
<span data-ttu-id="1bba7-131">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="1bba7-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1bba7-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="1bba7-132">-EdgeEnabled</span></span>
<span data-ttu-id="1bba7-133">Kennzeichnen, das die Edge-Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="1bba7-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="1bba7-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="1bba7-134">-EndorsementKey</span></span>
<span data-ttu-id="1bba7-135">TPM-Bestätigungsschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1bba7-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="1bba7-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="1bba7-136">-IotHub</span></span>
<span data-ttu-id="1bba7-137">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="1bba7-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="1bba7-138">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="1bba7-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="1bba7-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="1bba7-139">-IotHubHostName</span></span>
<span data-ttu-id="1bba7-140">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="1bba7-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="1bba7-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="1bba7-141">-PrimaryCAName</span></span>
<span data-ttu-id="1bba7-142">Der Name des primären Stammzertifizierungsstellenzertifikats.</span><span class="sxs-lookup"><span data-stu-id="1bba7-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="1bba7-143">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1bba7-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="1bba7-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="1bba7-144">-PrimaryCertificate</span></span>
<span data-ttu-id="1bba7-145">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="1bba7-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="1bba7-146">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="1bba7-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="1bba7-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1bba7-147">-PrimaryKey</span></span>
<span data-ttu-id="1bba7-148">Der primäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1bba7-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="1bba7-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="1bba7-149">-ProvisioningStatus</span></span>
<span data-ttu-id="1bba7-150">Aktivieren oder Deaktivieren der Registrierungseingabe.</span><span class="sxs-lookup"><span data-stu-id="1bba7-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="1bba7-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="1bba7-151">-RegistrationId</span></span>
<span data-ttu-id="1bba7-152">Individuelle Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="1bba7-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="1bba7-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="1bba7-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="1bba7-154">Gerätedaten, die bei der erneuten Bereitstellung für einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1bba7-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="1bba7-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bba7-155">-ResourceGroupName</span></span>
<span data-ttu-id="1bba7-156">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1bba7-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1bba7-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bba7-157">-ResourceId</span></span>
<span data-ttu-id="1bba7-158">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="1bba7-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1bba7-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bba7-159">-RootCertificate</span></span>
<span data-ttu-id="1bba7-160">Wechseln Sie zum Aktualisieren von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="1bba7-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="1bba7-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="1bba7-161">-SecondaryCAName</span></span>
<span data-ttu-id="1bba7-162">Der Name des zertifikats der sekundären Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="1bba7-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="1bba7-163">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1bba7-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="1bba7-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="1bba7-164">-SecondaryCertificate</span></span>
<span data-ttu-id="1bba7-165">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="1bba7-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="1bba7-166">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="1bba7-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="1bba7-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1bba7-167">-SecondaryKey</span></span>
<span data-ttu-id="1bba7-168">Der im Base64-Format gespeicherte sekundäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="1bba7-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="1bba7-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="1bba7-169">-StorageRootKey</span></span>
<span data-ttu-id="1bba7-170">TPM-Speicherstammschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1bba7-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="1bba7-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bba7-171">-Tag</span></span>
<span data-ttu-id="1bba7-172">Initiale Doppeltags.</span><span class="sxs-lookup"><span data-stu-id="1bba7-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="1bba7-173">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="1bba7-173">-WebhookUrl</span></span>
<span data-ttu-id="1bba7-174">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bba7-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="1bba7-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bba7-175">-Confirm</span></span>
<span data-ttu-id="1bba7-176">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bba7-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bba7-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bba7-177">-WhatIf</span></span>
<span data-ttu-id="1bba7-178">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bba7-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bba7-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bba7-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bba7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bba7-180">CommonParameters</span></span>
<span data-ttu-id="1bba7-181">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bba7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bba7-182">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bba7-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bba7-183">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1bba7-183">INPUTS</span></span>

### <span data-ttu-id="1bba7-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1bba7-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1bba7-185">System.String</span><span class="sxs-lookup"><span data-stu-id="1bba7-185">System.String</span></span>

## <span data-ttu-id="1bba7-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1bba7-186">OUTPUTS</span></span>

### <span data-ttu-id="1bba7-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="1bba7-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="1bba7-188">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1bba7-188">NOTES</span></span>

## <span data-ttu-id="1bba7-189">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1bba7-189">RELATED LINKS</span></span>
