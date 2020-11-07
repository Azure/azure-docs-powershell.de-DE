---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663721"
---
# <span data-ttu-id="7efb3-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efb3-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="7efb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7efb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7efb3-103">Erstellt eine Instanz von `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="7efb3-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7efb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7efb3-104">SYNTAX</span></span>

### <span data-ttu-id="7efb3-105">NoChangeCertificate (Standard)</span><span class="sxs-lookup"><span data-stu-id="7efb3-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7efb3-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="7efb3-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7efb3-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="7efb3-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7efb3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7efb3-108">DESCRIPTION</span></span>
<span data-ttu-id="7efb3-109">Das Cmdlet **New-AzureRmApiManagementCustomHostnameConfiguration** ist ein Hilfsbefehl, mit dem eine Instanz von **PsApiManagementCustomHostNameConfiguration** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7efb3-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="7efb3-110">Dieser Befehl wird mit dem Cmdlet New-AzureRmApiManagement und Set-AzureRmApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="7efb3-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="7efb3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7efb3-111">EXAMPLES</span></span>

### <span data-ttu-id="7efb3-112">Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem SSL-Zertifikat aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="7efb3-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="7efb3-113">Dieser Befehl erstellt und Initialisiert eine Instanz von **PsApiManagementCustomHostNameConfiguration** für Portal.</span><span class="sxs-lookup"><span data-stu-id="7efb3-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="7efb3-114">Anschließend wird ein neuer ApiManagement-Dienst mit benutzerdefinierter Hostname-Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="7efb3-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="7efb3-115">Beispiel 2: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem Schlüssel aus der keyvault-Ressource</span><span class="sxs-lookup"><span data-stu-id="7efb3-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="7efb3-116">Dieser Befehl erstellt und Initialisiert eine Instanz von **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7efb3-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="7efb3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7efb3-117">PARAMETERS</span></span>

### <span data-ttu-id="7efb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efb3-118">-DefaultProfile</span></span>
<span data-ttu-id="7efb3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7efb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="7efb3-120">-DefaultSslBinding</span></span>
<span data-ttu-id="7efb3-121">Bestimmt, ob es sich um einen geheimen Wert handelt, der verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efb3-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="7efb3-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7efb3-122">This parameter is optional.</span></span>
<span data-ttu-id="7efb3-123">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="7efb3-123">Default Value is false.</span></span>

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

### <span data-ttu-id="7efb3-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="7efb3-124">-Hostname</span></span>
<span data-ttu-id="7efb3-125">Benutzerdefinierter Hostname</span><span class="sxs-lookup"><span data-stu-id="7efb3-125">Custom Hostname</span></span>

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

### <span data-ttu-id="7efb3-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="7efb3-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="7efb3-127">Vorhandene Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7efb3-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-128">-HostNameType</span><span class="sxs-lookup"><span data-stu-id="7efb3-128">-HostnameType</span></span>
<span data-ttu-id="7efb3-129">Hostname-Typ</span><span class="sxs-lookup"><span data-stu-id="7efb3-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-130">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="7efb3-130">-KeyVaultId</span></span>
<span data-ttu-id="7efb3-131">Keyvault-to-Secret, die das benutzerdefinierte SSL-Zertifikat speichert.</span><span class="sxs-lookup"><span data-stu-id="7efb3-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7efb3-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="7efb3-133">Bestimmt, ob es sich um einen geheimen Wert handelt, der verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efb3-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="7efb3-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7efb3-134">This parameter is optional.</span></span>
<span data-ttu-id="7efb3-135">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="7efb3-135">Default Value is false.</span></span>

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

### <span data-ttu-id="7efb3-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="7efb3-136">-PfxPassword</span></span>
<span data-ttu-id="7efb3-137">Kennwort für die PFX-Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="7efb3-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="7efb3-138">-PfxPath</span></span>
<span data-ttu-id="7efb3-139">Pfad zu einer PFX-Zertifikatsdatei</span><span class="sxs-lookup"><span data-stu-id="7efb3-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efb3-140">CommonParameters</span></span>
<span data-ttu-id="7efb3-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efb3-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efb3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efb3-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7efb3-143">INPUTS</span></span>

### <span data-ttu-id="7efb3-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="7efb3-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="7efb3-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7efb3-145">OUTPUTS</span></span>

### <span data-ttu-id="7efb3-146">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efb3-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="7efb3-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7efb3-147">NOTES</span></span>

## <span data-ttu-id="7efb3-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7efb3-148">RELATED LINKS</span></span>

[<span data-ttu-id="7efb3-149">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7efb3-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="7efb3-150">Satz-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7efb3-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
