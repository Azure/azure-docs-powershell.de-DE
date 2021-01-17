---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387076"
---
# <span data-ttu-id="297c7-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="297c7-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="297c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="297c7-102">SYNOPSIS</span></span>
<span data-ttu-id="297c7-103">Erstellen Sie einen Geräteregistrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="297c7-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="297c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="297c7-104">SYNTAX</span></span>

### <span data-ttu-id="297c7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="297c7-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="297c7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="297c7-106">InputObjectSet</span></span>
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

### <span data-ttu-id="297c7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="297c7-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="297c7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="297c7-108">DESCRIPTION</span></span>
<span data-ttu-id="297c7-109">Erstellen Sie eine Geräteregistrierung bei einem Azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="297c7-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="297c7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="297c7-110">EXAMPLES</span></span>

### <span data-ttu-id="297c7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="297c7-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="297c7-112">Erstellen einer Registrierung mit dem Nachweistyp "SymmetricKey"</span><span class="sxs-lookup"><span data-stu-id="297c7-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="297c7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="297c7-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="297c7-114">Erstellen Sie eine Registrierung mit einem TPM-Nachweis.</span><span class="sxs-lookup"><span data-stu-id="297c7-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="297c7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="297c7-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="297c7-116">Erstellen einer Registrierung mit dem Nachweistyp X509</span><span class="sxs-lookup"><span data-stu-id="297c7-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="297c7-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="297c7-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="297c7-118">Erstellen Sie eine Registrierung mit dem Nachweistyp "SymmetricKey" und dem anfänglichen Status".</span><span class="sxs-lookup"><span data-stu-id="297c7-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="297c7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="297c7-119">PARAMETERS</span></span>

