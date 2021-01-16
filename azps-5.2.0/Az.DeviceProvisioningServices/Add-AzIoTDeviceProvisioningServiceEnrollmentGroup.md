---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298440"
---
# <span data-ttu-id="7098d-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7098d-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="7098d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7098d-102">SYNOPSIS</span></span>
<span data-ttu-id="7098d-103">Erstellen Sie eine Geräteregistrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7098d-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="7098d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7098d-104">SYNTAX</span></span>

### <span data-ttu-id="7098d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7098d-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7098d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7098d-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7098d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7098d-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7098d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7098d-108">DESCRIPTION</span></span>
<span data-ttu-id="7098d-109">Erstellen Sie eine Registrierungsgruppe in einem Azure IoT-Hub-Gerätebereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7098d-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7098d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7098d-110">EXAMPLES</span></span>

### <span data-ttu-id="7098d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7098d-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="7098d-112">Erstellen einer Registrierung mit dem Nachweistyp "SymmetricKey"</span><span class="sxs-lookup"><span data-stu-id="7098d-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="7098d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7098d-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="7098d-114">Erstellen einer Registrierung mit dem Nachweistyp X509</span><span class="sxs-lookup"><span data-stu-id="7098d-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="7098d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7098d-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="7098d-116">Erstellen Sie eine Registrierung mit dem Nachweistyp "SymmetricKey" und dem anfänglichen Status".</span><span class="sxs-lookup"><span data-stu-id="7098d-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="7098d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7098d-117">PARAMETERS</span></span>

### <span data-ttu-id="7098d-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7098d-118">-AllocationPolicy</span></span>
<span data-ttu-id="7098d-119">Der Typ der Zuordnung für das dem Hub zugewiesene Gerät.</span><span class="sxs-lookup"><span data-stu-id="7098d-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7098d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7098d-120">-ApiVersion</span></span>
<span data-ttu-id="7098d-121">Die API-Version des Bereitstellungsdiensts in der benutzerdefinierten Zuweisungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="7098d-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7098d-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="7098d-122">-AttestationType</span></span>
<span data-ttu-id="7098d-123">Nachweismechanismus.</span><span class="sxs-lookup"><span data-stu-id="7098d-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="7098d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7098d-124">-DefaultProfile</span></span>
<span data-ttu-id="7098d-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7098d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7098d-126">-Desired</span><span class="sxs-lookup"><span data-stu-id="7098d-126">-Desired</span></span>
<span data-ttu-id="7098d-127">Anfangs gewünschte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7098d-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7098d-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7098d-128">-DpsName</span></span>
<span data-ttu-id="7098d-129">Name des Bereitstellungsdiensts für IoT-Geräte</span><span class="sxs-lookup"><span data-stu-id="7098d-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7098d-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7098d-130">-DpsObject</span></span>
<span data-ttu-id="7098d-131">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="7098d-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7098d-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7098d-132">-EdgeEnabled</span></span>
<span data-ttu-id="7098d-133">Kennzeichnung zur Aktivierung der Kante.</span><span class="sxs-lookup"><span data-stu-id="7098d-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7098d-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7098d-134">-IotHub</span></span>
<span data-ttu-id="7098d-135">Hostname des IoT-Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="7098d-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7098d-136">Verwenden Sie eine durch Leerzeichen getrennte Liste für mehrere IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="7098d-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7098d-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7098d-137">-IotHubHostName</span></span>
<span data-ttu-id="7098d-138">Hostname des IoT-Hub-Ziels.</span><span class="sxs-lookup"><span data-stu-id="7098d-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7098d-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7098d-139">-Name</span></span>
<span data-ttu-id="7098d-140">Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7098d-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="7098d-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="7098d-141">-PrimaryCAName</span></span>
<span data-ttu-id="7098d-142">Der Name des primären Zertifikats der Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="7098d-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="7098d-143">Wenn ein Nachweis mit einem Zertifikat der Stammzertifizierungsstelle gewünscht wird, muss ein Stammzertifizierungsstellenname angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7098d-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7098d-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7098d-144">-PrimaryCertificate</span></span>
<span data-ttu-id="7098d-145">Der Pfad zu der Datei, die das primäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="7098d-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="7098d-146">Basis-64-Darstellung von X509-Zertifikat-CER-Datei oder PEM-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="7098d-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7098d-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7098d-147">-PrimaryKey</span></span>
<span data-ttu-id="7098d-148">Der im Basis64-Format gespeicherte primäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7098d-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7098d-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7098d-149">-ProvisioningStatus</span></span>
<span data-ttu-id="7098d-150">Registrierungseintrag aktivieren oder deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7098d-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7098d-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7098d-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="7098d-152">Gerätedaten, die bei der erneuten Bereitstellung an einen anderen Iot Hub behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7098d-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7098d-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7098d-153">-ResourceGroupName</span></span>
<span data-ttu-id="7098d-154">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7098d-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7098d-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7098d-155">-ResourceId</span></span>
<span data-ttu-id="7098d-156">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="7098d-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7098d-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="7098d-157">-RootCertificate</span></span>
<span data-ttu-id="7098d-158">Ermöglicht das Erstellen von X509attestation mithilfe von Stammzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="7098d-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="7098d-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="7098d-159">-SecondaryCAName</span></span>
<span data-ttu-id="7098d-160">Der Name des Zertifikats der sekundären Stammzertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="7098d-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="7098d-161">Wenn ein Nachweis mit einem Zertifikat der Stammzertifizierungsstelle gewünscht wird, muss ein Stammzertifizierungsstellenname angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7098d-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7098d-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7098d-162">-SecondaryCertificate</span></span>
<span data-ttu-id="7098d-163">Der Pfad zu der Datei, die das sekundäre Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="7098d-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="7098d-164">Basis-64-Darstellung von X509-Zertifikat-CER-Datei oder PEM-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="7098d-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7098d-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7098d-165">-SecondaryKey</span></span>
<span data-ttu-id="7098d-166">Der im Base64-Format gespeicherte sekundäre symmetrische freigegebene Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7098d-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7098d-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="7098d-167">-Tag</span></span>
<span data-ttu-id="7098d-168">Initiale tags.</span><span class="sxs-lookup"><span data-stu-id="7098d-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="7098d-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7098d-169">-WebhookUrl</span></span>
<span data-ttu-id="7098d-170">Die webhook-URL, die für benutzerdefinierte Zuweisungsanforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7098d-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7098d-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7098d-171">-Confirm</span></span>
<span data-ttu-id="7098d-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7098d-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7098d-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7098d-173">-WhatIf</span></span>
<span data-ttu-id="7098d-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7098d-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7098d-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7098d-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7098d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7098d-176">CommonParameters</span></span>
<span data-ttu-id="7098d-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7098d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7098d-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7098d-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7098d-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7098d-179">INPUTS</span></span>

### <span data-ttu-id="7098d-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7098d-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7098d-181">System.String</span><span class="sxs-lookup"><span data-stu-id="7098d-181">System.String</span></span>

## <span data-ttu-id="7098d-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7098d-182">OUTPUTS</span></span>

### <span data-ttu-id="7098d-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7098d-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="7098d-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7098d-184">NOTES</span></span>

## <span data-ttu-id="7098d-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7098d-185">RELATED LINKS</span></span>
