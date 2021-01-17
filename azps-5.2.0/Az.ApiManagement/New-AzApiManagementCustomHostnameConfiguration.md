---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369493"
---
# <span data-ttu-id="0902e-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0902e-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="0902e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0902e-102">SYNOPSIS</span></span>
<span data-ttu-id="0902e-103">Erstellt eine Instanz von `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="0902e-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="0902e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0902e-104">SYNTAX</span></span>

### <span data-ttu-id="0902e-105">NoChangeCertificate (Standard)</span><span class="sxs-lookup"><span data-stu-id="0902e-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0902e-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="0902e-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0902e-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="0902e-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0902e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0902e-108">DESCRIPTION</span></span>
<span data-ttu-id="0902e-109">Das **Cmdlet "New-AzApiManagementCustomHostnameConfiguration"** ist ein Hilfsbefehl, der eine Instanz von **"PsApiManagementCustomHostNameConfiguration" erstellt.**</span><span class="sxs-lookup"><span data-stu-id="0902e-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="0902e-110">Dieser Befehl wird mit dem Cmdlet New-AzApiManagement und Set-AzApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="0902e-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="0902e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0902e-111">EXAMPLES</span></span>

### <span data-ttu-id="0902e-112">Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mithilfe eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="0902e-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="0902e-113">Mit diesem Befehl wird eine Instanz von **"PsApiManagementCustomHostNameConfiguration** for Portal" erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="0902e-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="0902e-114">Anschließend erstellt er einen neuen ApiManagement-Dienst mit benutzerdefinierter Hostnamenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0902e-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="0902e-115">Beispiel 2: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mithilfe eines Geheimschlüssels aus der KeyVault-Ressource</span><span class="sxs-lookup"><span data-stu-id="0902e-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="0902e-116">Mit diesem Befehl wird eine Instanz von **"PsApiManagementCustomHostNameConfiguration" erstellt und initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="0902e-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="0902e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0902e-117">PARAMETERS</span></span>

### <span data-ttu-id="0902e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0902e-118">-DefaultProfile</span></span>
<span data-ttu-id="0902e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0902e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0902e-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="0902e-120">-DefaultSslBinding</span></span>
<span data-ttu-id="0902e-121">Bestimmt, ob der Wert ein geheimer Wert ist und verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0902e-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="0902e-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0902e-122">This parameter is optional.</span></span>
<span data-ttu-id="0902e-123">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="0902e-123">Default Value is false.</span></span>

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

### <span data-ttu-id="0902e-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="0902e-124">-Hostname</span></span>
<span data-ttu-id="0902e-125">Benutzerdefinierter Hostname</span><span class="sxs-lookup"><span data-stu-id="0902e-125">Custom Hostname</span></span>

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

### <span data-ttu-id="0902e-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="0902e-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="0902e-127">Vorhandene Zertifikatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0902e-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="0902e-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="0902e-128">-HostnameType</span></span>
<span data-ttu-id="0902e-129">Hostnametyp</span><span class="sxs-lookup"><span data-stu-id="0902e-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0902e-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0902e-130">-KeyVaultId</span></span>
<span data-ttu-id="0902e-131">KeyVaultId zum geheimen Speichern des benutzerdefinierten SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="0902e-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="0902e-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0902e-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="0902e-133">Bestimmt, ob der Wert ein geheimer Wert ist und verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0902e-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="0902e-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0902e-134">This parameter is optional.</span></span>
<span data-ttu-id="0902e-135">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="0902e-135">Default Value is false.</span></span>

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

### <span data-ttu-id="0902e-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="0902e-136">-PfxPassword</span></span>
<span data-ttu-id="0902e-137">Kennwort für die PFX-Zertifikatdatei.</span><span class="sxs-lookup"><span data-stu-id="0902e-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="0902e-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="0902e-138">-PfxPath</span></span>
<span data-ttu-id="0902e-139">Pfad zu einer PFX-Zertifikatdatei.</span><span class="sxs-lookup"><span data-stu-id="0902e-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="0902e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0902e-140">CommonParameters</span></span>
<span data-ttu-id="0902e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0902e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0902e-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0902e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0902e-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0902e-143">INPUTS</span></span>

### <span data-ttu-id="0902e-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="0902e-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="0902e-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0902e-145">OUTPUTS</span></span>

### <span data-ttu-id="0902e-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0902e-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="0902e-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0902e-147">NOTES</span></span>

## <span data-ttu-id="0902e-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0902e-148">RELATED LINKS</span></span>

[<span data-ttu-id="0902e-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0902e-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0902e-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0902e-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)