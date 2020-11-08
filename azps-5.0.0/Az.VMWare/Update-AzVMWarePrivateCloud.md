---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180140"
---
# <span data-ttu-id="bb7cc-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="bb7cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7cc-103">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-103">Update a private cloud</span></span>

## <span data-ttu-id="bb7cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb7cc-104">SYNTAX</span></span>

### <span data-ttu-id="bb7cc-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb7cc-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb7cc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bb7cc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb7cc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb7cc-107">DESCRIPTION</span></span>
<span data-ttu-id="bb7cc-108">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-108">Update a private cloud</span></span>

## <span data-ttu-id="bb7cc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb7cc-109">EXAMPLES</span></span>

### <span data-ttu-id="bb7cc-110">Beispiel 1: Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="bb7cc-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="bb7cc-111">Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="bb7cc-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="bb7cc-112">Beispiel 2: Aktualisieren der Größe der privaten Cloud nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="bb7cc-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="bb7cc-113">Aktualisieren der Größe der privaten Cloud nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="bb7cc-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="bb7cc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb7cc-114">PARAMETERS</span></span>

### <span data-ttu-id="bb7cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb7cc-115">-AsJob</span></span>
<span data-ttu-id="bb7cc-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bb7cc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bb7cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7cc-117">-DefaultProfile</span></span>
<span data-ttu-id="bb7cc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb7cc-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="bb7cc-119">-IdentitySource</span></span>
<span data-ttu-id="bb7cc-120">vCenter Single Sign on Identity sources to construct, siehe Abschnitt "Notizen" für IDENTITYSOURCE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7cc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb7cc-121">-InputObject</span></span>
<span data-ttu-id="bb7cc-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7cc-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="bb7cc-123">-Internet</span></span>
<span data-ttu-id="bb7cc-124">Die Verbindung zum Internet ist aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7cc-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="bb7cc-125">-ManagementClusterSize</span></span>
<span data-ttu-id="bb7cc-126">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="bb7cc-126">The cluster size</span></span>

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

### <span data-ttu-id="bb7cc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="bb7cc-127">-Name</span></span>
<span data-ttu-id="bb7cc-128">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="bb7cc-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bb7cc-129">-NoWait</span></span>
<span data-ttu-id="bb7cc-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bb7cc-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb7cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="bb7cc-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-132">The name of the resource group.</span></span>
<span data-ttu-id="bb7cc-133">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bb7cc-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bb7cc-134">-SubscriptionId</span></span>
<span data-ttu-id="bb7cc-135">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bb7cc-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb7cc-136">-Tag</span></span>
<span data-ttu-id="bb7cc-137">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-137">Resource tags.</span></span>

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

### <span data-ttu-id="bb7cc-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb7cc-138">-Confirm</span></span>
<span data-ttu-id="bb7cc-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb7cc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb7cc-140">-WhatIf</span></span>
<span data-ttu-id="bb7cc-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb7cc-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb7cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7cc-143">CommonParameters</span></span>
<span data-ttu-id="bb7cc-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7cc-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb7cc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7cc-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb7cc-146">INPUTS</span></span>

### <span data-ttu-id="bb7cc-147">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="bb7cc-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="bb7cc-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb7cc-148">OUTPUTS</span></span>

### <span data-ttu-id="bb7cc-149">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="bb7cc-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb7cc-150">NOTES</span></span>

<span data-ttu-id="bb7cc-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="bb7cc-151">ALIASES</span></span>

<span data-ttu-id="bb7cc-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb7cc-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb7cc-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb7cc-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb7cc-155">IDENTITYSOURCE <IIdentitySource [] >: vCenter Single Sign on Identity sources</span><span class="sxs-lookup"><span data-stu-id="bb7cc-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="bb7cc-156">`[Alias <String>]`: Der NetBIOS-Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="bb7cc-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="bb7cc-157">`[BaseGroupDn <String>]`: Der Basis-Distinguished Name für Gruppen</span><span class="sxs-lookup"><span data-stu-id="bb7cc-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="bb7cc-158">`[BaseUserDn <String>]`: Der Basis-Distinguished Name für Benutzer</span><span class="sxs-lookup"><span data-stu-id="bb7cc-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="bb7cc-159">`[Domain <String>]`: Der DNS-Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="bb7cc-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="bb7cc-160">`[Name <String>]`: Der Name der Identitäts Quelle</span><span class="sxs-lookup"><span data-stu-id="bb7cc-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="bb7cc-161">`[Password <String>]`: Das Kennwort des Active Directory-Benutzers mit einem Mindest-schreibgeschützten Zugriff auf den Basis-DN für Benutzer und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="bb7cc-162">`[PrimaryServer <String>]`: Primäre Server-URL</span><span class="sxs-lookup"><span data-stu-id="bb7cc-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="bb7cc-163">`[SecondaryServer <String>]`: Sekundäre Server-URL</span><span class="sxs-lookup"><span data-stu-id="bb7cc-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="bb7cc-164">`[Ssl <SslEnum?>]`: Schützen der LDAP-Kommunikation mit SSL-Zertifikat (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="bb7cc-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="bb7cc-165">`[Username <String>]`: Die ID eines Active Directory-Benutzers mit einem Mindest-schreibgeschützten Zugriff auf den Basis-DN für Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="bb7cc-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="bb7cc-166">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="bb7cc-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb7cc-167">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="bb7cc-168">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="bb7cc-169">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="bb7cc-170">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="bb7cc-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb7cc-171">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="bb7cc-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="bb7cc-172">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="bb7cc-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="bb7cc-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bb7cc-174">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="bb7cc-175">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="bb7cc-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="bb7cc-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb7cc-176">RELATED LINKS</span></span>

