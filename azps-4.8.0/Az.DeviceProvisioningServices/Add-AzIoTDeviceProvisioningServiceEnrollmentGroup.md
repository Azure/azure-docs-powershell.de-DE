---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008510"
---
# <span data-ttu-id="591ac-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="591ac-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="591ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="591ac-102">SYNOPSIS</span></span>
<span data-ttu-id="591ac-103">Erstellen Sie eine Geräte Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="591ac-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="591ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="591ac-104">SYNTAX</span></span>

### <span data-ttu-id="591ac-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="591ac-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="591ac-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="591ac-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="591ac-108">DESCRIPTION</span></span>
<span data-ttu-id="591ac-109">Erstellen Sie eine Registrierungsgruppe in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="591ac-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="591ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="591ac-110">EXAMPLES</span></span>

### <span data-ttu-id="591ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="591ac-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="591ac-112">Erstellen einer Anmeldung mit dem Bestätigungs SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="591ac-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="591ac-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="591ac-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="591ac-114">Erstellen einer Registrierung mit dem Bestätigungs X509</span><span class="sxs-lookup"><span data-stu-id="591ac-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="591ac-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="591ac-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="591ac-116">Erstellen Sie eine Anmeldung mit dem Testat-Typ SymmetricKey und dem anfänglichen Twin-Zustand.</span><span class="sxs-lookup"><span data-stu-id="591ac-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="591ac-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="591ac-117">PARAMETERS</span></span>

### <span data-ttu-id="591ac-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="591ac-118">-AllocationPolicy</span></span>
<span data-ttu-id="591ac-119">Der Typ der Zuordnung für das Gerät, das dem Hub zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="591ac-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="591ac-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="591ac-120">-ApiVersion</span></span>
<span data-ttu-id="591ac-121">Die API-Version des Bereitstellungs Diensts in der benutzerdefinierten Zuordnungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="591ac-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="591ac-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="591ac-122">-AttestationType</span></span>
<span data-ttu-id="591ac-123">Bescheinigungs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="591ac-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="591ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591ac-124">-DefaultProfile</span></span>
<span data-ttu-id="591ac-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="591ac-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="591ac-126">-Erwünscht</span><span class="sxs-lookup"><span data-stu-id="591ac-126">-Desired</span></span>
<span data-ttu-id="591ac-127">Anfängliche Zwillings gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="591ac-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="591ac-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="591ac-128">-DpsName</span></span>
<span data-ttu-id="591ac-129">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="591ac-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="591ac-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="591ac-130">-DpsObject</span></span>
<span data-ttu-id="591ac-131">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="591ac-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="591ac-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="591ac-132">-EdgeEnabled</span></span>
<span data-ttu-id="591ac-133">Kennzeichen, das die Kanten Aktivierung angibt.</span><span class="sxs-lookup"><span data-stu-id="591ac-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="591ac-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="591ac-134">-IotHub</span></span>
<span data-ttu-id="591ac-135">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="591ac-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="591ac-136">Verwenden Sie die durch Leerzeichen getrennte Liste für mehrere viele Hubs.</span><span class="sxs-lookup"><span data-stu-id="591ac-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="591ac-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="591ac-137">-IotHubHostName</span></span>
<span data-ttu-id="591ac-138">Hostname des Ziel-Zahl-Hubs</span><span class="sxs-lookup"><span data-stu-id="591ac-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="591ac-139">-Name</span><span class="sxs-lookup"><span data-stu-id="591ac-139">-Name</span></span>
<span data-ttu-id="591ac-140">Der Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="591ac-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="591ac-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="591ac-141">-PrimaryCAName</span></span>
<span data-ttu-id="591ac-142">Der Name des primären Stammzertifizierungsstellen-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="591ac-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="591ac-143">Wenn die Bescheinigung mit einem Stammzertifizierungsstellen-Zertifikat erwünscht ist, muss ein Stammzertifizierungsstellen-Name bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="591ac-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="591ac-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="591ac-144">-PrimaryCertificate</span></span>
<span data-ttu-id="591ac-145">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="591ac-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="591ac-146">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="591ac-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="591ac-147">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="591ac-147">-PrimaryKey</span></span>
<span data-ttu-id="591ac-148">Der primäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="591ac-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="591ac-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="591ac-149">-ProvisioningStatus</span></span>
<span data-ttu-id="591ac-150">Aktivieren oder Deaktivieren des Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="591ac-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="591ac-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="591ac-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="591ac-152">Gerätedaten, die bei der erneuten Bereitstellung an unterschiedlichen viel Hub gehandhabt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="591ac-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="591ac-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591ac-153">-ResourceGroupName</span></span>
<span data-ttu-id="591ac-154">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="591ac-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="591ac-155">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="591ac-155">-ResourceId</span></span>
<span data-ttu-id="591ac-156">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="591ac-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="591ac-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="591ac-157">-RootCertificate</span></span>
<span data-ttu-id="591ac-158">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="591ac-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="591ac-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="591ac-159">-SecondaryCAName</span></span>
<span data-ttu-id="591ac-160">Der Name des sekundären Stammzertifizierungsstellen-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="591ac-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="591ac-161">Wenn die Bescheinigung mit einem Stammzertifizierungsstellen-Zertifikat erwünscht ist, muss ein Stammzertifizierungsstellen-Name bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="591ac-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="591ac-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="591ac-162">-SecondaryCertificate</span></span>
<span data-ttu-id="591ac-163">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="591ac-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="591ac-164">Base-64-Darstellung der Datei "X509 Certificate. cer" oder des PEM-Dateipfads.</span><span class="sxs-lookup"><span data-stu-id="591ac-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="591ac-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="591ac-165">-SecondaryKey</span></span>
<span data-ttu-id="591ac-166">Der sekundäre symmetrische freigegebene Zugriffsschlüssel, der im Base64-Format gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="591ac-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="591ac-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="591ac-167">-Tag</span></span>
<span data-ttu-id="591ac-168">Anfängliche Twin-Tags.</span><span class="sxs-lookup"><span data-stu-id="591ac-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="591ac-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="591ac-169">-WebhookUrl</span></span>
<span data-ttu-id="591ac-170">Die webhook-URL, die für benutzerdefinierte Zuordnungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="591ac-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="591ac-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="591ac-171">-Confirm</span></span>
<span data-ttu-id="591ac-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="591ac-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591ac-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591ac-173">-WhatIf</span></span>
<span data-ttu-id="591ac-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="591ac-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591ac-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="591ac-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591ac-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591ac-176">CommonParameters</span></span>
<span data-ttu-id="591ac-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591ac-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591ac-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591ac-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591ac-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="591ac-179">INPUTS</span></span>

### <span data-ttu-id="591ac-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="591ac-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="591ac-181">System. String</span><span class="sxs-lookup"><span data-stu-id="591ac-181">System.String</span></span>

## <span data-ttu-id="591ac-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="591ac-182">OUTPUTS</span></span>

### <span data-ttu-id="591ac-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="591ac-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="591ac-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="591ac-184">NOTES</span></span>

## <span data-ttu-id="591ac-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="591ac-185">RELATED LINKS</span></span>
