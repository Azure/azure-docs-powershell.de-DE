---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935915"
---
# <span data-ttu-id="7c57b-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="7c57b-101">New-AzADDomainService</span></span>

## <span data-ttu-id="7c57b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c57b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c57b-103">Der Vorgang Domänendienst erstellen erstellt einen neuen Domänendienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="7c57b-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="7c57b-104">Wenn der spezifische Dienst bereits vorhanden ist, werden alle patchbaren Eigenschaften aktualisiert, und alle unveränderlichen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="7c57b-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="7c57b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c57b-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c57b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c57b-106">DESCRIPTION</span></span>
<span data-ttu-id="7c57b-107">Der Vorgang Domänendienst erstellen erstellt einen neuen Domänendienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="7c57b-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="7c57b-108">Wenn der spezifische Dienst bereits vorhanden ist, werden alle patchbaren Eigenschaften aktualisiert, und alle unveränderlichen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="7c57b-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="7c57b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c57b-109">EXAMPLES</span></span>

### <span data-ttu-id="7c57b-110">Beispiel 1: Erstellen des neuen ADDomainService</span><span class="sxs-lookup"><span data-stu-id="7c57b-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="7c57b-111">Erstellen des neuen ADDomainService</span><span class="sxs-lookup"><span data-stu-id="7c57b-111">Create new ADDomainService</span></span>

## <span data-ttu-id="7c57b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c57b-112">PARAMETERS</span></span>

### <span data-ttu-id="7c57b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c57b-113">-AsJob</span></span>
<span data-ttu-id="7c57b-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7c57b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7c57b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c57b-115">-DefaultProfile</span></span>
<span data-ttu-id="7c57b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c57b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c57b-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="7c57b-117">-DomainConfigurationType</span></span>
<span data-ttu-id="7c57b-118">Domänenkonfigurationstyp</span><span class="sxs-lookup"><span data-stu-id="7c57b-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="7c57b-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="7c57b-119">-DomainName</span></span>
<span data-ttu-id="7c57b-120">Der Name der Azure-Domäne, für die der Benutzer Domänendienste bereitstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="7c57b-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="7c57b-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="7c57b-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="7c57b-122">Ein -Kennzeichen, um festzustellen, ob NtlmV1 aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="7c57b-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="7c57b-124">Ein Flag, um festzustellen, ob SyncKerberosPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="7c57b-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="7c57b-126">Ein -Kennzeichen, um festzustellen, ob SyncNtlmPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="7c57b-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="7c57b-128">Ein Flag, um festzustellen, ob SyncOnPremPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="7c57b-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="7c57b-130">Ein -Kennzeichen, um festzustellen, ob TlsV1 aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="7c57b-131">-FilteredSync</span></span>
<span data-ttu-id="7c57b-132">Kennzeichnung "Aktiviert" oder "Deaktiviert" zum Aktivieren der gruppenbasierten gefilterten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7c57b-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="7c57b-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="7c57b-133">-ForestTrust</span></span>
<span data-ttu-id="7c57b-134">Liste der Einstellungen für Resource Forest To construct finden Sie im Abschnitt NOTIZEN zu FORESTTRUST-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7c57b-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="7c57b-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="7c57b-136">Ein -Kennzeichen, um festzustellen, ob der sichere LDAP-Zugriff über das Internet aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="7c57b-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="7c57b-138">Ein -Kennzeichen, um festzustellen, ob Secure LDAP aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c57b-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="7c57b-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="7c57b-140">Das zertifikat, das zum Konfigurieren von Secure LDAP erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7c57b-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="7c57b-141">Der hier übergebene Parameter sollte eine base64-codierte Darstellung der Zertifikat-Pfx-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="7c57b-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="7c57b-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7c57b-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="7c57b-143">Das Kennwort zum Entschlüsseln der bereitgestellten Pfx-Datei für sicheres LDAP-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="7c57b-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-144">-Name</span><span class="sxs-lookup"><span data-stu-id="7c57b-144">-Name</span></span>
<span data-ttu-id="7c57b-145">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="7c57b-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="7c57b-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="7c57b-147">Die Liste der zusätzlichen Empfänger</span><span class="sxs-lookup"><span data-stu-id="7c57b-147">The list of additional recipients</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="7c57b-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="7c57b-149">Sollten Domänencontrolleradministratoren benachrichtigt werden</span><span class="sxs-lookup"><span data-stu-id="7c57b-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="7c57b-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="7c57b-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="7c57b-151">Sollten globale Administratoren benachrichtigt werden</span><span class="sxs-lookup"><span data-stu-id="7c57b-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="7c57b-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c57b-152">-NoWait</span></span>
<span data-ttu-id="7c57b-153">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7c57b-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c57b-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="7c57b-154">-ReplicaSet</span></span>
<span data-ttu-id="7c57b-155">Liste der zu erstellenden ReplicaSets finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7c57b-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="7c57b-156">-ResourceForest</span></span>
<span data-ttu-id="7c57b-157">Ressourcenforst</span><span class="sxs-lookup"><span data-stu-id="7c57b-157">Resource Forest</span></span>

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

