---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 5aca36433089a2e84965ee6d1d8b2c17d3c53205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929040"
---
# <span data-ttu-id="42bbf-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="42bbf-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="42bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="42bbf-103">Erstellen Sie einen Geräteregistrierungsdatensatz.</span><span class="sxs-lookup"><span data-stu-id="42bbf-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="42bbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42bbf-104">SYNTAX</span></span>

### <span data-ttu-id="42bbf-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42bbf-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42bbf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42bbf-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42bbf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42bbf-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42bbf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42bbf-108">DESCRIPTION</span></span>
<span data-ttu-id="42bbf-109">Erstellen Sie eine Geräteregistrierung in einem Azure IoT Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="42bbf-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="42bbf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42bbf-110">EXAMPLES</span></span>

### <span data-ttu-id="42bbf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42bbf-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="42bbf-112">Erstellen einer Registrierung mit dem Nachweistyp "SymmetricKey"</span><span class="sxs-lookup"><span data-stu-id="42bbf-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="42bbf-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="42bbf-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="42bbf-114">Erstellen Sie eine Registrierung mit TPM-Nachweis.</span><span class="sxs-lookup"><span data-stu-id="42bbf-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="42bbf-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="42bbf-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="42bbf-116">Erstellen einer Registrierung mit dem Nachweistyp X509</span><span class="sxs-lookup"><span data-stu-id="42bbf-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="42bbf-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="42bbf-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="42bbf-118">Erstellen Sie eine Registrierung mit dem Nachweistyp "Symmetrischer Schlüssel" und dem anfangsen Doppelzustand.</span><span class="sxs-lookup"><span data-stu-id="42bbf-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="42bbf-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42bbf-119">PARAMETERS</span></span>

### <span data-ttu-id="42bbf-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="42bbf-120">-AllocationPolicy</span></span>
<span data-ttu-id="42bbf-121">Typ der Zuweisung für gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="42bbf-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="42bbf-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="42bbf-122">-ApiVersion</span></span>
<span data-ttu-id="42bbf-123">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="42bbf-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="42bbf-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="42bbf-124">-AttestationType</span></span>
<span data-ttu-id="42bbf-125">Nachweismechanismus.</span><span class="sxs-lookup"><span data-stu-id="42bbf-125">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bbf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bbf-126">-DefaultProfile</span></span>
<span data-ttu-id="42bbf-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42bbf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42bbf-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="42bbf-128">-Desired</span></span>
<span data-ttu-id="42bbf-129">Ursprüngliche eigenschaften des Doppelpaars.</span><span class="sxs-lookup"><span data-stu-id="42bbf-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="42bbf-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="42bbf-130">-DeviceId</span></span>
<span data-ttu-id="42bbf-131">IoT Hub-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="42bbf-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="42bbf-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="42bbf-132">-DpsName</span></span>
<span data-ttu-id="42bbf-133">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="42bbf-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="42bbf-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="42bbf-134">-DpsObject</span></span>
<span data-ttu-id="42bbf-135">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="42bbf-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="42bbf-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="42bbf-136">-EdgeEnabled</span></span>
<span data-ttu-id="42bbf-137">Kennzeichnen, das die Edge-Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="42bbf-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="42bbf-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="42bbf-138">-EndorsementKey</span></span>
<span data-ttu-id="42bbf-139">TPM-Bestätigungsschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="42bbf-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="42bbf-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="42bbf-140">-IotHub</span></span>
<span data-ttu-id="42bbf-141">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="42bbf-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="42bbf-142">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="42bbf-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="42bbf-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="42bbf-143">-IotHubHostName</span></span>
<span data-ttu-id="42bbf-144">Hostname des IoT Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="42bbf-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="42bbf-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="42bbf-145">-PrimaryCAName</span></span>
<span data-ttu-id="42bbf-146">Der Name des primären Stammzertifizierungsstellenzertifikats.</span><span class="sxs-lookup"><span data-stu-id="42bbf-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="42bbf-147">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42bbf-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="42bbf-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="42bbf-148">-PrimaryCertificate</span></span>
<span data-ttu-id="42bbf-149">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="42bbf-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="42bbf-150">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="42bbf-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="42bbf-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="42bbf-151">-PrimaryKey</span></span>
<span data-ttu-id="42bbf-152">Der primäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="42bbf-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="42bbf-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="42bbf-153">-ProvisioningStatus</span></span>
<span data-ttu-id="42bbf-154">Aktivieren oder Deaktivieren der Registrierungseingabe.</span><span class="sxs-lookup"><span data-stu-id="42bbf-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="42bbf-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="42bbf-155">-RegistrationId</span></span>
<span data-ttu-id="42bbf-156">Individuelle Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="42bbf-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="42bbf-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="42bbf-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="42bbf-158">Gerätedaten, die bei der erneuten Bereitstellung für einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42bbf-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="42bbf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42bbf-159">-ResourceGroupName</span></span>
<span data-ttu-id="42bbf-160">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42bbf-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42bbf-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42bbf-161">-ResourceId</span></span>
<span data-ttu-id="42bbf-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="42bbf-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="42bbf-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="42bbf-163">-RootCertificate</span></span>
<span data-ttu-id="42bbf-164">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="42bbf-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="42bbf-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="42bbf-165">-SecondaryCAName</span></span>
<span data-ttu-id="42bbf-166">Der Name des zertifikats der sekundären Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="42bbf-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="42bbf-167">Wenn eine Bestätigung mit einem Stammzertifizierungsstellenzertifikat gewünscht wird, muss ein Stamm-Ca-Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42bbf-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="42bbf-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="42bbf-168">-SecondaryCertificate</span></span>
<span data-ttu-id="42bbf-169">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="42bbf-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="42bbf-170">Base-64-Darstellung der X509-Zertifikat-CER-Datei oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="42bbf-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="42bbf-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="42bbf-171">-SecondaryKey</span></span>
<span data-ttu-id="42bbf-172">Der im Base64-Format gespeicherte sekundäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="42bbf-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="42bbf-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="42bbf-173">-StorageRootKey</span></span>
<span data-ttu-id="42bbf-174">TPM-Speicherstammschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="42bbf-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="42bbf-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="42bbf-175">-Tag</span></span>
<span data-ttu-id="42bbf-176">Initiale Doppeltags.</span><span class="sxs-lookup"><span data-stu-id="42bbf-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="42bbf-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="42bbf-177">-WebhookUrl</span></span>
<span data-ttu-id="42bbf-178">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42bbf-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="42bbf-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42bbf-179">-Confirm</span></span>
<span data-ttu-id="42bbf-180">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42bbf-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42bbf-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42bbf-181">-WhatIf</span></span>
<span data-ttu-id="42bbf-182">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42bbf-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42bbf-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42bbf-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42bbf-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bbf-184">CommonParameters</span></span>
<span data-ttu-id="42bbf-185">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42bbf-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bbf-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42bbf-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bbf-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42bbf-187">INPUTS</span></span>

### <span data-ttu-id="42bbf-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="42bbf-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="42bbf-189">System.String</span><span class="sxs-lookup"><span data-stu-id="42bbf-189">System.String</span></span>

## <span data-ttu-id="42bbf-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42bbf-190">OUTPUTS</span></span>

### <span data-ttu-id="42bbf-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="42bbf-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="42bbf-192">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="42bbf-192">NOTES</span></span>

## <span data-ttu-id="42bbf-193">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="42bbf-193">RELATED LINKS</span></span>
