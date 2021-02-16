---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162345"
---
# <span data-ttu-id="07a67-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="07a67-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="07a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a67-102">SYNOPSIS</span></span>
<span data-ttu-id="07a67-103">Tauscht VIPs zwischen zwei Lastensaldoern für den Clouddienst (erweiterte Unterstützung).</span><span class="sxs-lookup"><span data-stu-id="07a67-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="07a67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07a67-104">SYNTAX</span></span>

### <span data-ttu-id="07a67-105">CloudServiceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="07a67-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07a67-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="07a67-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07a67-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a67-107">DESCRIPTION</span></span>
<span data-ttu-id="07a67-108">Tauscht VIPs zwischen zwei Lastensaldoern für den Clouddienst (erweiterte Unterstützung).</span><span class="sxs-lookup"><span data-stu-id="07a67-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="07a67-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07a67-109">EXAMPLES</span></span>

### <span data-ttu-id="07a67-110">Beispiel 1: Wechseln des Clouddiensts mithilfe des Namens</span><span class="sxs-lookup"><span data-stu-id="07a67-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="07a67-111">Der obige Befehl ruft den vipswap-Vorgang im Clouddienst mit dem Namen "BService" auf und führt den Vorgang aus, sobald der Benutzer die Aktion in der Bestätigungsaufforderung bestätigt hat.</span><span class="sxs-lookup"><span data-stu-id="07a67-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="07a67-112">"BService" mit dem tauschbaren Clouddienst ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="07a67-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="07a67-113">Beispiel 2: Wechseln des Clouddiensts mithilfe des Clouddienstobjekts</span><span class="sxs-lookup"><span data-stu-id="07a67-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="07a67-114">Der obige Befehl ruft den vipswap-Vorgang im Clouddienst mit dem Namen "BService" auf und führt den Vorgang aus, sobald der Benutzer die Aktion in der Bestätigungsaufforderung bestätigt hat.</span><span class="sxs-lookup"><span data-stu-id="07a67-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="07a67-115">"BService" mit dem tauschbaren Clouddienst ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="07a67-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="07a67-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07a67-116">PARAMETERS</span></span>

### <span data-ttu-id="07a67-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07a67-117">-AsJob</span></span>
<span data-ttu-id="07a67-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="07a67-118">Run the command as a job</span></span>

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

### <span data-ttu-id="07a67-119">-Async</span><span class="sxs-lookup"><span data-stu-id="07a67-119">-Async</span></span>


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

### <span data-ttu-id="07a67-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="07a67-120">-CloudService</span></span>
<span data-ttu-id="07a67-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="07a67-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="07a67-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="07a67-122">-CloudServiceName</span></span>


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

### <span data-ttu-id="07a67-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a67-123">-DefaultProfile</span></span>
<span data-ttu-id="07a67-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07a67-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a67-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="07a67-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07a67-126">-SubscriptionId</span></span>
<span data-ttu-id="07a67-127">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="07a67-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="07a67-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="07a67-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07a67-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07a67-129">-Confirm</span></span>
<span data-ttu-id="07a67-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07a67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a67-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07a67-131">-WhatIf</span></span>
<span data-ttu-id="07a67-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a67-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07a67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a67-134">CommonParameters</span></span>
<span data-ttu-id="07a67-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a67-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07a67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a67-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07a67-137">INPUTS</span></span>

## <span data-ttu-id="07a67-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07a67-138">OUTPUTS</span></span>

### <span data-ttu-id="07a67-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07a67-139">System.Boolean</span></span>

## <span data-ttu-id="07a67-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07a67-140">NOTES</span></span>

<span data-ttu-id="07a67-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="07a67-141">ALIASES</span></span>

