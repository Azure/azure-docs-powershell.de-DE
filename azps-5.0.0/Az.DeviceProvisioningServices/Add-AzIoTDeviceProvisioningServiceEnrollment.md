---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175740"
---
# <span data-ttu-id="a0646-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="a0646-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="a0646-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0646-102">SYNOPSIS</span></span>
<span data-ttu-id="a0646-103">Erstellen Sie einen Geräte Registrierungseintrag.</span><span class="sxs-lookup"><span data-stu-id="a0646-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="a0646-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0646-104">SYNTAX</span></span>

### <span data-ttu-id="a0646-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0646-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="a0646-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0646-106">InputObjectSet</span></span>
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

### <span data-ttu-id="a0646-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a0646-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="a0646-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0646-108">DESCRIPTION</span></span>
<span data-ttu-id="a0646-109">Erstellen Sie eine Geräteregistrierung in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="a0646-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a0646-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0646-110">EXAMPLES</span></span>

### <span data-ttu-id="a0646-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0646-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="a0646-112">Erstellen einer Anmeldung mit dem Bestätigungs SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="a0646-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="a0646-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0646-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="a0646-114">Erstellen Sie eine Registrierung mit TPM-Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="a0646-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="a0646-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a0646-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="a0646-116">Erstellen einer Registrierung mit dem Bestätigungs X509</span><span class="sxs-lookup"><span data-stu-id="a0646-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="a0646-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a0646-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="a0646-118">Erstellen Sie eine Anmeldung mit dem Testat-Typ SymmetricKey und dem anfänglichen Twin-Zustand.</span><span class="sxs-lookup"><span data-stu-id="a0646-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="a0646-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0646-119">PARAMETERS</span></span>

### <span data-ttu-id="a0646-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a0646-120">-AllocationPolicy</span></span>
<span data-ttu-id="a0646-121">Der Typ der Zuordnung für das Gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a0646-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="a0646-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a0646-122">-ApiVersion</span></span>
<span data-ttu-id="a0646-123">Die API-Version des Bereitstellungs Diensts in der benutzerdefinierten Zuordnungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="a0646-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="a0646-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="a0646-124">-AttestationType</span></span>
<span data-ttu-id="a0646-125">Bescheinigungs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="a0646-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="a0646-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0646-126">-DefaultProfile</span></span>
<span data-ttu-id="a0646-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0646-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0646-128">-Erwünscht</span><span class="sxs-lookup"><span data-stu-id="a0646-128">-Desired</span></span>
<span data-ttu-id="a0646-129">Anfängliche Zwillings gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a0646-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="a0646-130">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="a0646-130">-DeviceId</span></span>
<span data-ttu-id="a0646-131">Viel Hub-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="a0646-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="a0646-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a0646-132">-DpsName</span></span>
<span data-ttu-id="a0646-133">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="a0646-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a0646-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a0646-134">-DpsObject</span></span>
<span data-ttu-id="a0646-135">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="a0646-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a0646-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="a0646-136">-EdgeEnabled</span></span>
<span data-ttu-id="a0646-137">Kennzeichen, das die Kanten Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="a0646-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="a0646-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="a0646-138">-EndorsementKey</span></span>
<span data-ttu-id="a0646-139">TPM-bestätigungsschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0646-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="a0646-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="a0646-140">-IotHub</span></span>
<span data-ttu-id="a0646-141">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="a0646-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="a0646-142">Verwenden Sie die durch Leerzeichen getrennte Liste für mehrere viele Hubs.</span><span class="sxs-lookup"><span data-stu-id="a0646-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="a0646-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="a0646-143">-IotHubHostName</span></span>
<span data-ttu-id="a0646-144">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="a0646-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="a0646-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="a0646-145">-PrimaryCAName</span></span>
<span data-ttu-id="a0646-146">Der Name des primären Stammzertifizierungsstellen-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a0646-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="a0646-147">Wenn die Bescheinigung mit einem Stammzertifizierungsstellen-Zertifikat erwünscht ist, muss ein Stammzertifizierungsstellen-Name bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0646-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a0646-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a0646-148">-PrimaryCertificate</span></span>
<span data-ttu-id="a0646-149">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="a0646-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="a0646-150">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="a0646-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a0646-151">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="a0646-151">-PrimaryKey</span></span>
<span data-ttu-id="a0646-152">Der primäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a0646-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a0646-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="a0646-153">-ProvisioningStatus</span></span>
<span data-ttu-id="a0646-154">Aktivieren oder Deaktivieren des Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="a0646-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="a0646-155">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="a0646-155">-RegistrationId</span></span>
<span data-ttu-id="a0646-156">Individuelle Registrierungs-ID für die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a0646-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="a0646-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0646-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="a0646-158">Gerätedaten, die bei der erneuten Bereitstellung an unterschiedlichen viel Hub gehandhabt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0646-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="a0646-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0646-159">-ResourceGroupName</span></span>
<span data-ttu-id="a0646-160">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a0646-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a0646-161">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0646-161">-ResourceId</span></span>
<span data-ttu-id="a0646-162">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="a0646-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a0646-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="a0646-163">-RootCertificate</span></span>
<span data-ttu-id="a0646-164">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="a0646-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="a0646-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="a0646-165">-SecondaryCAName</span></span>
<span data-ttu-id="a0646-166">Der Name des sekundären Stammzertifizierungsstellen-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a0646-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="a0646-167">Wenn die Bescheinigung mit einem Stammzertifizierungsstellen-Zertifikat erwünscht ist, muss ein Stammzertifizierungsstellen-Name bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0646-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a0646-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a0646-168">-SecondaryCertificate</span></span>
<span data-ttu-id="a0646-169">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="a0646-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="a0646-170">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="a0646-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a0646-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a0646-171">-SecondaryKey</span></span>
<span data-ttu-id="a0646-172">Der sekundäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a0646-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a0646-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="a0646-173">-StorageRootKey</span></span>
<span data-ttu-id="a0646-174">TPM-Speicherstammschlüssel für ein TPM-Gerät.</span><span class="sxs-lookup"><span data-stu-id="a0646-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="a0646-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0646-175">-Tag</span></span>
<span data-ttu-id="a0646-176">Anfängliche Twin-Tags.</span><span class="sxs-lookup"><span data-stu-id="a0646-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="a0646-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="a0646-177">-WebhookUrl</span></span>
<span data-ttu-id="a0646-178">Die webhook-URL, die für benutzerdefinierte Zuordnungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0646-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="a0646-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0646-179">-Confirm</span></span>
<span data-ttu-id="a0646-180">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0646-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0646-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0646-181">-WhatIf</span></span>
<span data-ttu-id="a0646-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0646-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0646-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0646-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0646-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0646-184">CommonParameters</span></span>
<span data-ttu-id="a0646-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0646-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0646-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0646-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0646-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0646-187">INPUTS</span></span>

### <span data-ttu-id="a0646-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a0646-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a0646-189">System. String</span><span class="sxs-lookup"><span data-stu-id="a0646-189">System.String</span></span>

## <span data-ttu-id="a0646-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0646-190">OUTPUTS</span></span>

### <span data-ttu-id="a0646-191">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="a0646-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="a0646-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0646-192">NOTES</span></span>

## <span data-ttu-id="a0646-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0646-193">RELATED LINKS</span></span>
