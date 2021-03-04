---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 4504eaf26331fa4e881d6a86f284a74b7f249565
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939040"
---
# <span data-ttu-id="d0edc-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="d0edc-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="d0edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0edc-102">SYNOPSIS</span></span>
<span data-ttu-id="d0edc-103">Der Vorgang "Domänendienst aktualisieren" kann zum Aktualisieren der vorhandenen Bereitstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="d0edc-104">Der Updateaufruf unterstützt nur die im PATCH-Textkörper aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0edc-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="d0edc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0edc-105">SYNTAX</span></span>

### <span data-ttu-id="d0edc-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0edc-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0edc-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d0edc-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0edc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0edc-108">DESCRIPTION</span></span>
<span data-ttu-id="d0edc-109">Der Vorgang "Domänendienst aktualisieren" kann zum Aktualisieren der vorhandenen Bereitstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="d0edc-110">Der Updateaufruf unterstützt nur die im PATCH-Textkörper aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0edc-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="d0edc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0edc-111">EXAMPLES</span></span>

### <span data-ttu-id="d0edc-112">Beispiel 1: Aktualisieren von AzADDomainService nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="d0edc-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="d0edc-113">Aktualisieren von AzADDomainService nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="d0edc-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="d0edc-114">Beispiel 2: Aktualisieren von AzADDomainService by Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0edc-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="d0edc-115">Aktualisieren von AzADDomainService by Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0edc-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="d0edc-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d0edc-116">PARAMETERS</span></span>

### <span data-ttu-id="d0edc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0edc-117">-AsJob</span></span>
<span data-ttu-id="d0edc-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d0edc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d0edc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0edc-119">-DefaultProfile</span></span>
<span data-ttu-id="d0edc-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0edc-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="d0edc-121">-DomainConfigurationType</span></span>
<span data-ttu-id="d0edc-122">Domänenkonfigurationstyp</span><span class="sxs-lookup"><span data-stu-id="d0edc-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="d0edc-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="d0edc-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="d0edc-124">Ein -Kennzeichen, um festzustellen, ob NtlmV1 aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="d0edc-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="d0edc-126">Ein Flag, um festzustellen, ob SyncKerberosPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="d0edc-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="d0edc-128">Ein -Kennzeichen, um festzustellen, ob SyncNtlmPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="d0edc-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="d0edc-130">Ein Flag, um festzustellen, ob SyncOnPremPasswords aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="d0edc-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="d0edc-132">Ein -Kennzeichen, um festzustellen, ob TlsV1 aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="d0edc-133">-FilteredSync</span></span>
<span data-ttu-id="d0edc-134">Kennzeichnung "Aktiviert" oder "Deaktiviert" zum Aktivieren der gruppenbasierten gefilterten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="d0edc-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="d0edc-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="d0edc-135">-ForestTrust</span></span>
<span data-ttu-id="d0edc-136">Liste der Einstellungen für Resource Forest To construct finden Sie im Abschnitt NOTIZEN zu FORESTTRUST-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d0edc-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="d0edc-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0edc-137">-InputObject</span></span>
<span data-ttu-id="d0edc-138">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d0edc-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0edc-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="d0edc-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="d0edc-140">Ein -Kennzeichen, um festzustellen, ob der sichere LDAP-Zugriff über das Internet aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="d0edc-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="d0edc-142">Ein -Kennzeichen, um festzustellen, ob Secure LDAP aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="d0edc-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="d0edc-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="d0edc-144">Das zertifikat, das zum Konfigurieren von Secure LDAP erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d0edc-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="d0edc-145">Der hier übergebene Parameter sollte eine base64-codierte Darstellung der Zertifikat-Pfx-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="d0edc-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="d0edc-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d0edc-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="d0edc-147">Das Kennwort zum Entschlüsseln der bereitgestellten Pfx-Datei für sicheres LDAP-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="d0edc-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="d0edc-148">-Name</span><span class="sxs-lookup"><span data-stu-id="d0edc-148">-Name</span></span>
<span data-ttu-id="d0edc-149">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="d0edc-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0edc-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="d0edc-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="d0edc-151">Die Liste der zusätzlichen Empfänger</span><span class="sxs-lookup"><span data-stu-id="d0edc-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="d0edc-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="d0edc-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="d0edc-153">Sollten Domänencontrolleradministratoren benachrichtigt werden</span><span class="sxs-lookup"><span data-stu-id="d0edc-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="d0edc-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="d0edc-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="d0edc-155">Sollten globale Administratoren benachrichtigt werden</span><span class="sxs-lookup"><span data-stu-id="d0edc-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="d0edc-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0edc-156">-NoWait</span></span>
<span data-ttu-id="d0edc-157">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d0edc-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0edc-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="d0edc-158">-ReplicaSet</span></span>
<span data-ttu-id="d0edc-159">Liste der zu erstellenden ReplicaSets finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d0edc-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0edc-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="d0edc-160">-ResourceForest</span></span>
<span data-ttu-id="d0edc-161">Ressourcenforst</span><span class="sxs-lookup"><span data-stu-id="d0edc-161">Resource Forest</span></span>

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

