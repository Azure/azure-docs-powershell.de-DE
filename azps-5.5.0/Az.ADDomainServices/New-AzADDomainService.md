---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 977621a3f92a8239925494102aed8c672509b222
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143833"
---
# <span data-ttu-id="1c669-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="1c669-101">New-AzADDomainService</span></span>

## <span data-ttu-id="1c669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c669-102">SYNOPSIS</span></span>
<span data-ttu-id="1c669-103">Der Vorgang "Create Domain Service" erstellt einen neuen Domänendienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="1c669-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="1c669-104">Wenn der spezifische Dienst bereits vorhanden ist, werden alle patchbaren Eigenschaften aktualisiert, und alle unveränderlichen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="1c669-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="1c669-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c669-105">SYNTAX</span></span>

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

## <span data-ttu-id="1c669-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c669-106">DESCRIPTION</span></span>
<span data-ttu-id="1c669-107">Der Vorgang "Create Domain Service" erstellt einen neuen Domänendienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="1c669-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="1c669-108">Wenn der spezifische Dienst bereits vorhanden ist, werden alle patchbaren Eigenschaften aktualisiert, und alle unveränderlichen Eigenschaften bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="1c669-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="1c669-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c669-109">EXAMPLES</span></span>

### <span data-ttu-id="1c669-110">Beispiel 1: Erstellen eines neuen ADDomainService</span><span class="sxs-lookup"><span data-stu-id="1c669-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="1c669-111">Erstellen des neuen ADDomainService</span><span class="sxs-lookup"><span data-stu-id="1c669-111">Create new ADDomainService</span></span>

## <span data-ttu-id="1c669-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c669-112">PARAMETERS</span></span>

### <span data-ttu-id="1c669-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c669-113">-AsJob</span></span>
<span data-ttu-id="1c669-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1c669-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1c669-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c669-115">-DefaultProfile</span></span>
<span data-ttu-id="1c669-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c669-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c669-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="1c669-117">-DomainConfigurationType</span></span>
<span data-ttu-id="1c669-118">Domänenkonfigurationstyp</span><span class="sxs-lookup"><span data-stu-id="1c669-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="1c669-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="1c669-119">-DomainName</span></span>
<span data-ttu-id="1c669-120">Der Name der Azure-Domäne, für die der Benutzer Domänendienste bereitstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="1c669-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="1c669-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="1c669-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="1c669-122">Ein Kennzeichen, um festzustellen, ob "NtlmV1" aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="1c669-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="1c669-124">Ein Kennzeichen, um festzustellen, ob "SyncKerberosPasswords" aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="1c669-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="1c669-126">Ein Kennzeichen, um zu bestimmen, ob "SyncNtlmPasswords" aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="1c669-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="1c669-128">Ein Kennzeichen, um festzustellen, ob "SyncOnPremPasswords" aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="1c669-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="1c669-130">Ein Kennzeichen, um festzustellen, ob TlsV1 aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="1c669-131">-FilteredSync</span></span>
<span data-ttu-id="1c669-132">Flag "Aktiviert" oder "Deaktiviert", um die gruppenbasierte gefilterte Synchronisierung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="1c669-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="1c669-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="1c669-133">-ForestTrust</span></span>
<span data-ttu-id="1c669-134">Liste der Einstellungen für "Ressource: Gesamtstruktur zum Erstellen" finden Sie im Abschnitt "NOTES" zu FORESTTRUST-Eigenschaften und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1c669-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c669-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="1c669-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="1c669-136">Ein Kennzeichen, mit dem Sie feststellen können, ob der Sichere LDAP-Zugriff über das Internet aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="1c669-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="1c669-138">Ein Kennzeichen, mit dem Sie feststellen können, ob Secure LDAP aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="1c669-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="1c669-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="1c669-140">Das Zertifikat, das zum Konfigurieren von sicherem LDAP erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1c669-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="1c669-141">Der hier übergebene Parameter sollte eine base64-codierte Darstellung der Zertifikat-PFX-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="1c669-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="1c669-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1c669-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="1c669-143">Das Kennwort zum Entschlüsseln der bereitgestellten Pfxdatei für sichere LDAP-Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="1c669-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="1c669-144">-Name</span><span class="sxs-lookup"><span data-stu-id="1c669-144">-Name</span></span>
<span data-ttu-id="1c669-145">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="1c669-145">The name of the domain service.</span></span>

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

