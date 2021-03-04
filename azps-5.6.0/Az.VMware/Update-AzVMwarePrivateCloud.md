---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: fbb45450352a99edc5a89d24ac8eb6bc4bcbf383
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936387"
---
# <span data-ttu-id="ab4ba-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="ab4ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4ba-103">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-103">Update a private cloud</span></span>

## <span data-ttu-id="ab4ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab4ba-104">SYNTAX</span></span>

### <span data-ttu-id="ab4ba-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab4ba-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab4ba-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ab4ba-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab4ba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab4ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ab4ba-108">Aktualisieren einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-108">Update a private cloud</span></span>

## <span data-ttu-id="ab4ba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab4ba-109">EXAMPLES</span></span>

### <span data-ttu-id="ab4ba-110">Beispiel 1: Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="ab4ba-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ab4ba-111">Aktualisieren der Größe der privaten Cloud nach Name</span><span class="sxs-lookup"><span data-stu-id="ab4ba-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="ab4ba-112">Beispiel 2: Aktualisieren der Größe der privaten Cloud nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="ab4ba-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ab4ba-113">Aktualisieren der Größe der privaten Cloud nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="ab4ba-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="ab4ba-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab4ba-114">PARAMETERS</span></span>

### <span data-ttu-id="ab4ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab4ba-115">-AsJob</span></span>
<span data-ttu-id="ab4ba-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ab4ba-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ab4ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4ba-117">-DefaultProfile</span></span>
<span data-ttu-id="ab4ba-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab4ba-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="ab4ba-119">-IdentitySource</span></span>
<span data-ttu-id="ab4ba-120">vCenter Single Sign On Identity Sources (Einmaliges Anmelden bei Identitätsquellen) Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für IDENTITYSOURCE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab4ba-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab4ba-121">-InputObject</span></span>
<span data-ttu-id="ab4ba-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab4ba-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="ab4ba-123">-Internet</span></span>
<span data-ttu-id="ab4ba-124">Die Internetverbindung ist aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="ab4ba-124">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="ab4ba-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="ab4ba-125">-ManagementClusterSize</span></span>
<span data-ttu-id="ab4ba-126">Die Clustergröße</span><span class="sxs-lookup"><span data-stu-id="ab4ba-126">The cluster size</span></span>

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

### <span data-ttu-id="ab4ba-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ab4ba-127">-Name</span></span>
<span data-ttu-id="ab4ba-128">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="ab4ba-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ab4ba-129">-NoWait</span></span>
<span data-ttu-id="ab4ba-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ab4ba-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ab4ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab4ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="ab4ba-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-132">The name of the resource group.</span></span>
<span data-ttu-id="ab4ba-133">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ab4ba-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab4ba-134">-SubscriptionId</span></span>
<span data-ttu-id="ab4ba-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ab4ba-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab4ba-136">-Tag</span></span>
<span data-ttu-id="ab4ba-137">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-137">Resource tags.</span></span>

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

### <span data-ttu-id="ab4ba-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab4ba-138">-Confirm</span></span>
<span data-ttu-id="ab4ba-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab4ba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4ba-140">-WhatIf</span></span>
<span data-ttu-id="ab4ba-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab4ba-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab4ba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4ba-143">CommonParameters</span></span>
<span data-ttu-id="ab4ba-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4ba-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab4ba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4ba-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab4ba-146">INPUTS</span></span>

### <span data-ttu-id="ab4ba-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ab4ba-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ab4ba-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab4ba-148">OUTPUTS</span></span>

### <span data-ttu-id="ab4ba-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="ab4ba-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab4ba-150">NOTES</span></span>

<span data-ttu-id="ab4ba-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ab4ba-151">ALIASES</span></span>

<span data-ttu-id="ab4ba-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ab4ba-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab4ba-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab4ba-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab4ba-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="ab4ba-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="ab4ba-156">`[Alias <String>]`: Der NetBIOS-Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="ab4ba-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="ab4ba-157">`[BaseGroupDn <String>]`: Der unterscheide Basisname für Gruppen</span><span class="sxs-lookup"><span data-stu-id="ab4ba-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="ab4ba-158">`[BaseUserDn <String>]`: Der unterscheide Name der Basis für Benutzer</span><span class="sxs-lookup"><span data-stu-id="ab4ba-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="ab4ba-159">`[Domain <String>]`: Der Dnsname der Domäne</span><span class="sxs-lookup"><span data-stu-id="ab4ba-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="ab4ba-160">`[Name <String>]`: Der Name der Identitätsquelle</span><span class="sxs-lookup"><span data-stu-id="ab4ba-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="ab4ba-161">`[Password <String>]`: Das Kennwort des Active Directory-Benutzers mit einem Minimum an schreibgeschützten Zugriff auf Basis-DN für Benutzer und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="ab4ba-162">`[PrimaryServer <String>]`: Primäre Server-URL</span><span class="sxs-lookup"><span data-stu-id="ab4ba-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="ab4ba-163">`[SecondaryServer <String>]`: URL des sekundären Servers</span><span class="sxs-lookup"><span data-stu-id="ab4ba-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="ab4ba-164">`[Ssl <SslEnum?>]`: Schützen der LDAP-Kommunikation mithilfe von SSL-Zertifikaten (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="ab4ba-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="ab4ba-165">`[Username <String>]`: Die ID eines Active Directory-Benutzers mit einem Minimum an schreibgeschützten Zugriff auf Basis-DN für Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="ab4ba-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="ab4ba-166">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="ab4ba-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab4ba-167">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ab4ba-168">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ab4ba-169">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ab4ba-170">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ab4ba-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab4ba-171">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="ab4ba-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ab4ba-172">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="ab4ba-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ab4ba-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ab4ba-174">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="ab4ba-175">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ab4ba-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ab4ba-176">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab4ba-176">RELATED LINKS</span></span>

