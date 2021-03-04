---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946289"
---
# <span data-ttu-id="c8961-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="c8961-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="c8961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8961-102">SYNOPSIS</span></span>
<span data-ttu-id="c8961-103">Tauscht VIPs zwischen zwei Load Balancern des Clouddiensts (erweiterter Support).</span><span class="sxs-lookup"><span data-stu-id="c8961-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="c8961-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8961-104">SYNTAX</span></span>

### <span data-ttu-id="c8961-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8961-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8961-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="c8961-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8961-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8961-107">DESCRIPTION</span></span>
<span data-ttu-id="c8961-108">Tauscht VIPs zwischen zwei Load Balancern des Clouddiensts (erweiterter Support).</span><span class="sxs-lookup"><span data-stu-id="c8961-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="c8961-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8961-109">EXAMPLES</span></span>

### <span data-ttu-id="c8961-110">Beispiel 1: Wechseln des Clouddiensts mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="c8961-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="c8961-111">Der Befehl oben ruft den vipswap-Vorgang im Clouddienst mit dem Namen "BService" auf und führt den Vorgang aus, sobald der Benutzer die Aktion in der Bestätigungsaufforderung bestätigt.</span><span class="sxs-lookup"><span data-stu-id="c8961-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="c8961-112">"BService" mit mit seinem swappablen Clouddienst getauscht werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="c8961-113">Beispiel 2: Wechseln des Clouddiensts mithilfe des Clouddienstobjekts</span><span class="sxs-lookup"><span data-stu-id="c8961-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="c8961-114">Der Befehl oben ruft den vipswap-Vorgang im Clouddienst mit dem Namen "BService" auf und führt den Vorgang aus, sobald der Benutzer die Aktion in der Bestätigungsaufforderung bestätigt.</span><span class="sxs-lookup"><span data-stu-id="c8961-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="c8961-115">"BService" mit mit seinem swappablen Clouddienst getauscht werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="c8961-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8961-116">PARAMETERS</span></span>

### <span data-ttu-id="c8961-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8961-117">-AsJob</span></span>
<span data-ttu-id="c8961-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c8961-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c8961-119">-Async</span><span class="sxs-lookup"><span data-stu-id="c8961-119">-Async</span></span>


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

### <span data-ttu-id="c8961-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="c8961-120">-CloudService</span></span>
<span data-ttu-id="c8961-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu CLOUDSERVICE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c8961-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8961-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c8961-122">-CloudServiceName</span></span>


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

### <span data-ttu-id="c8961-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8961-123">-DefaultProfile</span></span>
<span data-ttu-id="c8961-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8961-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8961-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="c8961-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8961-126">-SubscriptionId</span></span>
<span data-ttu-id="c8961-127">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c8961-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c8961-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c8961-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c8961-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8961-129">-Confirm</span></span>
<span data-ttu-id="c8961-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8961-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8961-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8961-131">-WhatIf</span></span>
<span data-ttu-id="c8961-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8961-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8961-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8961-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8961-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8961-134">CommonParameters</span></span>
<span data-ttu-id="c8961-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8961-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8961-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8961-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8961-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8961-137">INPUTS</span></span>

## <span data-ttu-id="c8961-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8961-138">OUTPUTS</span></span>

### <span data-ttu-id="c8961-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8961-139">System.Boolean</span></span>

## <span data-ttu-id="c8961-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c8961-140">NOTES</span></span>

<span data-ttu-id="c8961-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c8961-141">ALIASES</span></span>

<span data-ttu-id="c8961-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c8961-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8961-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c8961-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8961-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8961-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8961-145">CLOUDSERVICE <CloudService> :</span><span class="sxs-lookup"><span data-stu-id="c8961-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="c8961-146">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="c8961-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="c8961-147">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="c8961-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="c8961-148">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="c8961-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="c8961-149">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="c8961-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="c8961-150">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8961-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="c8961-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="c8961-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="c8961-152">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="c8961-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="c8961-154">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c8961-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="c8961-155">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c8961-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="c8961-156">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8961-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="c8961-157">Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c8961-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="c8961-158">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8961-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="c8961-159">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="c8961-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c8961-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="c8961-161">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="c8961-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="c8961-162">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8961-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="c8961-163">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8961-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="c8961-164">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8961-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="c8961-165">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8961-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="c8961-166">Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c8961-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="c8961-167">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c8961-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="c8961-168">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c8961-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="c8961-169">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c8961-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="c8961-170">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c8961-170">Specifies the version of the extension.</span></span> <span data-ttu-id="c8961-171">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8961-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="c8961-172">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c8961-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="c8961-173">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c8961-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="c8961-174">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8961-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="c8961-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="c8961-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="c8961-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="c8961-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="c8961-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c8961-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="c8961-179">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c8961-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="c8961-180">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c8961-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="c8961-181">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c8961-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="c8961-182">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c8961-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="c8961-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="c8961-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="c8961-184">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c8961-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="c8961-185">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="c8961-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8961-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="c8961-187">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c8961-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="c8961-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8961-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="c8961-189">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c8961-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="c8961-190">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="c8961-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="c8961-191">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="c8961-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="c8961-192">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8961-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="c8961-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="c8961-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="c8961-195">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c8961-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="c8961-196">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="c8961-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="c8961-197">`[SkuName <String>]`: Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="c8961-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="c8961-198">HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="c8961-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="c8961-199">`[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="c8961-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="c8961-200">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="c8961-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="c8961-201">**Standard**</span><span class="sxs-lookup"><span data-stu-id="c8961-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="c8961-202">**Basic**</span><span class="sxs-lookup"><span data-stu-id="c8961-202">**Basic**</span></span>
  - <span data-ttu-id="c8961-203">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8961-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="c8961-204">Der Standardwert ist `true` .</span><span class="sxs-lookup"><span data-stu-id="c8961-204">The default value is `true`.</span></span>         <span data-ttu-id="c8961-205">Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8961-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="c8961-206">Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c8961-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="c8961-207">Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="c8961-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="c8961-208">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="c8961-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c8961-209">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c8961-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c8961-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="c8961-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="c8961-211">Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c8961-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="c8961-212">Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8961-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="c8961-213">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="c8961-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="c8961-214">**Auto**</span><span class="sxs-lookup"><span data-stu-id="c8961-214">**Auto**</span></span><br /><br /><span data-ttu-id="c8961-215">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="c8961-215">**Manual**</span></span> <br /><br /><span data-ttu-id="c8961-216">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="c8961-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="c8961-217">Wenn nicht angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c8961-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="c8961-218">Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8961-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="c8961-219">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c8961-219">RELATED LINKS</span></span>