### <span data-ttu-id="1c669-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="1c669-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="1c669-147">Die Liste der zusätzlichen Empfänger</span><span class="sxs-lookup"><span data-stu-id="1c669-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="1c669-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="1c669-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="1c669-149">Sollten Administratoren des Domänencontrollers benachrichtigt werden?</span><span class="sxs-lookup"><span data-stu-id="1c669-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="1c669-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="1c669-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="1c669-151">Sollten globale Administratoren benachrichtigt werden?</span><span class="sxs-lookup"><span data-stu-id="1c669-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="1c669-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c669-152">-NoWait</span></span>
<span data-ttu-id="1c669-153">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1c669-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c669-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1c669-154">-ReplicaSet</span></span>
<span data-ttu-id="1c669-155">Liste der zu erstellenden ReplicaSets finden Sie im Abschnitt NOTES zu DEN #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1c669-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c669-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="1c669-156">-ResourceForest</span></span>
<span data-ttu-id="1c669-157">Ressourcenforst</span><span class="sxs-lookup"><span data-stu-id="1c669-157">Resource Forest</span></span>

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

### <span data-ttu-id="1c669-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c669-158">-ResourceGroupName</span></span>
<span data-ttu-id="1c669-159">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1c669-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="1c669-160">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="1c669-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c669-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="1c669-161">-Sku</span></span>
<span data-ttu-id="1c669-162">SKU-Typ</span><span class="sxs-lookup"><span data-stu-id="1c669-162">Sku Type</span></span>

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

### <span data-ttu-id="1c669-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c669-163">-SubscriptionId</span></span>
<span data-ttu-id="1c669-164">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1c669-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1c669-165">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="1c669-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1c669-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c669-166">-Tag</span></span>
<span data-ttu-id="1c669-167">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="1c669-167">Resource tags</span></span>

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

### <span data-ttu-id="1c669-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c669-168">-Confirm</span></span>
<span data-ttu-id="1c669-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c669-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c669-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1c669-170">-WhatIf</span></span>
<span data-ttu-id="1c669-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c669-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c669-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c669-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c669-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c669-173">CommonParameters</span></span>
<span data-ttu-id="1c669-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c669-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c669-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c669-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c669-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c669-176">INPUTS</span></span>

## <span data-ttu-id="1c669-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c669-177">OUTPUTS</span></span>

### <span data-ttu-id="1c669-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="1c669-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="1c669-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c669-179">NOTES</span></span>

<span data-ttu-id="1c669-180">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1c669-180">ALIASES</span></span>

<span data-ttu-id="1c669-181">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1c669-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c669-182">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c669-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c669-183">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c669-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c669-184">FORESTTRUST <IForestTrust[]>: Liste der Einstellungen für die Ressourcen gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="1c669-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="1c669-185">`[FriendlyName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1c669-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="1c669-186">`[RemoteDnsIP <String>]`: Remote-DNS-IPS</span><span class="sxs-lookup"><span data-stu-id="1c669-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="1c669-187">`[TrustDirection <String>]`: Vertrauensstellungsrichtung</span><span class="sxs-lookup"><span data-stu-id="1c669-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="1c669-188">`[TrustPassword <String>]`: Kennwort vertrauenswürdig</span><span class="sxs-lookup"><span data-stu-id="1c669-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="1c669-189">`[TrustedDomainFqdn <String>]`: FQDN der vertrauenswürdigen Domäne</span><span class="sxs-lookup"><span data-stu-id="1c669-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="1c669-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="1c669-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="1c669-191">`[Location <String>]`: Virtueller Netzwerkspeicherort</span><span class="sxs-lookup"><span data-stu-id="1c669-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="1c669-192">`[SubnetId <String>]`: Der Name des virtuellen Netzwerks, für das Domain Services bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c669-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="1c669-193">Die ID des Subnetzes, in dem Domänendienste bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c669-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="1c669-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="1c669-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="1c669-195">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c669-195">RELATED LINKS</span></span>

