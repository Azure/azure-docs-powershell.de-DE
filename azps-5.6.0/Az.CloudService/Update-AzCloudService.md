---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946277"
---
# <span data-ttu-id="dd0ad-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="dd0ad-101">Update-AzCloudService</span></span>

## <span data-ttu-id="dd0ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0ad-103">Erstellen oder Aktualisieren eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="dd0ad-103">Create or update a cloud service.</span></span>
<span data-ttu-id="dd0ad-104">Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="dd0ad-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd0ad-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd0ad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd0ad-106">DESCRIPTION</span></span>
<span data-ttu-id="dd0ad-107">Erstellen oder Aktualisieren eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="dd0ad-107">Create or update a cloud service.</span></span>
<span data-ttu-id="dd0ad-108">Beachten Sie, dass einige Eigenschaften nur während der Erstellung des Clouddiensts festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="dd0ad-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd0ad-109">EXAMPLES</span></span>

### <span data-ttu-id="dd0ad-110">Beispiel 1: Hinzufügen einer RDP-Erweiterung zu einem vorhandenen Clouddienst</span><span class="sxs-lookup"><span data-stu-id="dd0ad-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="dd0ad-111">Über dem Befehlssatz wird dem bereits vorhandenen Clouddienst ContosoCS, der zur Ressourcengruppe "ContosOrg" gehört, eine RDP-Erweiterung addiert.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="dd0ad-112">Beispiel 2: Entfernen aller Erweiterungen aus dem Clouddienst</span><span class="sxs-lookup"><span data-stu-id="dd0ad-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="dd0ad-113">Über dem Befehlssatz werden alle Erweiterungen aus dem vorhandenen Clouddienst contosoCS entfernt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="dd0ad-114">Beispiel 3: Entfernen der RDP-Erweiterung aus dem Clouddienst</span><span class="sxs-lookup"><span data-stu-id="dd0ad-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="dd0ad-115">Über dem Befehlssatz wird die RDP-Erweiterung aus dem vorhandenen Clouddienst ContosoCS entfernt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="dd0ad-116">Beispiel 4: Scale-Out /Scale-In Rolleninstanzen</span><span class="sxs-lookup"><span data-stu-id="dd0ad-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="dd0ad-117">Über einer Reihe von Befehlen wird gezeigt, wie Sie die Anzahl der Skalierungs- und Skalierungsinstanzen für den Clouddienst contosoCS, der zur Ressourcengruppe "ContosOrg" gehört, skalieren.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="dd0ad-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd0ad-118">PARAMETERS</span></span>

### <span data-ttu-id="dd0ad-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd0ad-119">-AsJob</span></span>
<span data-ttu-id="dd0ad-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd0ad-120">Run the command as a job</span></span>

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

### <span data-ttu-id="dd0ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0ad-121">-DefaultProfile</span></span>
<span data-ttu-id="dd0ad-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd0ad-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd0ad-123">-InputObject</span></span>
<span data-ttu-id="dd0ad-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0ad-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd0ad-125">-NoWait</span></span>
<span data-ttu-id="dd0ad-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dd0ad-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd0ad-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="dd0ad-127">-Parameter</span></span>
<span data-ttu-id="dd0ad-128">Beschreibt den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-128">Describes the cloud service.</span></span>
<span data-ttu-id="dd0ad-129">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu PARAMETER-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0ad-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd0ad-130">-Confirm</span></span>
<span data-ttu-id="dd0ad-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd0ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd0ad-132">-WhatIf</span></span>
<span data-ttu-id="dd0ad-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd0ad-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd0ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0ad-135">CommonParameters</span></span>
<span data-ttu-id="dd0ad-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0ad-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd0ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0ad-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd0ad-138">INPUTS</span></span>

### <span data-ttu-id="dd0ad-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="dd0ad-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="dd0ad-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="dd0ad-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="dd0ad-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd0ad-141">OUTPUTS</span></span>

### <span data-ttu-id="dd0ad-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="dd0ad-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="dd0ad-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd0ad-143">NOTES</span></span>

