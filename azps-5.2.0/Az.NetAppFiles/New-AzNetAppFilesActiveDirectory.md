---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359986"
---
# <span data-ttu-id="89531-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="89531-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="89531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89531-102">SYNOPSIS</span></span>
<span data-ttu-id="89531-103">Erstellt eine neue Active Directory-Konfiguration (Azure NetApp Files, ANF).</span><span class="sxs-lookup"><span data-stu-id="89531-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="89531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89531-104">SYNTAX</span></span>

### <span data-ttu-id="89531-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89531-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89531-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89531-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89531-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89531-107">DESCRIPTION</span></span>
<span data-ttu-id="89531-108">Das **Cmdlet "New-AzNetAppFilesActiveDirectory"** erstellt eine neue Active Directory-Konfiguration für ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="89531-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="89531-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89531-109">EXAMPLES</span></span>

### <span data-ttu-id="89531-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89531-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="89531-111">Mit diesem Befehl wird das Ad-Kennwort von "promt" in die neue Active Directory-Konfiguration für das "MyAnfAccount"-Konto für das ANF-Konto kopiert.</span><span class="sxs-lookup"><span data-stu-id="89531-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="89531-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89531-112">PARAMETERS</span></span>

### <span data-ttu-id="89531-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89531-113">-AccountName</span></span>
<span data-ttu-id="89531-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="89531-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="89531-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="89531-115">-AccountObject</span></span>
<span data-ttu-id="89531-116">Das Konto für das neue Sicherungsrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="89531-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="89531-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="89531-117">-AdName</span></span>
<span data-ttu-id="89531-118">Name des Active Directory-Computers.</span><span class="sxs-lookup"><span data-stu-id="89531-118">Name of the active directory machine.</span></span>
<span data-ttu-id="89531-119">Dieser optionale Parameter wird nur beim Erstellen von Kerberos-Volume</span><span class="sxs-lookup"><span data-stu-id="89531-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="89531-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="89531-120">-BackupOperator</span></span>
<span data-ttu-id="89531-121">Benutzer, die der Active Directory-Gruppe "Integrierter Sicherungsoperator" hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89531-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="89531-122">Eine Liste mit eindeutigen Benutzernamen ohne Domänenbezeichner</span><span class="sxs-lookup"><span data-stu-id="89531-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="89531-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89531-123">-DefaultProfile</span></span>
<span data-ttu-id="89531-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89531-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89531-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="89531-125">-Dns</span></span>
<span data-ttu-id="89531-126">Durch Kommas getrennte Liste der DNS-Server-IP-Adressen (nur IPv4) für die Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="89531-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="89531-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="89531-127">-Domain</span></span>
<span data-ttu-id="89531-128">Name der Active Directory-Domäne</span><span class="sxs-lookup"><span data-stu-id="89531-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="89531-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="89531-129">-KdcIP</span></span>
<span data-ttu-id="89531-130">Kdc-Server-IP-Adressen für den Active Directory-Computer.</span><span class="sxs-lookup"><span data-stu-id="89531-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="89531-131">Dieser optionale Parameter wird nur beim Erstellen von Kerberos-Volume verwendet.</span><span class="sxs-lookup"><span data-stu-id="89531-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="89531-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="89531-132">-OrganizationalUnit</span></span>
<span data-ttu-id="89531-133">Organisationseinheit im Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="89531-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="89531-134">-Password</span><span class="sxs-lookup"><span data-stu-id="89531-134">-Password</span></span>
<span data-ttu-id="89531-135">Nur-Text-Kennwort des Active Directory-Domänenadministrators, der Wert wird in der Antwort maskiert</span><span class="sxs-lookup"><span data-stu-id="89531-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="89531-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89531-136">-ResourceGroupName</span></span>
<span data-ttu-id="89531-137">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="89531-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="89531-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="89531-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="89531-139">Wenn LDAP über SSL/TLS aktiviert ist, muss das selbst signierte Stammzertifizierungsstellenzertifikat des Active Directory-Zertifikatdiensts base64-codiert sein. Dieser optionale Parameter wird nur für duales Protokoll mit LDAP-Benutzerzuordnungsvolumen verwendet.</span><span class="sxs-lookup"><span data-stu-id="89531-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="89531-140">-Site</span><span class="sxs-lookup"><span data-stu-id="89531-140">-Site</span></span>
<span data-ttu-id="89531-141">Die Active Directory-Website, auf die der Dienst die Domänencontrollerermittlung auf</span><span class="sxs-lookup"><span data-stu-id="89531-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="89531-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="89531-142">-SmbServerName</span></span>
<span data-ttu-id="89531-143">Der Name von NetERGEBNIS DES SMB-Servers.</span><span class="sxs-lookup"><span data-stu-id="89531-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="89531-144">Dieser Name wird als Computerkonto im Ad registriert und zum</span><span class="sxs-lookup"><span data-stu-id="89531-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="89531-145">-Username</span><span class="sxs-lookup"><span data-stu-id="89531-145">-Username</span></span>
<span data-ttu-id="89531-146">Benutzername des Active Directory-Domänenadministrators</span><span class="sxs-lookup"><span data-stu-id="89531-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="89531-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89531-147">-Confirm</span></span>
<span data-ttu-id="89531-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89531-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89531-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="89531-149">-WhatIf</span></span>
<span data-ttu-id="89531-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89531-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89531-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89531-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89531-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89531-152">CommonParameters</span></span>
<span data-ttu-id="89531-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89531-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89531-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89531-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89531-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89531-155">INPUTS</span></span>

### <span data-ttu-id="89531-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="89531-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="89531-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89531-157">OUTPUTS</span></span>

### <span data-ttu-id="89531-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="89531-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="89531-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89531-159">NOTES</span></span>

## <span data-ttu-id="89531-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89531-160">RELATED LINKS</span></span>
