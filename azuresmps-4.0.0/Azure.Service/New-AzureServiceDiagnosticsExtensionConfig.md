---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006104"
---
# <span data-ttu-id="e429e-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="e429e-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="e429e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e429e-102">SYNOPSIS</span></span>
<span data-ttu-id="e429e-103">Generiert eine Konfiguration für eine Diagnose Erweiterung für die angegebene Rolle (n) oder alle Rollen.</span><span class="sxs-lookup"><span data-stu-id="e429e-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="e429e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e429e-104">SYNTAX</span></span>

### <span data-ttu-id="e429e-105">Erweiterung (Standard)</span><span class="sxs-lookup"><span data-stu-id="e429e-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e429e-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e429e-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e429e-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e429e-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e429e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e429e-108">DESCRIPTION</span></span>
<span data-ttu-id="e429e-109">Das Cmdlet **New-AzureServiceDiagnosticsExtensionConfig** generiert eine Konfiguration für eine Diagnose Erweiterung für angegebene Rollen oder alle Rollen.</span><span class="sxs-lookup"><span data-stu-id="e429e-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="e429e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e429e-110">EXAMPLES</span></span>

### <span data-ttu-id="e429e-111">Beispiel 1: Erstellen der Azure Diagnostics-Erweiterung für alle Rollen im clouddienst</span><span class="sxs-lookup"><span data-stu-id="e429e-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="e429e-112">Dieser Befehl erstellt die Azure Diagnostics-Erweiterung für alle Rollen im clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e429e-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="e429e-113">Beispiel 2: Erstellen der Azure Diagnostics-Erweiterung für eine Rolle</span><span class="sxs-lookup"><span data-stu-id="e429e-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="e429e-114">Dieser Befehl erstellt die Azure Diagnostics-Erweiterung für die Rolle WebRole01 im clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e429e-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="e429e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e429e-115">PARAMETERS</span></span>

### <span data-ttu-id="e429e-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e429e-116">-CertificateThumbprint</span></span>
<span data-ttu-id="e429e-117">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e429e-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e429e-118">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e429e-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e429e-119">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="e429e-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e429e-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="e429e-121">Gibt den Diagnose Konfigurationspfad an.</span><span class="sxs-lookup"><span data-stu-id="e429e-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-122">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="e429e-122">-ExtensionId</span></span>
<span data-ttu-id="e429e-123">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="e429e-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-124">-Information</span><span class="sxs-lookup"><span data-stu-id="e429e-124">-InformationAction</span></span>
<span data-ttu-id="e429e-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e429e-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e429e-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e429e-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e429e-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e429e-127">Continue</span></span>
- <span data-ttu-id="e429e-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e429e-128">Ignore</span></span>
- <span data-ttu-id="e429e-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e429e-129">Inquire</span></span>
- <span data-ttu-id="e429e-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e429e-130">SilentlyContinue</span></span>
- <span data-ttu-id="e429e-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="e429e-131">Stop</span></span>
- <span data-ttu-id="e429e-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e429e-132">Suspend</span></span>

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

### <span data-ttu-id="e429e-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e429e-133">-InformationVariable</span></span>
<span data-ttu-id="e429e-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e429e-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e429e-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="e429e-135">-Profile</span></span>
<span data-ttu-id="e429e-136">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e429e-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e429e-137">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e429e-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e429e-138">-Role</span><span class="sxs-lookup"><span data-stu-id="e429e-138">-Role</span></span>
<span data-ttu-id="e429e-139">Gibt ein optionales Array von Rollen an, um die Diagnose Konfiguration für anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e429e-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="e429e-140">Wenn nicht angegeben, wird die Diagnose Konfiguration als Standardkonfiguration für alle Rollen angewendet.</span><span class="sxs-lookup"><span data-stu-id="e429e-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="e429e-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="e429e-142">Gibt den Endpunkt des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="e429e-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e429e-143">-StorageAccountKey</span></span>
<span data-ttu-id="e429e-144">Gibt den speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="e429e-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e429e-145">-StorageAccountName</span></span>
<span data-ttu-id="e429e-146">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="e429e-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-147">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="e429e-147">-StorageContext</span></span>
<span data-ttu-id="e429e-148">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e429e-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e429e-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e429e-150">Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e429e-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e429e-151">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="e429e-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="e429e-152">-X509Certificate</span></span>
<span data-ttu-id="e429e-153">Gibt ein X. 509-Zertifikat an, das automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e429e-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e429e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e429e-154">CommonParameters</span></span>
<span data-ttu-id="e429e-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e429e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e429e-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e429e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e429e-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e429e-157">INPUTS</span></span>

## <span data-ttu-id="e429e-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e429e-158">OUTPUTS</span></span>

## <span data-ttu-id="e429e-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e429e-159">NOTES</span></span>

## <span data-ttu-id="e429e-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e429e-160">RELATED LINKS</span></span>

[<span data-ttu-id="e429e-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e429e-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="e429e-162">Satz-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e429e-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


