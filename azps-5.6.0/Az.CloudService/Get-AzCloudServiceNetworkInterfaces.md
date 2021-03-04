---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: ae6bb602e90fd86334a28a804deed2be429347ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946667"
---
# <span data-ttu-id="042fa-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="042fa-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="042fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="042fa-102">SYNOPSIS</span></span>
<span data-ttu-id="042fa-103">Holen Sie sich die Netzwerkschnittstellen eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="042fa-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="042fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="042fa-104">SYNTAX</span></span>

### <span data-ttu-id="042fa-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="042fa-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="042fa-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="042fa-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="042fa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="042fa-107">DESCRIPTION</span></span>
<span data-ttu-id="042fa-108">Holen Sie sich die Netzwerkschnittstellen eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="042fa-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="042fa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="042fa-109">EXAMPLES</span></span>

### <span data-ttu-id="042fa-110">Beispiel 1: Erhalten von Netzwerkschnittstellen unter einem Clouddienstnamen</span><span class="sxs-lookup"><span data-stu-id="042fa-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="042fa-111">Ruft alle Netzwerkschnittstellen für einen bestimmten Clouddienstnamen ab.</span><span class="sxs-lookup"><span data-stu-id="042fa-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="042fa-112">Beispiel 2: Erhalten von Netzwerkschnittstellen durch ein Clouddienstobjekt</span><span class="sxs-lookup"><span data-stu-id="042fa-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="042fa-113">Ruft alle Netzwerkschnittstellen für ein bestimmtes Clouddienstobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="042fa-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="042fa-114">Beispiel 3: Holen Sie sich Netzwerkschnittstellen über ein Clouddienstobjekt und den Namen der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="042fa-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="042fa-115">Ruft alle Netzwerkschnittstellen für ein bestimmtes Clouddienstobjekt und den Namen der Rolleninstanz ab.</span><span class="sxs-lookup"><span data-stu-id="042fa-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="042fa-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="042fa-116">PARAMETERS</span></span>

### <span data-ttu-id="042fa-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="042fa-117">-CloudService</span></span>
<span data-ttu-id="042fa-118">CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="042fa-118">CloudService instance.</span></span>
<span data-ttu-id="042fa-119">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu CLOUDSERVICE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="042fa-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="042fa-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="042fa-120">-CloudServiceName</span></span>
<span data-ttu-id="042fa-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="042fa-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="042fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="042fa-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="042fa-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="042fa-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="042fa-124">-RoleInstanceName</span></span>
<span data-ttu-id="042fa-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="042fa-125">RoleInstanceName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042fa-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="042fa-126">-SubscriptionId</span></span>
<span data-ttu-id="042fa-127">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="042fa-127">Subscription.</span></span>

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

### <span data-ttu-id="042fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042fa-128">CommonParameters</span></span>
<span data-ttu-id="042fa-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042fa-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="042fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042fa-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="042fa-131">INPUTS</span></span>

## <span data-ttu-id="042fa-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="042fa-132">OUTPUTS</span></span>

## <span data-ttu-id="042fa-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="042fa-133">NOTES</span></span>

<span data-ttu-id="042fa-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="042fa-134">ALIASES</span></span>

<span data-ttu-id="042fa-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="042fa-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="042fa-136">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="042fa-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="042fa-137">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="042fa-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="042fa-138"><CloudService>CLOUDSERVICE: CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="042fa-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="042fa-139">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="042fa-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="042fa-140">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="042fa-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="042fa-141">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="042fa-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="042fa-142">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="042fa-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="042fa-143">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="042fa-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="042fa-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="042fa-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="042fa-145">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="042fa-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="042fa-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="042fa-147">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="042fa-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="042fa-148">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="042fa-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="042fa-149">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="042fa-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="042fa-150">Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="042fa-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="042fa-151">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="042fa-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="042fa-152">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="042fa-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="042fa-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="042fa-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="042fa-154">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="042fa-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="042fa-155">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="042fa-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="042fa-156">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="042fa-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="042fa-157">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="042fa-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="042fa-158">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="042fa-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="042fa-159">Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="042fa-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="042fa-160">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="042fa-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="042fa-161">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="042fa-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="042fa-162">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="042fa-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="042fa-163">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="042fa-163">Specifies the version of the extension.</span></span> <span data-ttu-id="042fa-164">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="042fa-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="042fa-165">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="042fa-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="042fa-166">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="042fa-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="042fa-167">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="042fa-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="042fa-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="042fa-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="042fa-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="042fa-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="042fa-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="042fa-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="042fa-172">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="042fa-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="042fa-173">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="042fa-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="042fa-174">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="042fa-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="042fa-175">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="042fa-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="042fa-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="042fa-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="042fa-177">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="042fa-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="042fa-178">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="042fa-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="042fa-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="042fa-180">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="042fa-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="042fa-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="042fa-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="042fa-182">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="042fa-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="042fa-183">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="042fa-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="042fa-184">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="042fa-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="042fa-185">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="042fa-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="042fa-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="042fa-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="042fa-188">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="042fa-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="042fa-189">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="042fa-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="042fa-190">`[SkuName <String>]`: Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="042fa-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="042fa-191">HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="042fa-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="042fa-192">`[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="042fa-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="042fa-193">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="042fa-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="042fa-194">**Standard**</span><span class="sxs-lookup"><span data-stu-id="042fa-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="042fa-195">**Basic**</span><span class="sxs-lookup"><span data-stu-id="042fa-195">**Basic**</span></span>
  - <span data-ttu-id="042fa-196">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="042fa-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="042fa-197">Der Standardwert ist `true` .</span><span class="sxs-lookup"><span data-stu-id="042fa-197">The default value is `true`.</span></span>         <span data-ttu-id="042fa-198">Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="042fa-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="042fa-199">Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="042fa-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="042fa-200">Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="042fa-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="042fa-201">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="042fa-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="042fa-202">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="042fa-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="042fa-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="042fa-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="042fa-204">Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="042fa-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="042fa-205">Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="042fa-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="042fa-206">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="042fa-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="042fa-207">**Auto**</span><span class="sxs-lookup"><span data-stu-id="042fa-207">**Auto**</span></span><br /><br /><span data-ttu-id="042fa-208">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="042fa-208">**Manual**</span></span> <br /><br /><span data-ttu-id="042fa-209">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="042fa-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="042fa-210">Wenn nicht angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="042fa-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="042fa-211">Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="042fa-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="042fa-212">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="042fa-212">RELATED LINKS</span></span>

