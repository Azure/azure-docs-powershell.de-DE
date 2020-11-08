---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006254"
---
# <span data-ttu-id="cd20b-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cd20b-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="cd20b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd20b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd20b-103">Aktiviert eine AD-Domänenerweiterung für einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="cd20b-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="cd20b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd20b-104">SYNTAX</span></span>

### <span data-ttu-id="cd20b-105">JoinDomainUsingEnumOptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd20b-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd20b-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="cd20b-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd20b-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="cd20b-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd20b-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd20b-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd20b-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd20b-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd20b-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd20b-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cd20b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd20b-111">DESCRIPTION</span></span>
<span data-ttu-id="cd20b-112">Das Cmdlet " **Satz-AzureServiceADDomainExtension** " aktiviert eine AD-Domänenerweiterung (Active Directory) für einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="cd20b-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="cd20b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd20b-113">EXAMPLES</span></span>

### <span data-ttu-id="cd20b-114">1:</span><span class="sxs-lookup"><span data-stu-id="cd20b-114">1:</span></span>
```

```

## <span data-ttu-id="cd20b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd20b-115">PARAMETERS</span></span>

### <span data-ttu-id="cd20b-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd20b-116">-CertificateThumbprint</span></span>
<span data-ttu-id="cd20b-117">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd20b-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="cd20b-118">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cd20b-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="cd20b-119">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="cd20b-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-120">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="cd20b-120">-Credential</span></span>
<span data-ttu-id="cd20b-121">Gibt die Anmeldeinformationen für die Teilnahme an der anzeigen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="cd20b-122">Zu den Anmeldeinformationen gehören ein Benutzername und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="cd20b-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-123">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="cd20b-123">-DomainName</span></span>
<span data-ttu-id="cd20b-124">Gibt den Namen der AD-Domäne an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-125">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="cd20b-125">-ExtensionId</span></span>
<span data-ttu-id="cd20b-126">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-127">-Information</span><span class="sxs-lookup"><span data-stu-id="cd20b-127">-InformationAction</span></span>
<span data-ttu-id="cd20b-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="cd20b-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cd20b-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd20b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd20b-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="cd20b-130">Continue</span></span>
- <span data-ttu-id="cd20b-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="cd20b-131">Ignore</span></span>
- <span data-ttu-id="cd20b-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="cd20b-132">Inquire</span></span>
- <span data-ttu-id="cd20b-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cd20b-133">SilentlyContinue</span></span>
- <span data-ttu-id="cd20b-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="cd20b-134">Stop</span></span>
- <span data-ttu-id="cd20b-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="cd20b-135">Suspend</span></span>

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

### <span data-ttu-id="cd20b-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cd20b-136">-InformationVariable</span></span>
<span data-ttu-id="cd20b-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cd20b-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="cd20b-138">-JoinOption</span></span>
<span data-ttu-id="cd20b-139">Gibt die Join-Options-Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-140">-Optionen</span><span class="sxs-lookup"><span data-stu-id="cd20b-140">-Options</span></span>
<span data-ttu-id="cd20b-141">Gibt die Join-Option "unsignierte Ganzzahl" an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="cd20b-142">-OUPath</span></span>
<span data-ttu-id="cd20b-143">Gibt den Organisations Einheits Pfad für den AD-Domänen Join-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd20b-144">-Profile</span></span>
<span data-ttu-id="cd20b-145">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="cd20b-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd20b-146">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="cd20b-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd20b-147">-Neu starten</span><span class="sxs-lookup"><span data-stu-id="cd20b-147">-Restart</span></span>
<span data-ttu-id="cd20b-148">Gibt an, ob der Computer neu gestartet werden soll, wenn der Join-Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cd20b-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-149">-Role</span><span class="sxs-lookup"><span data-stu-id="cd20b-149">-Role</span></span>
<span data-ttu-id="cd20b-150">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd20b-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="cd20b-151">Wenn nicht angegeben, wird die AD-Domänenkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd20b-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd20b-152">-ServiceName</span></span>
<span data-ttu-id="cd20b-153">Gibt den Namen des Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="cd20b-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="cd20b-154">-Slot</span></span>
<span data-ttu-id="cd20b-155">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd20b-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="cd20b-156">Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="cd20b-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="cd20b-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="cd20b-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="cd20b-158">Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd20b-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="cd20b-159">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="cd20b-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="cd20b-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="cd20b-161">Gibt die Anmeldeinformationen (Benutzername und Kennwort) an, um die Teilnahme an der AD-Domäne aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="cd20b-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-162">-Version</span><span class="sxs-lookup"><span data-stu-id="cd20b-162">-Version</span></span>
<span data-ttu-id="cd20b-163">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="cd20b-164">-WorkgroupName</span></span>
<span data-ttu-id="cd20b-165">Gibt den Namen der Arbeitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd20b-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="cd20b-166">-X509Certificate</span></span>
<span data-ttu-id="cd20b-167">Gibt ein x509-Zertifikat an, das bei Angabe automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd20b-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd20b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd20b-168">CommonParameters</span></span>
<span data-ttu-id="cd20b-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd20b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd20b-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd20b-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd20b-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd20b-171">INPUTS</span></span>

## <span data-ttu-id="cd20b-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd20b-172">OUTPUTS</span></span>

## <span data-ttu-id="cd20b-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd20b-173">NOTES</span></span>

## <span data-ttu-id="cd20b-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd20b-174">RELATED LINKS</span></span>

[<span data-ttu-id="cd20b-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cd20b-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="cd20b-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cd20b-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="cd20b-177">Neu – AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="cd20b-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


