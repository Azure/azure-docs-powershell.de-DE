---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149036"
---
# <span data-ttu-id="4f9f2-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="4f9f2-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="4f9f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9f2-103">Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="4f9f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f9f2-104">SYNTAX</span></span>

### <span data-ttu-id="4f9f2-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f9f2-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f9f2-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="4f9f2-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f9f2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="4f9f2-108">Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="4f9f2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f9f2-109">EXAMPLES</span></span>

### <span data-ttu-id="4f9f2-110">Beispiel 1: Öffentliche IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="4f9f2-111">Ruft die öffentlichen IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen ab.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="4f9f2-112">Beispiel 2: Öffentliche IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="4f9f2-113">Ruft die öffentlichen IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="4f9f2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f9f2-114">PARAMETERS</span></span>

### <span data-ttu-id="4f9f2-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="4f9f2-115">-CloudService</span></span>
<span data-ttu-id="4f9f2-116">CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-116">CloudService instance.</span></span>
<span data-ttu-id="4f9f2-117">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9f2-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="4f9f2-118">-CloudServiceName</span></span>
<span data-ttu-id="4f9f2-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-119">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f9f2-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-121">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9f2-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f9f2-122">-SubscriptionId</span></span>
<span data-ttu-id="4f9f2-123">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-123">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9f2-124">CommonParameters</span></span>
<span data-ttu-id="4f9f2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9f2-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f9f2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9f2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f9f2-127">INPUTS</span></span>

## <span data-ttu-id="4f9f2-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f9f2-128">OUTPUTS</span></span>

## <span data-ttu-id="4f9f2-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f9f2-129">NOTES</span></span>

<span data-ttu-id="4f9f2-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4f9f2-130">ALIASES</span></span>

<span data-ttu-id="4f9f2-131">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4f9f2-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f9f2-132">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f9f2-133">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f9f2-134"><CloudService>CLOUDSERVICE: CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="4f9f2-135">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="4f9f2-136">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="4f9f2-137">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="4f9f2-138">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="4f9f2-139">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="4f9f2-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="4f9f2-141">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="4f9f2-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform automatisch ein Upgrade von "typeHandlerVersion" auf höhere Nebenversionen durchführen kann, sobald diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="4f9f2-143">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="4f9f2-144">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="4f9f2-145">Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="4f9f2-146">Wenn weder forceUpdateTag noch irgendeine der öffentlichen oder geschützten Einstellungen geändert wird, würde die Erweiterung zu der Rolleninstanz mit derselben Sequenznummer fließen, und es ist aufgabe der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="4f9f2-147">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="4f9f2-148">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="4f9f2-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4f9f2-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="4f9f2-150">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="4f9f2-151">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="4f9f2-152">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="4f9f2-153">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="4f9f2-154">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="4f9f2-155">Bei einer XML-Erweiterung (wie RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="4f9f2-156">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f9f2-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="4f9f2-157">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="4f9f2-158">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="4f9f2-159">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-159">Specifies the version of the extension.</span></span> <span data-ttu-id="4f9f2-160">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="4f9f2-161">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="4f9f2-162">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben sind, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="4f9f2-163">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="4f9f2-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="4f9f2-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Lastenausgleichskonfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="4f9f2-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="4f9f2-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="4f9f2-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4f9f2-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="4f9f2-168">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die der Clouddienst verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="4f9f2-169">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f9f2-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="4f9f2-170">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f9f2-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="4f9f2-171">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="4f9f2-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="4f9f2-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="4f9f2-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="4f9f2-173">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f9f2-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="4f9f2-174">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="4f9f2-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt den Satz von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="4f9f2-176">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f9f2-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="4f9f2-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="4f9f2-178">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="4f9f2-179">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="4f9f2-180">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="4f9f2-181">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="4f9f2-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="4f9f2-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="4f9f2-184">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="4f9f2-185">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="4f9f2-186">`[SkuName <String>]`: Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="4f9f2-187">HINWEIS: Wenn die neue SKU auf der Derzeit im Clouddienst verwendeten Hardware nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten SKU zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="4f9f2-188">`[SkuTier <String>]`: Gibt die Stufe des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="4f9f2-189">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="4f9f2-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="4f9f2-190">**Standard**</span><span class="sxs-lookup"><span data-stu-id="4f9f2-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="4f9f2-191">**Standard**</span><span class="sxs-lookup"><span data-stu-id="4f9f2-191">**Basic**</span></span>
  - <span data-ttu-id="4f9f2-192">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst sofort nach seiner Erstellen gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="4f9f2-193">Der Standardwert ist `true` " .</span><span class="sxs-lookup"><span data-stu-id="4f9f2-193">The default value is `true`.</span></span>         <span data-ttu-id="4f9f2-194">Wenn "false", wird das Dienstmodell noch bereitgestellt, aber der Code wird nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="4f9f2-195">Stattdessen wird der Dienst bis zum Startaufruf "PoweredOff" verwendet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="4f9f2-196">Bei einem bereitgestellten Dienst fallen weiterhin Kosten an, auch wenn er nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="4f9f2-197">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="4f9f2-198">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4f9f2-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="4f9f2-200">Rolleninstanzen werden Domänen zugeordnet, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="4f9f2-201">Updates können manuell in jeder Updatedomäne oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="4f9f2-202">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="4f9f2-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="4f9f2-203">**Auto**</span><span class="sxs-lookup"><span data-stu-id="4f9f2-203">**Auto**</span></span><br /><br /><span data-ttu-id="4f9f2-204">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="4f9f2-204">**Manual**</span></span> <br /><br /><span data-ttu-id="4f9f2-205">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="4f9f2-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="4f9f2-206">Wenn keine Angabe ausgeführt wird, ist der Standardwert "Auto". Wenn dies auf "Manuell" festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="4f9f2-207">Wenn dies auf "Automatisch" festgelegt ist, wird das Update automatisch auf jede Updatedomäne der Reihe nach angewendet.</span><span class="sxs-lookup"><span data-stu-id="4f9f2-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="4f9f2-208">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f9f2-208">RELATED LINKS</span></span>

