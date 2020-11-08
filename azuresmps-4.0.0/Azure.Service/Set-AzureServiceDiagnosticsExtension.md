---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006253"
---
# <span data-ttu-id="69156-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="69156-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="69156-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69156-102">SYNOPSIS</span></span>
<span data-ttu-id="69156-103">Aktiviert die Azure Diagnostics-Erweiterung für angegebene Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="69156-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="69156-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69156-104">SYNTAX</span></span>

### <span data-ttu-id="69156-105">Setextension (Standard)</span><span class="sxs-lookup"><span data-stu-id="69156-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="69156-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="69156-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="69156-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="69156-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="69156-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69156-108">DESCRIPTION</span></span>
<span data-ttu-id="69156-109">Das Cmdlet " **AzureServiceDiagnosticsExtension** " aktiviert die Azure Diagnostics-Erweiterung für bestimmte Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="69156-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="69156-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69156-110">EXAMPLES</span></span>

### <span data-ttu-id="69156-111">Beispiel 1: Aktivieren der Azure Diagnostics-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="69156-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="69156-112">Mit diesem Befehl wird die Azure Diagnostics-Erweiterung für alle Rollen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="69156-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="69156-113">Beispiel 2: Aktivieren der Azure Diagnostics-Erweiterung für eine angegebene Rolle</span><span class="sxs-lookup"><span data-stu-id="69156-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="69156-114">Mit diesem Befehl wird die Azure Diagnostics-Erweiterung für eine angegebene Rolle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="69156-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="69156-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="69156-115">PARAMETERS</span></span>

### <span data-ttu-id="69156-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="69156-116">-CertificateThumbprint</span></span>
<span data-ttu-id="69156-117">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69156-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="69156-118">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="69156-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="69156-119">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="69156-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="69156-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="69156-121">Gibt ein Array der Konfiguration für Azure Diagnostics an.</span><span class="sxs-lookup"><span data-stu-id="69156-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="69156-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="69156-123">Gibt die Konfiguration für Azure Diagnostics an.</span><span class="sxs-lookup"><span data-stu-id="69156-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="69156-124">Sie können das Schema mithilfe des folgenden Befehls herunterladen:</span><span class="sxs-lookup"><span data-stu-id="69156-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-125">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="69156-125">-ExtensionId</span></span>
<span data-ttu-id="69156-126">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="69156-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-127">-Information</span><span class="sxs-lookup"><span data-stu-id="69156-127">-InformationAction</span></span>
<span data-ttu-id="69156-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="69156-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="69156-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="69156-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69156-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="69156-130">Continue</span></span>
- <span data-ttu-id="69156-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="69156-131">Ignore</span></span>
- <span data-ttu-id="69156-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="69156-132">Inquire</span></span>
- <span data-ttu-id="69156-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="69156-133">SilentlyContinue</span></span>
- <span data-ttu-id="69156-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="69156-134">Stop</span></span>
- <span data-ttu-id="69156-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="69156-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69156-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="69156-136">-InformationVariable</span></span>
<span data-ttu-id="69156-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="69156-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69156-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="69156-138">-Profile</span></span>
<span data-ttu-id="69156-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="69156-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69156-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="69156-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69156-141">-Role</span><span class="sxs-lookup"><span data-stu-id="69156-141">-Role</span></span>
<span data-ttu-id="69156-142">Gibt ein optionales Array von Rollen an, für das die Azure Diagnostics-Konfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="69156-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="69156-143">Wenn Sie diesen Parameter nicht angeben, wird die Diagnose Konfiguration als Standardkonfiguration für alle Rollen übernommen.</span><span class="sxs-lookup"><span data-stu-id="69156-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69156-144">-ServiceName</span></span>
<span data-ttu-id="69156-145">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="69156-145">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="69156-146">-Slot</span></span>
<span data-ttu-id="69156-147">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="69156-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="69156-148">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="69156-148">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="69156-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="69156-150">Gibt einen Speicherkonto Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="69156-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="69156-151">-StorageAccountKey</span></span>
<span data-ttu-id="69156-152">Gibt einen speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="69156-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69156-153">-StorageAccountName</span></span>
<span data-ttu-id="69156-154">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="69156-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-155">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="69156-155">-StorageContext</span></span>
<span data-ttu-id="69156-156">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="69156-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="69156-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="69156-158">Gibt einen Hashalgorithmus für Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69156-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="69156-159">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="69156-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-160">-Version</span><span class="sxs-lookup"><span data-stu-id="69156-160">-Version</span></span>
<span data-ttu-id="69156-161">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="69156-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="69156-162">-X509Certificate</span></span>
<span data-ttu-id="69156-163">Gibt ein X. 509-Zertifikat an, das bei Angabe automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69156-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69156-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69156-164">CommonParameters</span></span>
<span data-ttu-id="69156-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69156-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69156-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69156-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69156-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69156-167">INPUTS</span></span>

## <span data-ttu-id="69156-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69156-168">OUTPUTS</span></span>

## <span data-ttu-id="69156-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="69156-169">NOTES</span></span>

## <span data-ttu-id="69156-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69156-170">RELATED LINKS</span></span>

[<span data-ttu-id="69156-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="69156-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="69156-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="69156-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


