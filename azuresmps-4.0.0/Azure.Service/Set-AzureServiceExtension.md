---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005653"
---
# <span data-ttu-id="c6af7-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c6af7-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="c6af7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6af7-102">SYNOPSIS</span></span>
<span data-ttu-id="c6af7-103">Fügt eine Cloud-Diensterweiterung zu einer Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6af7-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="c6af7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6af7-104">SYNTAX</span></span>

### <span data-ttu-id="c6af7-105">Setextension (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6af7-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c6af7-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="c6af7-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6af7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6af7-107">DESCRIPTION</span></span>
<span data-ttu-id="c6af7-108">Das Cmdlet " **Satz-AzureServiceExtension** " fügt eine Cloud-Diensterweiterung zu einer Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6af7-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="c6af7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6af7-109">EXAMPLES</span></span>

### <span data-ttu-id="c6af7-110">Beispiel 1: Hinzufügen eines Cloud-Diensts zu einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c6af7-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="c6af7-111">Dieser Befehl fügt einen clouddienst zu einer Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6af7-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="c6af7-112">Beispiel 2: Hinzufügen eines Cloud-Diensts zu einer Bereitstellung für eine bestimmte Rolle</span><span class="sxs-lookup"><span data-stu-id="c6af7-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="c6af7-113">Dieser Befehl fügt einen clouddienst zu einer Bereitstellung für eine bestimmte Rolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6af7-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="c6af7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6af7-114">PARAMETERS</span></span>

### <span data-ttu-id="c6af7-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c6af7-115">-CertificateThumbprint</span></span>
<span data-ttu-id="c6af7-116">Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6af7-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="c6af7-117">Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c6af7-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="c6af7-118">Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c6af7-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="c6af7-119">-Erweiterungs-Nr</span><span class="sxs-lookup"><span data-stu-id="c6af7-119">-ExtensionId</span></span>
<span data-ttu-id="c6af7-120">Gibt die Erweiterungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-120">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="c6af7-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c6af7-121">-ExtensionName</span></span>
<span data-ttu-id="c6af7-122">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6af7-123">-Information</span><span class="sxs-lookup"><span data-stu-id="c6af7-123">-InformationAction</span></span>
<span data-ttu-id="c6af7-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c6af7-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6af7-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c6af7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6af7-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c6af7-126">Continue</span></span>
- <span data-ttu-id="c6af7-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c6af7-127">Ignore</span></span>
- <span data-ttu-id="c6af7-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c6af7-128">Inquire</span></span>
- <span data-ttu-id="c6af7-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6af7-129">SilentlyContinue</span></span>
- <span data-ttu-id="c6af7-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="c6af7-130">Stop</span></span>
- <span data-ttu-id="c6af7-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c6af7-131">Suspend</span></span>

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

### <span data-ttu-id="c6af7-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6af7-132">-InformationVariable</span></span>
<span data-ttu-id="c6af7-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6af7-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6af7-134">-PrivateConfiguration</span></span>
<span data-ttu-id="c6af7-135">Gibt den privaten Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6af7-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6af7-136">-Profile</span></span>
<span data-ttu-id="c6af7-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c6af7-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6af7-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c6af7-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6af7-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c6af7-139">-ProviderNamespace</span></span>
<span data-ttu-id="c6af7-140">Gibt den Namespace des Erweiterungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6af7-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6af7-141">-PublicConfiguration</span></span>
<span data-ttu-id="c6af7-142">Gibt den öffentlichen Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6af7-143">-Role</span><span class="sxs-lookup"><span data-stu-id="c6af7-143">-Role</span></span>
<span data-ttu-id="c6af7-144">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6af7-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="c6af7-145">Wenn dieser Parameter nicht angegeben wird, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6af7-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="c6af7-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6af7-146">-ServiceName</span></span>
<span data-ttu-id="c6af7-147">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="c6af7-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="c6af7-148">-Slot</span></span>
<span data-ttu-id="c6af7-149">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6af7-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="c6af7-150">Gültige Werte sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="c6af7-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="c6af7-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c6af7-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c6af7-152">Gibt den Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c6af7-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="c6af7-153">Dieser Parameter ist optional, und der Standardwert ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="c6af7-153">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="c6af7-154">-Version</span><span class="sxs-lookup"><span data-stu-id="c6af7-154">-Version</span></span>
<span data-ttu-id="c6af7-155">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="c6af7-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6af7-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="c6af7-156">-X509Certificate</span></span>
<span data-ttu-id="c6af7-157">Gibt ein X. 509-Zertifikat an, das automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6af7-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="c6af7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6af7-158">CommonParameters</span></span>
<span data-ttu-id="c6af7-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6af7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6af7-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6af7-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6af7-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6af7-161">INPUTS</span></span>

## <span data-ttu-id="c6af7-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6af7-162">OUTPUTS</span></span>

## <span data-ttu-id="c6af7-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6af7-163">NOTES</span></span>

## <span data-ttu-id="c6af7-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6af7-164">RELATED LINKS</span></span>

[<span data-ttu-id="c6af7-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c6af7-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="c6af7-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c6af7-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