### <span data-ttu-id="d0edc-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0edc-162">-ResourceGroupName</span></span>
<span data-ttu-id="d0edc-163">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d0edc-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="d0edc-164">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d0edc-164">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0edc-165">-Sku</span><span class="sxs-lookup"><span data-stu-id="d0edc-165">-Sku</span></span>
<span data-ttu-id="d0edc-166">Sku-Typ</span><span class="sxs-lookup"><span data-stu-id="d0edc-166">Sku Type</span></span>

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

### <span data-ttu-id="d0edc-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0edc-167">-SubscriptionId</span></span>
<span data-ttu-id="d0edc-168">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d0edc-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0edc-169">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d0edc-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0edc-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0edc-170">-Tag</span></span>
<span data-ttu-id="d0edc-171">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="d0edc-171">Resource tags</span></span>

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

### <span data-ttu-id="d0edc-172">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0edc-172">-Confirm</span></span>
<span data-ttu-id="d0edc-173">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0edc-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0edc-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0edc-174">-WhatIf</span></span>
<span data-ttu-id="d0edc-175">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0edc-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0edc-176">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0edc-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0edc-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0edc-177">CommonParameters</span></span>
<span data-ttu-id="d0edc-178">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0edc-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0edc-179">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0edc-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0edc-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0edc-180">INPUTS</span></span>

### <span data-ttu-id="d0edc-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="d0edc-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="d0edc-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0edc-182">OUTPUTS</span></span>

### <span data-ttu-id="d0edc-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="d0edc-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="d0edc-184">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d0edc-184">NOTES</span></span>

<span data-ttu-id="d0edc-185">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d0edc-185">ALIASES</span></span>

<span data-ttu-id="d0edc-186">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d0edc-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0edc-187">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d0edc-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0edc-188">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0edc-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0edc-189">FORESTTRUST <IForestTrust[]>: Liste der Einstellungen für Die Ressourcen gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="d0edc-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="d0edc-190">`[FriendlyName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="d0edc-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="d0edc-191">`[RemoteDnsIP <String>]`: Remote-DNS-Ips</span><span class="sxs-lookup"><span data-stu-id="d0edc-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="d0edc-192">`[TrustDirection <String>]`: Richtung vertrauen</span><span class="sxs-lookup"><span data-stu-id="d0edc-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="d0edc-193">`[TrustPassword <String>]`: Kennwort "Vertrauen"</span><span class="sxs-lookup"><span data-stu-id="d0edc-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="d0edc-194">`[TrustedDomainFqdn <String>]`: FQDN für vertrauenswürdige Domäne</span><span class="sxs-lookup"><span data-stu-id="d0edc-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="d0edc-195">INPUTOBJECT <IAdDomainServicesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d0edc-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0edc-196">`[DomainServiceName <String>]`: Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="d0edc-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="d0edc-197">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d0edc-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0edc-198">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d0edc-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="d0edc-199">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d0edc-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="d0edc-200">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d0edc-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d0edc-201">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d0edc-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d0edc-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="d0edc-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="d0edc-203">`[Location <String>]`: Virtueller Netzwerkspeicherort</span><span class="sxs-lookup"><span data-stu-id="d0edc-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="d0edc-204">`[SubnetId <String>]`: Der Name des virtuellen Netzwerks, für das Domain Services bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0edc-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="d0edc-205">Die ID des Subnetzes, für das Domänendienste bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="d0edc-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="d0edc-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="d0edc-207">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d0edc-207">RELATED LINKS</span></span>

