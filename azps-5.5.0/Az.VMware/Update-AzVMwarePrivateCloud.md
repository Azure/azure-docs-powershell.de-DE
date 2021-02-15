---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174825"
---
# <span data-ttu-id="8f249-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="8f249-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="8f249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f249-102">SYNOPSIS</span></span>
<span data-ttu-id="8f249-103">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-103">Update a private cloud</span></span>

## <span data-ttu-id="8f249-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f249-104">SYNTAX</span></span>

### <span data-ttu-id="8f249-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f249-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f249-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f249-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f249-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f249-107">DESCRIPTION</span></span>
<span data-ttu-id="8f249-108">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-108">Update a private cloud</span></span>

## <span data-ttu-id="8f249-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f249-109">EXAMPLES</span></span>

### <span data-ttu-id="8f249-110">Beispiel 1: Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="8f249-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="8f249-111">Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="8f249-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="8f249-112">Beispiel 2: Aktualisieren der Größe der privaten Cloud durch Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="8f249-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="8f249-113">Aktualisieren der Größe der privaten Cloud durch Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="8f249-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="8f249-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f249-114">PARAMETERS</span></span>

### <span data-ttu-id="8f249-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f249-115">-AsJob</span></span>
<span data-ttu-id="8f249-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8f249-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8f249-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f249-117">-DefaultProfile</span></span>
<span data-ttu-id="8f249-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f249-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f249-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="8f249-119">-IdentitySource</span></span>
<span data-ttu-id="8f249-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8f249-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f249-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f249-121">-InputObject</span></span>
<span data-ttu-id="8f249-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8f249-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f249-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="8f249-123">-Internet</span></span>
<span data-ttu-id="8f249-124">Die Internetverbindung ist aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="8f249-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f249-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="8f249-125">-ManagementClusterSize</span></span>
<span data-ttu-id="8f249-126">Clustergröße</span><span class="sxs-lookup"><span data-stu-id="8f249-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f249-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8f249-127">-Name</span></span>
<span data-ttu-id="8f249-128">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f249-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f249-129">-NoWait</span></span>
<span data-ttu-id="8f249-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8f249-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f249-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f249-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f249-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f249-132">The name of the resource group.</span></span>
<span data-ttu-id="8f249-133">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8f249-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8f249-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f249-134">-SubscriptionId</span></span>
<span data-ttu-id="8f249-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8f249-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8f249-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f249-136">-Tag</span></span>
<span data-ttu-id="8f249-137">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="8f249-137">Resource tags.</span></span>

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

### <span data-ttu-id="8f249-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f249-138">-Confirm</span></span>
<span data-ttu-id="8f249-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f249-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f249-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f249-140">-WhatIf</span></span>
<span data-ttu-id="8f249-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f249-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f249-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f249-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f249-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f249-143">CommonParameters</span></span>
<span data-ttu-id="8f249-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f249-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f249-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f249-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f249-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f249-146">INPUTS</span></span>

### <span data-ttu-id="8f249-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="8f249-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="8f249-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f249-148">OUTPUTS</span></span>

### <span data-ttu-id="8f249-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="8f249-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="8f249-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f249-150">NOTES</span></span>

<span data-ttu-id="8f249-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8f249-151">ALIASES</span></span>

<span data-ttu-id="8f249-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8f249-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f249-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f249-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f249-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f249-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f249-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="8f249-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="8f249-156">`[Alias <String>]`: Der Name der Domäne (NetERGEBNISS)</span><span class="sxs-lookup"><span data-stu-id="8f249-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="8f249-157">`[BaseGroupDn <String>]`: Der Distinguished Base Name für Gruppen</span><span class="sxs-lookup"><span data-stu-id="8f249-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="8f249-158">`[BaseUserDn <String>]`: Der Distinguished Base Name für Benutzer</span><span class="sxs-lookup"><span data-stu-id="8f249-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="8f249-159">`[Domain <String>]`: Der Dnsname der Domäne</span><span class="sxs-lookup"><span data-stu-id="8f249-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="8f249-160">`[Name <String>]`: Der Name der Identitätsquelle</span><span class="sxs-lookup"><span data-stu-id="8f249-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="8f249-161">`[Password <String>]`: Das Kennwort des Active Directory-Benutzers mit einem Minimum an schreibgeschützten Zugriff auf Basis-DN für Benutzer und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="8f249-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="8f249-162">`[PrimaryServer <String>]`: Primäre Server-URL</span><span class="sxs-lookup"><span data-stu-id="8f249-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="8f249-163">`[SecondaryServer <String>]`: URL des sekundären Servers</span><span class="sxs-lookup"><span data-stu-id="8f249-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="8f249-164">`[Ssl <SslEnum?>]`: Schützen der LDAP-Kommunikation mithilfe von SSL-Zertifikaten (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="8f249-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="8f249-165">`[Username <String>]`: Die ID eines Active Directory-Benutzers mit einem Minimum an schreibgeschützten Zugriff auf Basis-DN für Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="8f249-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="8f249-166">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8f249-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f249-167">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="8f249-168">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="8f249-169">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="8f249-170">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8f249-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f249-171">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="8f249-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="8f249-172">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8f249-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="8f249-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f249-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8f249-174">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8f249-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="8f249-175">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8f249-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8f249-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f249-176">RELATED LINKS</span></span>