<span data-ttu-id="dd0ad-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dd0ad-144">ALIASES</span></span>

<span data-ttu-id="dd0ad-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dd0ad-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd0ad-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd0ad-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd0ad-148">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="dd0ad-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd0ad-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd0ad-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="dd0ad-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dd0ad-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd0ad-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd0ad-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="dd0ad-152">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="dd0ad-153">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="dd0ad-154">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd0ad-155">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dd0ad-156">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="dd0ad-157">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="dd0ad-158">PARAMETER <ICloudService> : Beschreibt den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="dd0ad-159">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="dd0ad-160">`[Configuration <String>]`: Gibt die XML-Dienstkonfiguration (CSCFG) für den Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="dd0ad-161">`[ConfigurationUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort der Dienstkonfiguration im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="dd0ad-162">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="dd0ad-163">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="dd0ad-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Beschreibt ein Clouddiensterweiterungsprofil.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="dd0ad-165">`[Extension <IExtension[]>]`: Liste der Erweiterungen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="dd0ad-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Geben Sie explizit an, ob die Plattform ein automatisches Upgrade von typeHandlerVersion auf höhere Nebenversionen durchführen kann, wenn sie verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="dd0ad-167">`[ForceUpdateTag <String>]`: Tag, um die Anwendung der bereitgestellten öffentlichen und geschützten Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="dd0ad-168">Wenn Sie den Tagwert ändern, können Sie die Erweiterung erneut ausführen, ohne die öffentlichen oder geschützten Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="dd0ad-169">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="dd0ad-170">Wenn sich weder forceUpdateTag noch eine der öffentlichen oder geschützten Einstellungen ändert, würde die Erweiterung zur Rolleninstanz mit derselben Sequenznummer fließen, und es liegt an der Handlerimplementierung, ob sie erneut ausgeführt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="dd0ad-171">`[Name <String>]`: Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="dd0ad-172">`[ProtectedSetting <String>]`: Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die Rolleninstanz gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="dd0ad-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd0ad-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="dd0ad-174">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="dd0ad-175">`[RolesAppliedTo <String[]>]`: Optionale Liste der Rollen zum Anwenden dieser Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="dd0ad-176">Wenn keine Eigenschaft angegeben oder "\*" angegeben wird, wird die Erweiterung auf alle Rollen im Clouddienst angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="dd0ad-177">`[Setting <String>]`: Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="dd0ad-178">Bei JSON-Erweiterungen sind dies die JSON-Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="dd0ad-179">Für die XML-Erweiterung (z. B. RDP) ist dies die XML-Einstellung für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="dd0ad-180">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd0ad-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="dd0ad-181">`[Type <String>]`: Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="dd0ad-182">`[TypeHandlerVersion <String>]`: Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="dd0ad-183">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-183">Specifies the version of the extension.</span></span> <span data-ttu-id="dd0ad-184">Wenn dieses Element nicht angegeben ist oder ein Sternchen (\*) als Wert verwendet wird, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="dd0ad-185">Wenn der Wert mit einer Hauptversionsnummer und einem Sternchen als Nebenversionsnummer (X.) angegeben ist, wird die neueste Nebenversion der angegebenen Hauptversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="dd0ad-186">Wenn eine Hauptversionsnummer und eine Nebenversionsnummer (X.Y) angegeben werden, wird die spezifische Erweiterungsversion ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="dd0ad-187">Wenn eine Version angegeben wird, wird für die Rolleninstanz ein automatisches Upgrade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="dd0ad-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Netzwerkprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="dd0ad-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: Die Liste der Load Balancer-Konfigurationen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="dd0ad-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Liste der IP</span><span class="sxs-lookup"><span data-stu-id="dd0ad-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="dd0ad-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dd0ad-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="dd0ad-192">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="dd0ad-193">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd0ad-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="dd0ad-194">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd0ad-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="dd0ad-195">`[Name <String>]`: Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="dd0ad-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="dd0ad-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="dd0ad-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="dd0ad-197">`[Id <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd0ad-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="dd0ad-198">`[OSProfile <ICloudServiceOSProfile>]`: Beschreibt das Betriebssystemprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="dd0ad-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Gibt eine Gruppe von Zertifikaten an, die auf den Rolleninstanzen installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="dd0ad-200">`[SourceVaultId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dd0ad-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="dd0ad-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: Die Liste der Schlüsseltresorverweise in SourceVault, die Zertifikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="dd0ad-202">`[CertificateUrl <String>]`: Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="dd0ad-203">`[PackageUrl <String>]`: Gibt eine URL an, die sich auf den Speicherort des Dienstpakets im Blob-Dienst bezieht.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="dd0ad-204">Die Dienstpaket-URL kann der SAS-URI (Shared Access Signature) aus einem beliebigen Speicherkonto sein.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="dd0ad-205">Dies ist eine Schreibeigenschaft und wird in GET-Aufrufen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="dd0ad-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Beschreibt das Rollenprofil für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="dd0ad-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: Liste der Rollen für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="dd0ad-208">`[Name <String>]`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="dd0ad-209">`[SkuCapacity <Int64?>]`: Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="dd0ad-210">`[SkuName <String>]`: Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="dd0ad-211">HINWEIS: Wenn die neue SKU auf der Hardware, auf der sich der Clouddienst derzeit befindet, nicht unterstützt wird, müssen Sie den Clouddienst löschen und neu erstellen oder zur alten Sku zurück wechseln.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="dd0ad-212">`[SkuTier <String>]`: Gibt die Ebene des Clouddiensts an.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="dd0ad-213">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="dd0ad-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="dd0ad-214">**Standard**</span><span class="sxs-lookup"><span data-stu-id="dd0ad-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="dd0ad-215">**Basic**</span><span class="sxs-lookup"><span data-stu-id="dd0ad-215">**Basic**</span></span>
  - <span data-ttu-id="dd0ad-216">`[StartCloudService <Boolean?>]`: (Optional) Gibt an, ob der Clouddienst unmittelbar nach seiner Er erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="dd0ad-217">Der Standardwert ist `true` .</span><span class="sxs-lookup"><span data-stu-id="dd0ad-217">The default value is `true`.</span></span>         <span data-ttu-id="dd0ad-218">Ist false, wird das Dienstmodell weiterhin bereitgestellt, der Code wird jedoch nicht sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="dd0ad-219">Stattdessen wird der Dienst bis zum Aufrufen von Start eingeschaltet, zu dem der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="dd0ad-220">Für einen bereitgestellten Dienst fallen weiterhin Gebühren an, auch wenn er ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="dd0ad-221">`[Tag <ICloudServiceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="dd0ad-222">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dd0ad-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Updatemodus für den Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="dd0ad-224">Rolleninstanzen werden zugewiesen, um Domänen zu aktualisieren, wenn der Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="dd0ad-225">Updates können in jeder Updatedomäne manuell initiiert oder automatisch in allen Updatedomänen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="dd0ad-226">Mögliche Werte sind</span><span class="sxs-lookup"><span data-stu-id="dd0ad-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="dd0ad-227">**Auto**</span><span class="sxs-lookup"><span data-stu-id="dd0ad-227">**Auto**</span></span><br /><br /><span data-ttu-id="dd0ad-228">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="dd0ad-228">**Manual**</span></span> <br /><br /><span data-ttu-id="dd0ad-229">**Gleichzeitig**</span><span class="sxs-lookup"><span data-stu-id="dd0ad-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="dd0ad-230">Wenn nicht angegeben, ist der Standardwert Auto. Wenn auf Manuell festgelegt ist, muss PUT UpdateDomain aufgerufen werden, um das Update anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="dd0ad-231">Wenn auf Auto festgelegt ist, wird das Update automatisch auf jede Updatedomäne in der Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd0ad-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="dd0ad-232">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd0ad-232">RELATED LINKS</span></span>

