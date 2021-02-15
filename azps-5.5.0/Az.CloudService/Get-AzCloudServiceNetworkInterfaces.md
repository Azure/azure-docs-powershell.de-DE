---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: 7f8a51c518bd034e51d8c25d5029bb57b3e38caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164220"
---
# <span data-ttu-id="873d9-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="873d9-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="873d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="873d9-102">SYNOPSIS</span></span>
<span data-ttu-id="873d9-103">Holen Sie sich die Netzwerkschnittstellen eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="873d9-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="873d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="873d9-104">SYNTAX</span></span>

### <span data-ttu-id="873d9-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="873d9-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="873d9-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="873d9-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="873d9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="873d9-107">DESCRIPTION</span></span>
<span data-ttu-id="873d9-108">Holen Sie sich die Netzwerkschnittstellen eines Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="873d9-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="873d9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="873d9-109">EXAMPLES</span></span>

### <span data-ttu-id="873d9-110">Beispiel 1: Erhalten von Netzwerkschnittstellen unter einem Clouddienstnamen</span><span class="sxs-lookup"><span data-stu-id="873d9-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="873d9-111">Ruft alle Netzwerkschnittstellen für einen bestimmten Clouddienstnamen ab.</span><span class="sxs-lookup"><span data-stu-id="873d9-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="873d9-112">Beispiel 2: Erhalten von Netzwerkschnittstellen durch ein Clouddienstobjekt</span><span class="sxs-lookup"><span data-stu-id="873d9-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="873d9-113">Ruft alle Netzwerkschnittstellen für ein bestimmtes Clouddienstobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="873d9-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="873d9-114">Beispiel 3: Erhalten von Netzwerkschnittstellen durch ein Clouddienstobjekt und den Namen der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="873d9-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="873d9-115">Ruft alle Netzwerkschnittstellen für ein bestimmtes Clouddienstobjekt und den Namen der Rolleninstanz ab.</span><span class="sxs-lookup"><span data-stu-id="873d9-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="873d9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="873d9-116">PARAMETERS</span></span>

### <span data-ttu-id="873d9-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="873d9-117">-CloudService</span></span>
<span data-ttu-id="873d9-118">CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="873d9-118">CloudService instance.</span></span>
<span data-ttu-id="873d9-119">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="873d9-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="873d9-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="873d9-120">-CloudServiceName</span></span>
<span data-ttu-id="873d9-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="873d9-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="873d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="873d9-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="873d9-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="873d9-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="873d9-124">-RoleInstanceName</span></span>
<span data-ttu-id="873d9-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="873d9-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="873d9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="873d9-126">-SubscriptionId</span></span>
<span data-ttu-id="873d9-127">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="873d9-127">Subscription.</span></span>

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

### <span data-ttu-id="873d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873d9-128">CommonParameters</span></span>
<span data-ttu-id="873d9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873d9-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="873d9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873d9-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="873d9-131">INPUTS</span></span>

## <span data-ttu-id="873d9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="873d9-132">OUTPUTS</span></span>

## <span data-ttu-id="873d9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="873d9-133">NOTES</span></span>

<span data-ttu-id="873d9-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="873d9-134">ALIASES</span></span>

