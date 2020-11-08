---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006019"
---
# <span data-ttu-id="7f3e3-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="7f3e3-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="7f3e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3e3-103">Aktiviert die Remote Desktop Erweiterung für bestimmte Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="7f3e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f3e3-104">SYNTAX</span></span>

### <span data-ttu-id="7f3e3-105">Setextension (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f3e3-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f3e3-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f3e3-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f3e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f3e3-107">DESCRIPTION</span></span>
<span data-ttu-id="7f3e3-108">Das Cmdlet " **Satz-AzureServiceRemoteDesktopExtension** " ermöglicht die Remote Desktop Erweiterung für bestimmte Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="7f3e3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f3e3-109">EXAMPLES</span></span>

### <span data-ttu-id="7f3e3-110">Beispiel 1: Aktivieren der Remote Desktop Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7f3e3-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="7f3e3-111">Mit diesem Befehl wird die Remote Desktop Erweiterung für den angegebenen Dienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="7f3e3-112">Beispiel 2: Aktivieren der Remote Desktop Erweiterung für eine bestimmte Rolle</span><span class="sxs-lookup"><span data-stu-id="7f3e3-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="7f3e3-113">Mit diesem Befehl wird die Remote Desktop Erweiterung für den angegebenen Dienst und die angegebene Rolle aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="7f3e3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f3e3-114">PARAMETERS</span></span>

### <span data-ttu-id="7f3e3-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f3e3-115">-CertificateThumbprint</span></span>
<span data-ttu-id="7f3e3-116">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="7f3e3-117">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="7f3e3-118">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3e3-119">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="7f3e3-119">-Credential</span></span>
<span data-ttu-id="7f3e3-120">Gibt die Anmeldeinformationen an, die für den Remote Desktop aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="7f3e3-121">Zu den Anmeldeinformationen gehören ein Benutzername und ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3e3-122">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="7f3e3-122">-Expiration</span></span>
<span data-ttu-id="7f3e3-123">Gibt ein Datum Zeit Objekt an, mit dem der Benutzer angeben kann, wann das Benutzerkonto abläuft.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3e3-124">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="7f3e3-124">-ExtensionId</span></span>
<span data-ttu-id="7f3e3-125">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3e3-126">-Information</span><span class="sxs-lookup"><span data-stu-id="7f3e3-126">-InformationAction</span></span>
<span data-ttu-id="7f3e3-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7f3e3-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7f3e3-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f3e3-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7f3e3-129">Continue</span></span>
- <span data-ttu-id="7f3e3-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7f3e3-130">Ignore</span></span>
- <span data-ttu-id="7f3e3-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7f3e3-131">Inquire</span></span>
- <span data-ttu-id="7f3e3-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f3e3-132">SilentlyContinue</span></span>
- <span data-ttu-id="7f3e3-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="7f3e3-133">Stop</span></span>
- <span data-ttu-id="7f3e3-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7f3e3-134">Suspend</span></span>

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

### <span data-ttu-id="7f3e3-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f3e3-135">-InformationVariable</span></span>
<span data-ttu-id="7f3e3-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f3e3-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="7f3e3-137">-Profile</span></span>
<span data-ttu-id="7f3e3-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f3e3-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f3e3-140">-Role</span><span class="sxs-lookup"><span data-stu-id="7f3e3-140">-Role</span></span>
<span data-ttu-id="7f3e3-141">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="7f3e3-142">Wenn dieser Parameter nicht angegeben wird, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="7f3e3-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f3e3-143">-ServiceName</span></span>
<span data-ttu-id="7f3e3-144">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="7f3e3-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="7f3e3-145">-Slot</span></span>
<span data-ttu-id="7f3e3-146">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="7f3e3-147">Die akzeptablen Werte für diesen Parameter sind: Production, Staging.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="7f3e3-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7f3e3-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7f3e3-149">Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="7f3e3-150">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="7f3e3-151">-Version</span><span class="sxs-lookup"><span data-stu-id="7f3e3-151">-Version</span></span>
<span data-ttu-id="7f3e3-152">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3e3-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="7f3e3-153">-X509Certificate</span></span>
<span data-ttu-id="7f3e3-154">Gibt ein x509-Zertifikat an, das automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="7f3e3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3e3-155">CommonParameters</span></span>
<span data-ttu-id="7f3e3-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3e3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3e3-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3e3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3e3-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f3e3-158">INPUTS</span></span>

## <span data-ttu-id="7f3e3-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f3e3-159">OUTPUTS</span></span>

## <span data-ttu-id="7f3e3-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f3e3-160">NOTES</span></span>

## <span data-ttu-id="7f3e3-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f3e3-161">RELATED LINKS</span></span>

[<span data-ttu-id="7f3e3-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="7f3e3-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


