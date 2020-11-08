---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006101"
---
# <span data-ttu-id="6a1be-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="6a1be-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="6a1be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a1be-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1be-103">Generiert eine Remote Desktop Erweiterungskonfiguration für eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6a1be-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="6a1be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a1be-104">SYNTAX</span></span>

### <span data-ttu-id="6a1be-105">Erweiterung (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a1be-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a1be-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a1be-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6a1be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a1be-107">DESCRIPTION</span></span>
<span data-ttu-id="6a1be-108">Das Cmdlet **New-AzureServiceRemoteDesktopExtensionConfig** generiert eine Konfiguration für eine Remote Desktop Erweiterung für eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6a1be-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="6a1be-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a1be-109">EXAMPLES</span></span>

### <span data-ttu-id="6a1be-110">Beispiel 1: Erstellen einer Remote Desktop Erweiterungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="6a1be-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="6a1be-111">Mit diesem Befehl wird eine Remote Desktop Erweiterungskonfiguration für die angegebenen Anmeldeinformationen generiert.</span><span class="sxs-lookup"><span data-stu-id="6a1be-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="6a1be-112">Beispiel 2: Generieren einer Remote Desktop Erweiterungskonfiguration für eine angegebene Rolle</span><span class="sxs-lookup"><span data-stu-id="6a1be-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="6a1be-113">Mit diesem Befehl wird eine Remote Desktop Erweiterungskonfiguration für die angegebenen Anmeldeinformationen und die WebRole01-Rolle generiert.</span><span class="sxs-lookup"><span data-stu-id="6a1be-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="6a1be-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a1be-114">PARAMETERS</span></span>

### <span data-ttu-id="6a1be-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a1be-115">-CertificateThumbprint</span></span>
<span data-ttu-id="6a1be-116">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a1be-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="6a1be-117">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6a1be-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="6a1be-118">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="6a1be-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="6a1be-119">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="6a1be-119">-Credential</span></span>
<span data-ttu-id="6a1be-120">Gibt die Anmeldeinformationen an, die für den Remote Desktop aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6a1be-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="6a1be-121">Zu den Anmeldeinformationen gehören ein Benutzername und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="6a1be-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1be-122">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="6a1be-122">-Expiration</span></span>
<span data-ttu-id="6a1be-123">Gibt ein **DateTime** -Objekt an, mit dem der Benutzer angeben kann, wann das Benutzerkonto abläuft.</span><span class="sxs-lookup"><span data-stu-id="6a1be-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1be-124">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="6a1be-124">-ExtensionId</span></span>
<span data-ttu-id="6a1be-125">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="6a1be-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1be-126">-Information</span><span class="sxs-lookup"><span data-stu-id="6a1be-126">-InformationAction</span></span>
<span data-ttu-id="6a1be-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6a1be-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a1be-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6a1be-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a1be-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6a1be-129">Continue</span></span>
- <span data-ttu-id="6a1be-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6a1be-130">Ignore</span></span>
- <span data-ttu-id="6a1be-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6a1be-131">Inquire</span></span>
- <span data-ttu-id="6a1be-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a1be-132">SilentlyContinue</span></span>
- <span data-ttu-id="6a1be-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="6a1be-133">Stop</span></span>
- <span data-ttu-id="6a1be-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6a1be-134">Suspend</span></span>

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

### <span data-ttu-id="6a1be-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a1be-135">-InformationVariable</span></span>
<span data-ttu-id="6a1be-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6a1be-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6a1be-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a1be-137">-Profile</span></span>
<span data-ttu-id="6a1be-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6a1be-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a1be-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6a1be-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a1be-140">-Role</span><span class="sxs-lookup"><span data-stu-id="6a1be-140">-Role</span></span>
<span data-ttu-id="6a1be-141">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a1be-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="6a1be-142">Wenn dieser Parameter nicht angegeben wird, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a1be-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="6a1be-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6a1be-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6a1be-144">Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6a1be-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="6a1be-145">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="6a1be-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="6a1be-146">-Version</span><span class="sxs-lookup"><span data-stu-id="6a1be-146">-Version</span></span>
<span data-ttu-id="6a1be-147">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="6a1be-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1be-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="6a1be-148">-X509Certificate</span></span>
<span data-ttu-id="6a1be-149">Gibt ein x509-Zertifikat an, das bei Angabe automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a1be-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="6a1be-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1be-150">CommonParameters</span></span>
<span data-ttu-id="6a1be-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1be-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1be-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a1be-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1be-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a1be-153">INPUTS</span></span>

## <span data-ttu-id="6a1be-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a1be-154">OUTPUTS</span></span>

## <span data-ttu-id="6a1be-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a1be-155">NOTES</span></span>

## <span data-ttu-id="6a1be-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a1be-156">RELATED LINKS</span></span>

[<span data-ttu-id="6a1be-157">Satz-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="6a1be-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


