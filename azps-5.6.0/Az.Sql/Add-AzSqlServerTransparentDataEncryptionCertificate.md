---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923339"
---
# <span data-ttu-id="642ce-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="642ce-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="642ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="642ce-102">SYNOPSIS</span></span>
<span data-ttu-id="642ce-103">Fügt ein Transparentes Datenverschlüsselungszertifikat für die angegebene SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="642ce-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="642ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="642ce-104">SYNTAX</span></span>

### <span data-ttu-id="642ce-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="642ce-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642ce-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="642ce-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642ce-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="642ce-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642ce-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="642ce-108">DESCRIPTION</span></span>
<span data-ttu-id="642ce-109">Die Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein Zertifikat für transparente Datenverschlüsselung für die angegebene SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="642ce-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="642ce-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="642ce-110">EXAMPLES</span></span>

### <span data-ttu-id="642ce-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="642ce-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="642ce-112">Hinzufügen eines TDE-Zertifikats zu einem Sql Server mithilfe des Ressourcengruppennamens und SQL Server Namen</span><span class="sxs-lookup"><span data-stu-id="642ce-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="642ce-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="642ce-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="642ce-114">Hinzufügen eines TDE-Zertifikats zu den Servern mit Server resourceId</span><span class="sxs-lookup"><span data-stu-id="642ce-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="642ce-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="642ce-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="642ce-116">Hinzufügen eines TDE-Zertifikats zu allen SQL-Servern in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="642ce-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="642ce-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="642ce-117">PARAMETERS</span></span>

### <span data-ttu-id="642ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642ce-118">-DefaultProfile</span></span>
<span data-ttu-id="642ce-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="642ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642ce-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="642ce-120">-PassThru</span></span>
<span data-ttu-id="642ce-121">Gibt bei erfolgreicher Ausführung das hinzugefügte Zertifikatobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="642ce-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="642ce-122">-Password</span><span class="sxs-lookup"><span data-stu-id="642ce-122">-Password</span></span>
<span data-ttu-id="642ce-123">Das Kennwort für transparentes Datenverschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="642ce-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="642ce-124">-PrivateBlob</span></span>
<span data-ttu-id="642ce-125">Das private Blob für zertifikat für transparente Datenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="642ce-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="642ce-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="642ce-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="642ce-128">-ServerName</span></span>
<span data-ttu-id="642ce-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="642ce-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="642ce-130">-SqlServer</span></span>
<span data-ttu-id="642ce-131">Das Sql Server-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="642ce-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="642ce-132">-SqlServerResourceId</span></span>
<span data-ttu-id="642ce-133">Die Sql Server-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="642ce-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642ce-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="642ce-134">-Confirm</span></span>
<span data-ttu-id="642ce-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="642ce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642ce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642ce-136">-WhatIf</span></span>
<span data-ttu-id="642ce-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="642ce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642ce-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="642ce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642ce-139">CommonParameters</span></span>
<span data-ttu-id="642ce-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642ce-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="642ce-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642ce-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="642ce-142">INPUTS</span></span>

### <span data-ttu-id="642ce-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="642ce-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="642ce-144">System.String</span><span class="sxs-lookup"><span data-stu-id="642ce-144">System.String</span></span>

## <span data-ttu-id="642ce-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="642ce-145">OUTPUTS</span></span>

### <span data-ttu-id="642ce-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="642ce-146">System.Boolean</span></span>

## <span data-ttu-id="642ce-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="642ce-147">NOTES</span></span>

## <span data-ttu-id="642ce-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="642ce-148">RELATED LINKS</span></span>