### <span data-ttu-id="297c7-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="297c7-120">-AllocationPolicy</span></span>
<span data-ttu-id="297c7-121">Der Typ der Zuordnung für das dem Hub zugewiesene Gerät.</span><span class="sxs-lookup"><span data-stu-id="297c7-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="297c7-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="297c7-122">-ApiVersion</span></span>
<span data-ttu-id="297c7-123">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="297c7-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="297c7-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="297c7-124">-AttestationType</span></span>
<span data-ttu-id="297c7-125">Nachweismechanismus.</span><span class="sxs-lookup"><span data-stu-id="297c7-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="297c7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297c7-126">-DefaultProfile</span></span>
<span data-ttu-id="297c7-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="297c7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297c7-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="297c7-128">-Desired</span></span>
<span data-ttu-id="297c7-129">Anfangs gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="297c7-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="297c7-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="297c7-130">-DeviceId</span></span>
<span data-ttu-id="297c7-131">IoT-Hub-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="297c7-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="297c7-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="297c7-132">-DpsName</span></span>
<span data-ttu-id="297c7-133">Name des IoT-Gerätebereitstellungsdiensts</span><span class="sxs-lookup"><span data-stu-id="297c7-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="297c7-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="297c7-134">-DpsObject</span></span>
<span data-ttu-id="297c7-135">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="297c7-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="297c7-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="297c7-136">-EdgeEnabled</span></span>
<span data-ttu-id="297c7-137">Kennzeichnung zur Aktivierung von Rand.</span><span class="sxs-lookup"><span data-stu-id="297c7-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="297c7-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="297c7-138">-EndorsementKey</span></span>
<span data-ttu-id="297c7-139">TPM-Empfehlungsschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="297c7-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="297c7-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="297c7-140">-IotHub</span></span>
<span data-ttu-id="297c7-141">Hostname des IoT-Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="297c7-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="297c7-142">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="297c7-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="297c7-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="297c7-143">-IotHubHostName</span></span>
<span data-ttu-id="297c7-144">Hostname des IoT-Zielhubs.</span><span class="sxs-lookup"><span data-stu-id="297c7-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="297c7-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="297c7-145">-PrimaryCAName</span></span>
<span data-ttu-id="297c7-146">Der Name des primären Zertifizierungsstellenstammzertifikats.</span><span class="sxs-lookup"><span data-stu-id="297c7-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="297c7-147">Wenn ein Nachweis mit einem Stammzertifikat der Zertifizierungsstelle gewünscht wird, muss ein Stammzertifizierungsstellenname angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="297c7-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="297c7-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="297c7-148">-PrimaryCertificate</span></span>
<span data-ttu-id="297c7-149">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="297c7-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="297c7-150">Basis-64-Darstellung von X509-Zertifikat-CER-Datei oder PEM-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="297c7-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="297c7-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="297c7-151">-PrimaryKey</span></span>
<span data-ttu-id="297c7-152">Der im Basis64-Format gespeicherte primäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="297c7-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="297c7-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="297c7-153">-ProvisioningStatus</span></span>
<span data-ttu-id="297c7-154">Registrierungseintrag aktivieren oder deaktivieren</span><span class="sxs-lookup"><span data-stu-id="297c7-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="297c7-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="297c7-155">-RegistrationId</span></span>
<span data-ttu-id="297c7-156">Registrierungs-ID für die individuelle Registrierung.</span><span class="sxs-lookup"><span data-stu-id="297c7-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="297c7-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="297c7-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="297c7-158">Gerätedaten, die bei der erneuten Bereitstellung an einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="297c7-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="297c7-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297c7-159">-ResourceGroupName</span></span>
<span data-ttu-id="297c7-160">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="297c7-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="297c7-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="297c7-161">-ResourceId</span></span>
<span data-ttu-id="297c7-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="297c7-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="297c7-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="297c7-163">-RootCertificate</span></span>
<span data-ttu-id="297c7-164">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="297c7-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="297c7-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="297c7-165">-SecondaryCAName</span></span>
<span data-ttu-id="297c7-166">Der Name des Zertifikats für die sekundäre Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="297c7-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="297c7-167">Wenn ein Nachweis mit einem Stammzertifikat der Zertifizierungsstelle gewünscht wird, muss ein Stammzertifizierungsstellenname angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="297c7-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="297c7-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="297c7-168">-SecondaryCertificate</span></span>
<span data-ttu-id="297c7-169">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="297c7-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="297c7-170">Basis-64-Darstellung von X509-Zertifikat-CER-Datei oder PEM-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="297c7-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="297c7-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="297c7-171">-SecondaryKey</span></span>
<span data-ttu-id="297c7-172">Der im Base64-Format gespeicherte sekundäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="297c7-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="297c7-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="297c7-173">-StorageRootKey</span></span>
<span data-ttu-id="297c7-174">TPM-Speicherstammschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="297c7-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="297c7-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="297c7-175">-Tag</span></span>
<span data-ttu-id="297c7-176">Initiale tags.</span><span class="sxs-lookup"><span data-stu-id="297c7-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="297c7-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="297c7-177">-WebhookUrl</span></span>
<span data-ttu-id="297c7-178">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="297c7-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="297c7-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="297c7-179">-Confirm</span></span>
<span data-ttu-id="297c7-180">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="297c7-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297c7-181">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="297c7-181">-WhatIf</span></span>
<span data-ttu-id="297c7-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="297c7-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297c7-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="297c7-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297c7-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297c7-184">CommonParameters</span></span>
<span data-ttu-id="297c7-185">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297c7-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297c7-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="297c7-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297c7-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="297c7-187">INPUTS</span></span>

### <span data-ttu-id="297c7-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="297c7-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="297c7-189">System.String</span><span class="sxs-lookup"><span data-stu-id="297c7-189">System.String</span></span>

## <span data-ttu-id="297c7-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="297c7-190">OUTPUTS</span></span>

### <span data-ttu-id="297c7-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="297c7-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="297c7-192">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="297c7-192">NOTES</span></span>

## <span data-ttu-id="297c7-193">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="297c7-193">RELATED LINKS</span></span>
