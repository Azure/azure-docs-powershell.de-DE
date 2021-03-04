---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: d875ad9af0ebe864f9d396fed44961a5d48f38c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930587"
---
# <span data-ttu-id="b909f-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b909f-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="b909f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b909f-102">SYNOPSIS</span></span>
<span data-ttu-id="b909f-103">Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="b909f-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="b909f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b909f-104">SYNTAX</span></span>

### <span data-ttu-id="b909f-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b909f-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="b909f-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="b909f-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="b909f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b909f-107">DESCRIPTION</span></span>
<span data-ttu-id="b909f-108">Holen Sie sich die öffentliche IP-Adresse eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="b909f-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="b909f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b909f-109">EXAMPLES</span></span>

### <span data-ttu-id="b909f-110">Beispiel 1: Öffentliche IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen erhalten.</span><span class="sxs-lookup"><span data-stu-id="b909f-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="b909f-111">Ruft die öffentlichen IP-Adressen auf Instanzebene für einen bestimmten Clouddienstnamen ab.</span><span class="sxs-lookup"><span data-stu-id="b909f-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="b909f-112">Beispiel 2: Öffentliche IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="b909f-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="b909f-113">Ruft die öffentlichen IP-Adressen auf Instanzebene für ein bestimmtes Clouddienstobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="b909f-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="b909f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b909f-114">PARAMETERS</span></span>

### <span data-ttu-id="b909f-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="b909f-115">-CloudService</span></span>
<span data-ttu-id="b909f-116">CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b909f-116">CloudService instance.</span></span>
<span data-ttu-id="b909f-117">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu CLOUDSERVICE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b909f-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b909f-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b909f-118">-CloudServiceName</span></span>
<span data-ttu-id="b909f-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="b909f-119">CloudServiceName.</span></span>

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

### <span data-ttu-id="b909f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b909f-120">-ResourceGroupName</span></span>
<span data-ttu-id="b909f-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="b909f-121">ResourceGroupName.</span></span>

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

### <span data-ttu-id="b909f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b909f-122">-SubscriptionId</span></span>
<span data-ttu-id="b909f-123">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b909f-123">Subscription.</span></span>

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

### <span data-ttu-id="b909f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b909f-124">CommonParameters</span></span>
<span data-ttu-id="b909f-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b909f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b909f-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b909f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b909f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b909f-127">INPUTS</span></span>

## <span data-ttu-id="b909f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b909f-128">OUTPUTS</span></span>

## <span data-ttu-id="b909f-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b909f-129">NOTES</span></span>

<span data-ttu-id="b909f-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b909f-130">ALIASES</span></span>

<span data-ttu-id="b909f-131">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b909f-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b909f-132">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b909f-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b909f-133">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b909f-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b909f-134"><CloudService>CLOUDSERVICE: CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b909f-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="b909f-135">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="b909f-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="b909f-136">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="b909f-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="b909f-137">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="b909f-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="b909f-138">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="b909f-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="b909f-139">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b909f-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="b909f-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="b909f-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="b909f-141">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="b909f-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="b909f-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="b909f-143">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="b909f-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="b909f-144">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b909f-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="b909f-145">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="b909f-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="b909f-146">Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b909f-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="b909f-147">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b909f-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="b909f-148">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b909f-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="b909f-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b909f-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="b909f-150">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="b909f-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="b909f-151">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b909f-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="b909f-152">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="b909f-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="b909f-153">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b909f-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="b909f-154">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b909f-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="b909f-155">Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b909f-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="b909f-156">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b909f-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b909f-157">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b909f-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="b909f-158">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b909f-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="b909f-159">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b909f-159">Specifies the version of the extension.</span></span> <span data-ttu-id="b909f-160">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b909f-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="b909f-161">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b909f-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="b909f-162">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b909f-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="b909f-163">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b909f-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="b909f-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="b909f-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="b909f-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="b909f-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="b909f-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b909f-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="b909f-168">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b909f-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="b909f-169">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b909f-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="b909f-170">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b909f-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b909f-171">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b909f-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="b909f-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="b909f-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="b909f-173">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b909f-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="b909f-174">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="b909f-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b909f-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="b909f-176">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b909f-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b909f-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="b909f-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="b909f-178">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b909f-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="b909f-179">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="b909f-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="b909f-180">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="b909f-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="b909f-181">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b909f-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="b909f-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="b909f-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="b909f-184">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b909f-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="b909f-185">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="b909f-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="b909f-186">`[SkuName <String>]`: Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="b909f-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="b909f-187">HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="b909f-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="b909f-188">`[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="b909f-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="b909f-189">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="b909f-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="b909f-190">**Standard**</span><span class="sxs-lookup"><span data-stu-id="b909f-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="b909f-191">**Basic**</span><span class="sxs-lookup"><span data-stu-id="b909f-191">**Basic**</span></span>
  - <span data-ttu-id="b909f-192">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b909f-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="b909f-193">Der Standardwert ist `true` .</span><span class="sxs-lookup"><span data-stu-id="b909f-193">The default value is `true`.</span></span>         <span data-ttu-id="b909f-194">Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b909f-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="b909f-195">Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b909f-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="b909f-196">Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="b909f-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="b909f-197">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="b909f-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b909f-198">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b909f-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b909f-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="b909f-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="b909f-200">Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b909f-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="b909f-201">Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="b909f-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="b909f-202">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="b909f-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="b909f-203">**Auto**</span><span class="sxs-lookup"><span data-stu-id="b909f-203">**Auto**</span></span><br /><br /><span data-ttu-id="b909f-204">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="b909f-204">**Manual**</span></span> <br /><br /><span data-ttu-id="b909f-205">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="b909f-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="b909f-206">Wenn nicht angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b909f-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="b909f-207">Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="b909f-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="b909f-208">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b909f-208">RELATED LINKS</span></span>

