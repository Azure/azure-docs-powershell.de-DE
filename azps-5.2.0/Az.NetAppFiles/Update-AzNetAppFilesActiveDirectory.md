---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295409"
---
# <span data-ttu-id="5e67f-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5e67f-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5e67f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e67f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e67f-103">Aktualisiert eine Konfiguration von Azure NetApp Files (ANF) Active Directory auf die optionalen Zusatzmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="5e67f-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="5e67f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e67f-104">SYNTAX</span></span>

### <span data-ttu-id="5e67f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e67f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e67f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e67f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e67f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e67f-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e67f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e67f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e67f-109">Das **Cmdlet "Update-AzNetAppFilesAccount"** ändert eine ANF Active Directory-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5e67f-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="5e67f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e67f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e67f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e67f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="5e67f-112">Dieser Befehl führt eine Aktualisierung für die angegebene Active Directory-Konfiguration aus und ändert den Benutzernamen in die angegebene Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5e67f-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="5e67f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e67f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e67f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e67f-114">-AccountName</span></span>
<span data-ttu-id="5e67f-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="5e67f-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5e67f-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5e67f-116">-AccountObject</span></span>
<span data-ttu-id="5e67f-117">Das Konto für das Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="5e67f-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="5e67f-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="5e67f-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="5e67f-119">Die ID des ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e67f-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="5e67f-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="5e67f-120">-AdName</span></span>
<span data-ttu-id="5e67f-121">Name des Active Directory-Computers.</span><span class="sxs-lookup"><span data-stu-id="5e67f-121">Name of the active directory machine.</span></span>
<span data-ttu-id="5e67f-122">Dieser optionale Parameter wird nur beim Erstellen von Kerberos-Volume</span><span class="sxs-lookup"><span data-stu-id="5e67f-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="5e67f-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="5e67f-123">-BackupOperator</span></span>
<span data-ttu-id="5e67f-124">Benutzer, die der Active Directory-Gruppe "Integrierter Sicherungsoperator" hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e67f-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="5e67f-125">Eine Liste mit eindeutigen Benutzernamen ohne Domänenbezeichner</span><span class="sxs-lookup"><span data-stu-id="5e67f-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="5e67f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e67f-126">-DefaultProfile</span></span>
<span data-ttu-id="5e67f-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e67f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e67f-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="5e67f-128">-Dns</span></span>
<span data-ttu-id="5e67f-129">Durch Kommas getrennte Liste der DNS-Server-IP-Adressen (nur IPv4) für die Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="5e67f-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="5e67f-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="5e67f-130">-Domain</span></span>
<span data-ttu-id="5e67f-131">Name der Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="5e67f-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="5e67f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e67f-132">-InputObject</span></span>
<span data-ttu-id="5e67f-133">Das zu entfernende Active Directory-Objekt</span><span class="sxs-lookup"><span data-stu-id="5e67f-133">The active directory object to remove</span></span>

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

### <span data-ttu-id="5e67f-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="5e67f-134">-KdcIP</span></span>
<span data-ttu-id="5e67f-135">Kdc-Server-IP-Adressen für den Active Directory-Computer.</span><span class="sxs-lookup"><span data-stu-id="5e67f-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="5e67f-136">Dieser optionale Parameter wird nur beim Erstellen von Kerberos verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e67f-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="5e67f-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="5e67f-137">-OrganizationalUnit</span></span>
<span data-ttu-id="5e67f-138">Organisationseinheit im Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e67f-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="5e67f-139">-Password</span><span class="sxs-lookup"><span data-stu-id="5e67f-139">-Password</span></span>
<span data-ttu-id="5e67f-140">Nur-Text-Kennwort des Active Directory-Domänenadministrators, der Wert wird in der Antwort maskiert</span><span class="sxs-lookup"><span data-stu-id="5e67f-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="5e67f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e67f-141">-ResourceGroupName</span></span>
<span data-ttu-id="5e67f-142">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="5e67f-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5e67f-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="5e67f-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="5e67f-144">Wenn LDAP über SSL/TLS aktiviert ist, muss das selbst signierte Stammzertifikat des Active Directory-Zertifikatdiensts base64-codiert sein. Dieser optionale Parameter wird nur für duales Protokoll mit LDAP-Benutzerzuordnungsvolumen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e67f-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="5e67f-145">-Site</span><span class="sxs-lookup"><span data-stu-id="5e67f-145">-Site</span></span>
<span data-ttu-id="5e67f-146">Die Active Directory-Website, auf die der Dienst die Domänencontrollerermittlung auf</span><span class="sxs-lookup"><span data-stu-id="5e67f-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="5e67f-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="5e67f-147">-SmbServerName</span></span>
<span data-ttu-id="5e67f-148">Der Name von NetANJAS des SMB-Servers.</span><span class="sxs-lookup"><span data-stu-id="5e67f-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="5e67f-149">Dieser Name wird als Computerkonto im Ad registriert und zum</span><span class="sxs-lookup"><span data-stu-id="5e67f-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="5e67f-150">-Username</span><span class="sxs-lookup"><span data-stu-id="5e67f-150">-Username</span></span>
<span data-ttu-id="5e67f-151">Benutzername des Active Directory-Domänenadministrators</span><span class="sxs-lookup"><span data-stu-id="5e67f-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="5e67f-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e67f-152">-Confirm</span></span>
<span data-ttu-id="5e67f-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e67f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e67f-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e67f-154">-WhatIf</span></span>
<span data-ttu-id="5e67f-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e67f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e67f-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e67f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e67f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e67f-157">CommonParameters</span></span>
<span data-ttu-id="5e67f-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e67f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e67f-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e67f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e67f-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e67f-160">INPUTS</span></span>

### <span data-ttu-id="5e67f-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5e67f-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="5e67f-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5e67f-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5e67f-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e67f-163">OUTPUTS</span></span>

### <span data-ttu-id="5e67f-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5e67f-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5e67f-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e67f-165">NOTES</span></span>

## <span data-ttu-id="5e67f-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e67f-166">RELATED LINKS</span></span>
