---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006103"
---
# <span data-ttu-id="6453e-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="6453e-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="6453e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6453e-102">SYNOPSIS</span></span>
<span data-ttu-id="6453e-103">Generiert die Konfiguration für die AD-Domänenerweiterung für Cloud-Dienste.</span><span class="sxs-lookup"><span data-stu-id="6453e-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="6453e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6453e-104">SYNTAX</span></span>

### <span data-ttu-id="6453e-105">JoinDomainUsingEnumOptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="6453e-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6453e-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="6453e-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6453e-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="6453e-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6453e-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="6453e-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6453e-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="6453e-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6453e-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="6453e-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6453e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6453e-111">DESCRIPTION</span></span>
<span data-ttu-id="6453e-112">Das Cmdlet **New-AzureServiceADDomainExtensionConfig** generiert die Konfiguration für die Active Directory-Domänenerweiterung (AD) für Cloud-Dienste.</span><span class="sxs-lookup"><span data-stu-id="6453e-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="6453e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6453e-113">EXAMPLES</span></span>

### <span data-ttu-id="6453e-114">Beispiel 1: Angeben einer AD-Domänenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6453e-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="6453e-115">Mit diesem Befehl wird eine Konfiguration für die AD-Domänenerweiterung generiert.</span><span class="sxs-lookup"><span data-stu-id="6453e-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="6453e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6453e-116">PARAMETERS</span></span>

### <span data-ttu-id="6453e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6453e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="6453e-118">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6453e-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="6453e-119">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6453e-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="6453e-120">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="6453e-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-121">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="6453e-121">-Credential</span></span>
<span data-ttu-id="6453e-122">Gibt die Anmeldeinformationen an, die für die Teilnahme an der anzeigen Domäne verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6453e-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="6453e-123">Zu den Anmeldeinformationen gehören ein Benutzername und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="6453e-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-124">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="6453e-124">-DomainName</span></span>
<span data-ttu-id="6453e-125">Gibt den Namen der AD-Domäne an.</span><span class="sxs-lookup"><span data-stu-id="6453e-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-126">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="6453e-126">-ExtensionId</span></span>
<span data-ttu-id="6453e-127">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="6453e-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-128">-Information</span><span class="sxs-lookup"><span data-stu-id="6453e-128">-InformationAction</span></span>
<span data-ttu-id="6453e-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6453e-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6453e-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6453e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6453e-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6453e-131">Continue</span></span>
- <span data-ttu-id="6453e-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6453e-132">Ignore</span></span>
- <span data-ttu-id="6453e-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6453e-133">Inquire</span></span>
- <span data-ttu-id="6453e-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6453e-134">SilentlyContinue</span></span>
- <span data-ttu-id="6453e-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="6453e-135">Stop</span></span>
- <span data-ttu-id="6453e-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6453e-136">Suspend</span></span>

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

### <span data-ttu-id="6453e-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6453e-137">-InformationVariable</span></span>
<span data-ttu-id="6453e-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6453e-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6453e-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="6453e-139">-JoinOption</span></span>
<span data-ttu-id="6453e-140">Gibt die Join-Options-Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="6453e-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-141">-Optionen</span><span class="sxs-lookup"><span data-stu-id="6453e-141">-Options</span></span>
<span data-ttu-id="6453e-142">Gibt die Join-Option "unsignierte Ganzzahl" an.</span><span class="sxs-lookup"><span data-stu-id="6453e-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="6453e-143">-OUPath</span></span>
<span data-ttu-id="6453e-144">Gibt den Organisations Einheits Pfad für den AD-Domänen Join-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="6453e-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="6453e-145">-Profile</span></span>
<span data-ttu-id="6453e-146">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6453e-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6453e-147">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6453e-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6453e-148">-Neu starten</span><span class="sxs-lookup"><span data-stu-id="6453e-148">-Restart</span></span>
<span data-ttu-id="6453e-149">Gibt an, ob der Computer neu gestartet werden soll, wenn der Join-Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6453e-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-150">-Role</span><span class="sxs-lookup"><span data-stu-id="6453e-150">-Role</span></span>
<span data-ttu-id="6453e-151">Gibt ein optionales Array von Rollen an, um die Remote Desktopkonfiguration für die AD-Domänenkonfiguration anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6453e-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="6453e-152">Wenn Sie diesen Parameter nicht angeben, wird die AD-Domänenkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6453e-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6453e-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6453e-154">Gibt einen Hashalgorithmus für Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6453e-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="6453e-155">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="6453e-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="6453e-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="6453e-157">Gibt die Anmeldeinformationen (Benutzername und Kennwort) an, um die Teilnahme an der AD-Domäne aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6453e-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-158">-Version</span><span class="sxs-lookup"><span data-stu-id="6453e-158">-Version</span></span>
<span data-ttu-id="6453e-159">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="6453e-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="6453e-160">-WorkgroupName</span></span>
<span data-ttu-id="6453e-161">Gibt den Namen der Arbeitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="6453e-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="6453e-162">-X509Certificate</span></span>
<span data-ttu-id="6453e-163">Gibt ein X. 509-Zertifikat an, das automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6453e-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6453e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6453e-164">CommonParameters</span></span>
<span data-ttu-id="6453e-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6453e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6453e-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6453e-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6453e-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6453e-167">INPUTS</span></span>

## <span data-ttu-id="6453e-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6453e-168">OUTPUTS</span></span>

## <span data-ttu-id="6453e-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="6453e-169">NOTES</span></span>

## <span data-ttu-id="6453e-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6453e-170">RELATED LINKS</span></span>

[<span data-ttu-id="6453e-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6453e-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="6453e-172">Satz-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6453e-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


