---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006102"
---
# <span data-ttu-id="d05e6-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="d05e6-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="d05e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d05e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d05e6-103">Erstellt eine Cloud-Dienst Erweiterungskonfiguration für eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d05e6-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="d05e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d05e6-104">SYNTAX</span></span>

### <span data-ttu-id="d05e6-105">Erweiterung (Standard)</span><span class="sxs-lookup"><span data-stu-id="d05e6-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d05e6-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="d05e6-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d05e6-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d05e6-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d05e6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d05e6-108">DESCRIPTION</span></span>
<span data-ttu-id="d05e6-109">Das Cmdlet **New-AzureServiceExtensionConfig** erstellt eine Cloud-Dienst Erweiterungskonfiguration für eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d05e6-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="d05e6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d05e6-110">EXAMPLES</span></span>

### <span data-ttu-id="d05e6-111">Beispiel 1: Erstellen einer Erweiterungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="d05e6-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="d05e6-112">Mit diesem Befehl wird eine Erweiterungskonfiguration angegeben.</span><span class="sxs-lookup"><span data-stu-id="d05e6-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="d05e6-113">Beispiel 2: Erstellen einer Erweiterungskonfiguration für eine Rolle</span><span class="sxs-lookup"><span data-stu-id="d05e6-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="d05e6-114">Dieser Befehl gibt eine Erweiterungskonfiguration für die Rolle WebRole1.</span><span class="sxs-lookup"><span data-stu-id="d05e6-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="d05e6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d05e6-115">PARAMETERS</span></span>

### <span data-ttu-id="d05e6-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d05e6-116">-CertificateThumbprint</span></span>
<span data-ttu-id="d05e6-117">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d05e6-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="d05e6-118">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d05e6-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="d05e6-119">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="d05e6-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="d05e6-120">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="d05e6-120">-ExtensionId</span></span>
<span data-ttu-id="d05e6-121">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d05e6-122">-ExtensionName</span></span>
<span data-ttu-id="d05e6-123">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="d05e6-124">-ExtensionState</span></span>
<span data-ttu-id="d05e6-125">Gibt den Zustand der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="d05e6-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d05e6-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d05e6-127">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="d05e6-127">Enable</span></span> 
- <span data-ttu-id="d05e6-128">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d05e6-128">Disable</span></span> 
- <span data-ttu-id="d05e6-129">Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="d05e6-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-130">-Information</span><span class="sxs-lookup"><span data-stu-id="d05e6-130">-InformationAction</span></span>
<span data-ttu-id="d05e6-131">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d05e6-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d05e6-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d05e6-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d05e6-133">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d05e6-133">Continue</span></span>
- <span data-ttu-id="d05e6-134">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d05e6-134">Ignore</span></span>
- <span data-ttu-id="d05e6-135">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d05e6-135">Inquire</span></span>
- <span data-ttu-id="d05e6-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d05e6-136">SilentlyContinue</span></span>
- <span data-ttu-id="d05e6-137">Beenden</span><span class="sxs-lookup"><span data-stu-id="d05e6-137">Stop</span></span>
- <span data-ttu-id="d05e6-138">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d05e6-138">Suspend</span></span>

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

### <span data-ttu-id="d05e6-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d05e6-139">-InformationVariable</span></span>
<span data-ttu-id="d05e6-140">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d05e6-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05e6-141">-PrivateConfiguration</span></span>
<span data-ttu-id="d05e6-142">Gibt den privaten Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="d05e6-143">-Profile</span></span>
<span data-ttu-id="d05e6-144">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d05e6-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d05e6-145">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d05e6-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d05e6-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d05e6-146">-ProviderNamespace</span></span>
<span data-ttu-id="d05e6-147">Gibt den Anbieter Namespace der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="d05e6-148">-PublicConfiguration</span></span>
<span data-ttu-id="d05e6-149">Gibt den öffentlichen Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d05e6-150">-Role</span><span class="sxs-lookup"><span data-stu-id="d05e6-150">-Role</span></span>
<span data-ttu-id="d05e6-151">Gibt ein optionales Array von Rollen an, für die die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d05e6-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="d05e6-152">Wenn nicht angegeben, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d05e6-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="d05e6-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d05e6-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="d05e6-154">Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d05e6-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="d05e6-155">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="d05e6-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="d05e6-156">-Version</span><span class="sxs-lookup"><span data-stu-id="d05e6-156">-Version</span></span>
<span data-ttu-id="d05e6-157">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="d05e6-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="d05e6-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="d05e6-158">-X509Certificate</span></span>
<span data-ttu-id="d05e6-159">Gibt ein x509-Zertifikat an, das bei Angabe automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d05e6-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="d05e6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05e6-160">CommonParameters</span></span>
<span data-ttu-id="d05e6-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d05e6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05e6-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05e6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05e6-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d05e6-163">INPUTS</span></span>

## <span data-ttu-id="d05e6-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d05e6-164">OUTPUTS</span></span>

## <span data-ttu-id="d05e6-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="d05e6-165">NOTES</span></span>

## <span data-ttu-id="d05e6-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d05e6-166">RELATED LINKS</span></span>

[<span data-ttu-id="d05e6-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d05e6-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="d05e6-168">Satz-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d05e6-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