<span data-ttu-id="07a67-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="07a67-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07a67-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07a67-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07a67-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07a67-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07a67-145">CLOUDSERVICE <CloudService> :</span><span class="sxs-lookup"><span data-stu-id="07a67-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="07a67-146">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="07a67-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="07a67-147">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="07a67-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="07a67-148">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="07a67-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="07a67-149">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="07a67-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="07a67-150">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="07a67-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="07a67-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="07a67-152">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="07a67-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform automatisch ein Upgrade von "typeHandlerVersion" auf höhere Nebenversionen durchführen kann, sobald diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="07a67-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="07a67-154">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="07a67-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="07a67-155">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="07a67-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="07a67-156">Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="07a67-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="07a67-157">Wenn weder forceUpdateTag noch irgendeine der öffentlichen oder geschützten Einstellungen geändert wird, würde die Erweiterung zu der Rolleninstanz mit derselben Sequenznummer fließen, und es ist aufgabe der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="07a67-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="07a67-158">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="07a67-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="07a67-159">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="07a67-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="07a67-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07a67-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="07a67-161">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="07a67-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="07a67-162">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="07a67-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="07a67-163">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="07a67-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="07a67-164">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="07a67-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="07a67-165">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="07a67-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="07a67-166">Bei einer XML-Erweiterung (wie RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="07a67-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="07a67-167">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="07a67-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07a67-168">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="07a67-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="07a67-169">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="07a67-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="07a67-170">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="07a67-170">Specifies the version of the extension.</span></span> <span data-ttu-id="07a67-171">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="07a67-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="07a67-172">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="07a67-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="07a67-173">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben sind, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="07a67-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="07a67-174">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07a67-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="07a67-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="07a67-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Lastenausgleichskonfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="07a67-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="07a67-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="07a67-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="07a67-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="07a67-179">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die der Clouddienst verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="07a67-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="07a67-180">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="07a67-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="07a67-181">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="07a67-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07a67-182">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="07a67-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="07a67-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="07a67-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="07a67-184">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="07a67-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="07a67-185">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="07a67-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt den Satz von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07a67-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="07a67-187">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="07a67-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="07a67-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="07a67-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="07a67-189">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="07a67-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="07a67-190">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob Service bezieht.</span><span class="sxs-lookup"><span data-stu-id="07a67-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="07a67-191">Bei der Dienstpaket-URL kann es sich um einen SAS-URI (Shared Access Signature) eines beliebigen Speicherkontos sein.</span><span class="sxs-lookup"><span data-stu-id="07a67-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="07a67-192">Dies ist eine schreib ausschließliche Eigenschaft, die nicht in GET-Aufrufen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="07a67-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="07a67-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="07a67-195">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="07a67-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="07a67-196">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="07a67-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="07a67-197">`[SkuName <String>]`: Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="07a67-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="07a67-198">HINWEIS: Wenn die neue SKU auf der Derzeit im Clouddienst verwendeten Hardware nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten SKU zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="07a67-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="07a67-199">`[SkuTier <String>]`: Gibt die Stufe des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="07a67-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="07a67-200">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="07a67-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="07a67-201">**Standard**</span><span class="sxs-lookup"><span data-stu-id="07a67-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="07a67-202">**Standard**</span><span class="sxs-lookup"><span data-stu-id="07a67-202">**Basic**</span></span>
  - <span data-ttu-id="07a67-203">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst sofort nach seiner Erstellen gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a67-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="07a67-204">Der Standardwert ist `true` " .</span><span class="sxs-lookup"><span data-stu-id="07a67-204">The default value is `true`.</span></span>         <span data-ttu-id="07a67-205">Wenn "false", wird das Dienstmodell noch bereitgestellt, aber der Code wird nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07a67-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="07a67-206">Stattdessen wird der Dienst bis zum Startaufruf "PoweredOff" verwendet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="07a67-207">Bei einem bereitgestellten Dienst fallen weiterhin Kosten an, auch wenn er nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="07a67-208">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="07a67-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="07a67-209">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="07a67-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="07a67-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="07a67-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="07a67-211">Rolleninstanzen werden Domänen zugeordnet, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="07a67-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="07a67-212">Updates können manuell in jeder Updatedomäne oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="07a67-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="07a67-213">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="07a67-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="07a67-214">**Auto**</span><span class="sxs-lookup"><span data-stu-id="07a67-214">**Auto**</span></span><br /><br /><span data-ttu-id="07a67-215">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="07a67-215">**Manual**</span></span> <br /><br /><span data-ttu-id="07a67-216">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="07a67-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="07a67-217">Wenn keine Angabe ausgeführt wird, ist der Standardwert "Auto". Wenn dies auf "Manuell" festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="07a67-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="07a67-218">Wenn dies auf "Automatisch" festgelegt ist, wird das Update automatisch auf jede Updatedomäne der Reihe nach angewendet.</span><span class="sxs-lookup"><span data-stu-id="07a67-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="07a67-219">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07a67-219">RELATED LINKS</span></span>

