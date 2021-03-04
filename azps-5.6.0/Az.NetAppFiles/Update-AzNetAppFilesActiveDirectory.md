---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 3baa4a20d6109d2767dee1b4ff53e2b363adfccf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926683"
---
# <span data-ttu-id="0cb95-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cb95-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cb95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cb95-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb95-103">Aktualisiert eine Azure NetApp Files (ANF)-Active Directory-Konfiguration auf die optionalen bereitgestellten Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="0cb95-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="0cb95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cb95-104">SYNTAX</span></span>

### <span data-ttu-id="0cb95-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cb95-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb95-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cb95-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb95-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cb95-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cb95-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cb95-108">DESCRIPTION</span></span>
<span data-ttu-id="0cb95-109">Das **Update-AzNetAppFilesAccount-Cmdlet** ändert eine ANF-Active Directory-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0cb95-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="0cb95-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0cb95-110">EXAMPLES</span></span>

### <span data-ttu-id="0cb95-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cb95-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="0cb95-112">Mit diesem Befehl wird eine Aktualisierung der angegebenen Active Directory-Konfiguration ausgeführt, bei der der Benutzername an die angegebene Konfiguration geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0cb95-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="0cb95-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0cb95-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb95-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cb95-114">-AccountName</span></span>
<span data-ttu-id="0cb95-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0cb95-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0cb95-116">-AccountObject</span></span>
<span data-ttu-id="0cb95-117">Das Konto für das Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="0cb95-117">The account for the active directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="0cb95-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="0cb95-119">Die ID des ANF-Active Directory</span><span class="sxs-lookup"><span data-stu-id="0cb95-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="0cb95-120">-AdName</span></span>
<span data-ttu-id="0cb95-121">Name des Active Directory-Computers.</span><span class="sxs-lookup"><span data-stu-id="0cb95-121">Name of the active directory machine.</span></span>
<span data-ttu-id="0cb95-122">Dieser optionale Parameter wird nur beim Erstellen des Kerberosvolumes verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cb95-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="0cb95-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="0cb95-123">-BackupOperator</span></span>
<span data-ttu-id="0cb95-124">Benutzer, die der Active Directory-Gruppe des integrierten Sicherungsoperators hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cb95-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="0cb95-125">Eine Liste eindeutiger Benutzernamen ohne Domänenbezeichner</span><span class="sxs-lookup"><span data-stu-id="0cb95-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="0cb95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb95-126">-DefaultProfile</span></span>
<span data-ttu-id="0cb95-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cb95-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="0cb95-128">-Dns</span></span>
<span data-ttu-id="0cb95-129">Durch Kommas getrennte Liste der DNS-Server-IP-Adressen (nur IPv4) für die Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="0cb95-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="0cb95-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="0cb95-130">-Domain</span></span>
<span data-ttu-id="0cb95-131">Name der Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="0cb95-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="0cb95-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cb95-132">-InputObject</span></span>
<span data-ttu-id="0cb95-133">Das zu entfernende Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="0cb95-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="0cb95-134">-KdcIP</span></span>
<span data-ttu-id="0cb95-135">kdc server-IP-Adressen für den Active Directory-Computer.</span><span class="sxs-lookup"><span data-stu-id="0cb95-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="0cb95-136">Dieser optionale Parameter wird nur beim Erstellen des Kerberosvolumens verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cb95-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="0cb95-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="0cb95-137">-OrganizationalUnit</span></span>
<span data-ttu-id="0cb95-138">Organisationseinheit (OU) im Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="0cb95-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="0cb95-139">-Password</span><span class="sxs-lookup"><span data-stu-id="0cb95-139">-Password</span></span>
<span data-ttu-id="0cb95-140">Nur-Text-Kennwort des Active Directory-Domänenadministrators, Wert wird in der Antwort maskiert</span><span class="sxs-lookup"><span data-stu-id="0cb95-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="0cb95-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb95-141">-ResourceGroupName</span></span>
<span data-ttu-id="0cb95-142">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0cb95-142">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cb95-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="0cb95-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="0cb95-144">Wenn LDAP über SSL/TLS aktiviert ist, muss der LDAP-Client über das selbst signierte Stammzertifizierungszertifikat des Active Directory-Zertifikats base64 verfügen. Dieser optionale Parameter wird nur für zwei Protokolle mit LDAP-Benutzerzuordnungsvolumes verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cb95-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="0cb95-145">-Website</span><span class="sxs-lookup"><span data-stu-id="0cb95-145">-Site</span></span>
<span data-ttu-id="0cb95-146">Die Active Directory-Website, auf der der Dienst die Domänencontrollerermittlung auf</span><span class="sxs-lookup"><span data-stu-id="0cb95-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="0cb95-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="0cb95-147">-SmbServerName</span></span>
<span data-ttu-id="0cb95-148">NetBIOS-Name des SMB-Servers.</span><span class="sxs-lookup"><span data-stu-id="0cb95-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="0cb95-149">Dieser Name wird als Computerkonto in der AD registriert und zum Mounten von Volumes verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cb95-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="0cb95-150">-Benutzername</span><span class="sxs-lookup"><span data-stu-id="0cb95-150">-Username</span></span>
<span data-ttu-id="0cb95-151">Benutzername des Active Directory-Domänenadministrators</span><span class="sxs-lookup"><span data-stu-id="0cb95-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="0cb95-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0cb95-152">-Confirm</span></span>
<span data-ttu-id="0cb95-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cb95-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb95-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb95-154">-WhatIf</span></span>
<span data-ttu-id="0cb95-155">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cb95-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb95-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cb95-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb95-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb95-157">CommonParameters</span></span>
<span data-ttu-id="0cb95-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb95-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb95-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cb95-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb95-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0cb95-160">INPUTS</span></span>

### <span data-ttu-id="0cb95-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0cb95-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="0cb95-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cb95-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cb95-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0cb95-163">OUTPUTS</span></span>

### <span data-ttu-id="0cb95-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cb95-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cb95-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0cb95-165">NOTES</span></span>

## <span data-ttu-id="0cb95-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0cb95-166">RELATED LINKS</span></span>