### <span data-ttu-id="7c57b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c57b-158">-ResourceGroupName</span></span>
<span data-ttu-id="7c57b-159">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7c57b-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="7c57b-160">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="7c57b-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7c57b-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c57b-161">-Sku</span></span>
<span data-ttu-id="7c57b-162">Sku-Typ</span><span class="sxs-lookup"><span data-stu-id="7c57b-162">Sku Type</span></span>

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

### <span data-ttu-id="7c57b-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c57b-163">-SubscriptionId</span></span>
<span data-ttu-id="7c57b-164">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7c57b-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c57b-165">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="7c57b-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7c57b-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c57b-166">-Tag</span></span>
<span data-ttu-id="7c57b-167">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="7c57b-167">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c57b-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c57b-168">-Confirm</span></span>
<span data-ttu-id="7c57b-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c57b-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c57b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c57b-170">-WhatIf</span></span>
<span data-ttu-id="7c57b-171">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c57b-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c57b-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c57b-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c57b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c57b-173">CommonParameters</span></span>
<span data-ttu-id="7c57b-174">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c57b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c57b-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c57b-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c57b-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c57b-176">INPUTS</span></span>

## <span data-ttu-id="7c57b-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c57b-177">OUTPUTS</span></span>

### <span data-ttu-id="7c57b-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="7c57b-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="7c57b-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7c57b-179">NOTES</span></span>

<span data-ttu-id="7c57b-180">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7c57b-180">ALIASES</span></span>

<span data-ttu-id="7c57b-181">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7c57b-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c57b-182">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7c57b-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c57b-183">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c57b-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c57b-184">FORESTTRUST <IForestTrust[]>: Liste der Einstellungen für Die Ressourcen gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="7c57b-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="7c57b-185">`[FriendlyName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="7c57b-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="7c57b-186">`[RemoteDnsIP <String>]`: Remote-DNS-Ips</span><span class="sxs-lookup"><span data-stu-id="7c57b-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="7c57b-187">`[TrustDirection <String>]`: Richtung vertrauen</span><span class="sxs-lookup"><span data-stu-id="7c57b-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="7c57b-188">`[TrustPassword <String>]`: Kennwort "Vertrauen"</span><span class="sxs-lookup"><span data-stu-id="7c57b-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="7c57b-189">`[TrustedDomainFqdn <String>]`: FQDN für vertrauenswürdige Domäne</span><span class="sxs-lookup"><span data-stu-id="7c57b-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="7c57b-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="7c57b-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="7c57b-191">`[Location <String>]`: Virtueller Netzwerkspeicherort</span><span class="sxs-lookup"><span data-stu-id="7c57b-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="7c57b-192">`[SubnetId <String>]`: Der Name des virtuellen Netzwerks, für das Domain Services bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c57b-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="7c57b-193">Die ID des Subnetzes, für das Domänendienste bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7c57b-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="7c57b-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="7c57b-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="7c57b-195">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7c57b-195">RELATED LINKS</span></span>