<span data-ttu-id="873d9-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="873d9-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="873d9-136">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="873d9-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="873d9-137">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="873d9-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="873d9-138"><CloudService>CLOUDSERVICE: CloudService-Instanz.</span><span class="sxs-lookup"><span data-stu-id="873d9-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="873d9-139">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="873d9-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="873d9-140">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="873d9-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="873d9-141">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="873d9-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="873d9-142">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="873d9-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="873d9-143">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="873d9-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="873d9-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="873d9-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="873d9-145">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="873d9-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform automatisch ein Upgrade von "typeHandlerVersion" auf höhere Nebenversionen durchführen kann, sobald diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="873d9-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="873d9-147">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="873d9-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="873d9-148">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="873d9-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="873d9-149">Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="873d9-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="873d9-150">Wenn weder forceUpdateTag noch irgendeine der öffentlichen oder geschützten Einstellungen geändert wird, würde die Erweiterung zu der Rolleninstanz mit derselben Sequenznummer fließen, und es ist aufgabe der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="873d9-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="873d9-151">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="873d9-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="873d9-152">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="873d9-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="873d9-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="873d9-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="873d9-154">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="873d9-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="873d9-155">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="873d9-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="873d9-156">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="873d9-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="873d9-157">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="873d9-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="873d9-158">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="873d9-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="873d9-159">Bei einer XML-Erweiterung (wie RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="873d9-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="873d9-160">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="873d9-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="873d9-161">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="873d9-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="873d9-162">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="873d9-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="873d9-163">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="873d9-163">Specifies the version of the extension.</span></span> <span data-ttu-id="873d9-164">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="873d9-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="873d9-165">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="873d9-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="873d9-166">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben sind, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="873d9-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="873d9-167">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="873d9-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="873d9-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="873d9-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Lastenausgleichskonfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="873d9-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="873d9-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="873d9-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="873d9-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="873d9-172">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die der Clouddienst verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="873d9-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="873d9-173">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="873d9-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="873d9-174">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="873d9-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="873d9-175">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="873d9-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="873d9-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="873d9-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="873d9-177">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="873d9-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="873d9-178">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="873d9-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt den Satz von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="873d9-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="873d9-180">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="873d9-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="873d9-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="873d9-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="873d9-182">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="873d9-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="873d9-183">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="873d9-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="873d9-184">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="873d9-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="873d9-185">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="873d9-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="873d9-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="873d9-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="873d9-188">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="873d9-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="873d9-189">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="873d9-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="873d9-190">`[SkuName <String>]`: Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="873d9-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="873d9-191">HINWEIS: Wenn die neue SKU auf der Derzeit im Clouddienst verwendeten Hardware nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten SKU zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="873d9-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="873d9-192">`[SkuTier <String>]`: Gibt die Stufe des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="873d9-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="873d9-193">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="873d9-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="873d9-194">**Standard**</span><span class="sxs-lookup"><span data-stu-id="873d9-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="873d9-195">**Standard**</span><span class="sxs-lookup"><span data-stu-id="873d9-195">**Basic**</span></span>
  - <span data-ttu-id="873d9-196">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst sofort nach seiner Erstellen gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="873d9-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="873d9-197">Der Standardwert ist `true` " .</span><span class="sxs-lookup"><span data-stu-id="873d9-197">The default value is `true`.</span></span>         <span data-ttu-id="873d9-198">Wenn "false", wird das Dienstmodell noch bereitgestellt, aber der Code wird nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="873d9-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="873d9-199">Stattdessen wird der Dienst bis zum Startaufruf "PoweredOff" verwendet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="873d9-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="873d9-200">Bei einem bereitgestellten Dienst fallen weiterhin Kosten an, auch wenn er nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="873d9-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="873d9-201">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="873d9-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="873d9-202">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="873d9-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="873d9-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="873d9-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="873d9-204">Rolleninstanzen werden Domänen zugeordnet, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="873d9-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="873d9-205">Updates können manuell in jeder Updatedomäne oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="873d9-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="873d9-206">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="873d9-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="873d9-207">**Auto**</span><span class="sxs-lookup"><span data-stu-id="873d9-207">**Auto**</span></span><br /><br /><span data-ttu-id="873d9-208">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="873d9-208">**Manual**</span></span> <br /><br /><span data-ttu-id="873d9-209">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="873d9-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="873d9-210">Wenn keine Angabe ausgeführt wird, ist der Standardwert "Auto". Wenn dies auf "Manuell" festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="873d9-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="873d9-211">Wenn dies auf "Automatisch" festgelegt ist, wird das Update automatisch auf jede Updatedomäne der Reihe nach angewendet.</span><span class="sxs-lookup"><span data-stu-id="873d9-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="873d9-212">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="873d9-212">RELATED LINKS</span></span>

